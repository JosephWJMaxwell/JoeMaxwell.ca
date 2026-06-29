<template>
  <main class="page">
    <section class="card">
      <p class="eyebrow">JoeMaxwell.ca</p>
      <h1>{{ profile.name }}</h1>
      <p class="headline">{{ profile.title }}</p>
      <p class="summary">{{ profile.summary }}</p>

      <div class="links">
        <a :href="profile.linkedin" target="_blank" rel="noreferrer">LinkedIn</a>
      </div>
    </section>

    <section class="card">
      <h2>Experience Highlights</h2>
      <ul>
        <li v-for="item in highlights" :key="item">{{ item }}</li>
      </ul>
    </section>

    <section class="card">
      <h2>Core Skills</h2>
      <div class="chips">
        <span v-for="skill in skills" :key="skill">{{ skill }}</span>
      </div>
    </section>
  </main>
</template>

<script setup>
const profile = {
  name: "Joe Maxwell",
  title: "Software Developer",
  summary:
    "Building practical software with a focus on modern web development, clear UX, and reliable delivery.",
  linkedin: "https://www.linkedin.com/in/joey-maxwell/",
};

const highlights = [
  "Built full-stack products using modern JavaScript and .NET ecosystems.",
  "Shipped client-facing features from concept to production.",
  "Focused on maintainable architecture, clean code, and user outcomes.",
];

const skills = [
  "Vue.js",
  "TypeScript",
  "JavaScript",
  "C# / .NET",
  "REST APIs",
  "PostgreSQL",
  "Azure",
  "GitHub Actions",
];
</script>
