---
title: 广州今日天气
layout: page
---

{% raw %}

<div id="app" class="weather-card">
  <header class="weather-header">
    <h1>{{ city }}今日天气</h1>
    <p class="date">{{ date }}</p>
  </header>
  <section class="weather-body">
    <div class="temperature">{{ temperature }}</div>
    <p class="description">{{ description }}</p>
    <ul class="details">
      <li>体感温度：{{ feelsLike }}</li>
      <li>湿度：{{ humidity }}</li>
      <li>风向：{{ windDirection }}</li>
      <li>风速：{{ windSpeed }}</li>
    </ul>
  </section>
  <section class="tips">
    <h2>出行建议</h2>
    <p>{{ suggestion }}</p>
  </section>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.prod.js"></script>
<script>
const { createApp } = Vue;

createApp({
  data() {
    return {
      city: '广州',
      date: new Date().toLocaleDateString('zh-CN', {
        year: 'numeric',
        month: 'long',
        day: 'numeric',
        weekday: 'long'
      }),
      temperature: '29°C',
      feelsLike: '体感 31°C',
      description: '多云间晴，湿度较大，傍晚有轻微阵雨的可能。',
      humidity: '72%',
      windDirection: '东北偏东',
      windSpeed: '10 km/h',
      suggestion: '天气较为闷热，记得携带雨具和补充水分，午后防晒同样不能少。'
    };
  }
}).mount('#app');
</script>

<style>
.weather-card {
  max-width: 560px;
  margin: 2.5rem auto;
  padding: 2.5rem;
  border-radius: 20px;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.95), rgba(236, 248, 255, 0.9));
  box-shadow: 0 20px 45px rgba(15, 55, 95, 0.18);
  color: #12344d;
  text-align: center;
  backdrop-filter: blur(6px);
}

.weather-header h1 {
  margin-bottom: 0.25rem;
  font-size: 2rem;
  font-weight: 700;
}

.weather-header .date {
  margin: 0;
  font-size: 1rem;
  color: #4c6b85;
}

.weather-body {
  margin: 2rem 0 1.5rem;
}

.temperature {
  font-size: 3rem;
  font-weight: 700;
  color: #1f7acb;
  margin-bottom: 0.5rem;
}

.description {
  margin: 0 auto 1.5rem;
  max-width: 360px;
  line-height: 1.6;
}

.details {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.75rem;
  font-size: 0.95rem;
  color: #345265;
}

.details li {
  background-color: rgba(255, 255, 255, 0.6);
  border-radius: 12px;
  padding: 0.75rem 0.5rem;
}

.tips {
  margin-top: 2rem;
  padding-top: 1.5rem;
  border-top: 1px solid rgba(31, 122, 203, 0.15);
}

.tips h2 {
  font-size: 1.25rem;
  margin-bottom: 0.75rem;
}

.tips p {
  margin: 0;
  line-height: 1.7;
}

@media (max-width: 600px) {
  .weather-card {
    margin: 1.5rem;
    padding: 1.75rem;
  }

  .details {
    grid-template-columns: 1fr;
  }
}
</style>

{% endraw %}
