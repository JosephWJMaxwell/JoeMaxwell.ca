<template>
  <main class="page">
    <section class="card">
      <h1>{{ profile.name }}</h1>
      <p class="headline">{{ profile.title }}</p>
      <p class="summary">{{ profile.summary }}</p>

      <div class="links">
        <a :href="profile.linkedin" target="_blank" rel="noreferrer">LinkedIn</a>
      </div>
    </section>

    <section class="card">
      <h2>Here is what I'm about as a developer</h2>
      <div class="about-grid">
        <article v-for="section in aboutSections" :key="section.title" class="about-block">
          <h3>{{ section.title }}</h3>
          <p>{{ section.body }}</p>
        </article>
      </div>
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
    "Building practical software with a focus on clarity, reliability, and modern full-stack development.",
  linkedin: "https://www.linkedin.com/in/joey-maxwell/",
};

const aboutSections = [
  {
    title: "How I build",
    body:
      "I build with a focus on clarity, reliability, and usability. I like creating software that feels clean to use, is easy to maintain, and solves real problems without unnecessary complexity.",
  },
  {
    title: "What people can expect from me",
    body:
      "People can expect thoughtful implementation, steady progress, and attention to detail. I care about writing maintainable code, communicating clearly, and building solutions that are practical and dependable.",
  },
  {
    title: "Where I'm growing",
    body:
      "I'm continuing to grow in cloud development, modern full-stack architecture, and building polished applications with strong foundations. I'm especially interested in deepening my work with Azure, .NET, front-end frameworks, and database-driven systems.",
  },
];

const skills = [
  "Vue.js",
  "Angular",
  "TypeScript",
  "JavaScript",
  "C# / .NET",
  "SQL Server",
  "PostgreSQL",
  "GitHub",
  "Azure",
  "REST APIs",
  "GitHub Actions",
  "CI/CD",
];
</script>
