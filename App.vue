<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
</script>

<template>
  <div class="portfolio">

    <!-- Navigation -->
    <nav class="navbar">
      <h2 class="logo">Joebest</h2>

      <button class="menu-btn" @click="menuOpen = !menuOpen">
        ☰
      </button>

      <div class="nav-links" :class="{ show: menuOpen }">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>

    <!-- Hero -->
    <section id="home" class="hero">
      <div>
        <p class="welcome">WELCOME TO MY PORTFOLIO</p>

        <h1>
          Hi, I'm <span>Joebest</span>
        </h1>

        <h2>Frontend Developer</h2>

        <p class="intro">
          I create responsive and user-friendly websites
          using modern frontend technologies.
        </p>

        <a href="#projects" class="button">
          View My Projects
        </a>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="section">
      <h2>About Me</h2>

      <p>
        I am a frontend developer learning to build modern,
        responsive and interactive websites. I enjoy turning
        ideas into clean and useful web experiences.
      </p>
    </section>

    <!-- Skills -->
    <section id="skills" class="section">
      <h2>My Skills</h2>

      <div class="skills">
        <div>HTML</div>
        <div>CSS</div>
        <div>JavaScript</div>
        <div>Vue.js</div>
        <div>Responsive Design</div>
        <div>Git & GitHub</div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects" class="section">
      <h2>My Projects</h2>

      <div class="projects">

        <article class="project">
          <h3>Portfolio Website</h3>
          <p>
            A responsive personal portfolio website
            built with Vue.js.
          </p>
          <button>View Project</button>
        </article>

        <article class="project">
          <h3>Todo App</h3>
          <p>
            A simple application for creating and
            managing tasks.
          </p>
          <button>View Project</button>
        </article>

        <article class="project">
          <h3>Landing Page</h3>
          <p>
            A modern landing page designed for a
            fictional business.
          </p>
          <button>View Project</button>
        </article>

      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="section contact">
      <h2>Contact Me</h2>

      <p>
        Interested in working together?
      </p>

      <a href="mailto:your-email@example.com" class="button">
        Send Me an Email
      </a>
    </section>

    <!-- Footer -->
    <footer>
      <p>© 2026 Joebest. All rights reserved.</p>
    </footer>

  </div>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Arial, sans-serif;
  background: #f5f7fb;
  color: #222;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 8%;
  background: white;
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
}

.logo {
  font-size: 24px;
}

.nav-links {
  display: flex;
  gap: 25px;
}

.nav-links a {
  text-decoration: none;
  color: #222;
  font-weight: bold;
}

.menu-btn {
  display: none;
  border: none;
  background: none;
  font-size: 25px;
}

.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  padding: 60px 8%;
  background: white;
}

.welcome {
  font-size: 14px;
  font-weight: bold;
  margin-bottom: 15px;
}

.hero h1 {
  font-size: 55px;
  margin-bottom: 10px;
}

.hero h1 span {
  color: #2563eb;
}

.hero h2 {
  font-size: 30px;
  margin-bottom: 20px;
}

.intro {
  max-width: 550px;
  line-height: 1.7;
  margin-bottom: 30px;
}

.button {
  display: inline-block;
  background: #2563eb;
  color: white;
  padding: 13px 22px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: bold;
}

.section {
  padding: 80px 8%;
  text-align: center;
}

.section h2 {
  font-size: 35px;
  margin-bottom: 25px;
}

.section > p {
  max-width: 700px;
  margin: auto;
  line-height: 1.8;
}

.skills {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  max-width: 800px;
  margin: 30px auto;
}

.skills div {
  background: white;
  padding: 25px;
  border-radius: 8px;
  font-weight: bold;
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
}

.projects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 25px;
  margin-top: 30px;
}

.project {
  background: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
}

.project h3 {
  margin-bottom: 15px;
}

.project p {
  line-height: 1.6;
  margin-bottom: 20px;
}

.project button {
  border: none;
  background: #2563eb;
  color: white;
  padding: 10px 18px;
  border-radius: 5px;
}

.contact {
  background: white;
}

footer {
  text-align: center;
  padding: 25px;
  background: #111827;
  color: white;
}

@media (max-width: 700px) {

  .menu-btn {
    display: block;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: 70px;
    right: 5%;
    background: white;
    padding: 20px;
    flex-direction: column;
    box-shadow: 0 3px 15px rgba(0, 0, 0, 0.15);
  }

  .nav-links.show {
    display: flex;
  }

  .hero h1 {
    font-size: 40px;
  }

  .hero h2 {
    font-size: 24px;
  }

  .skills,
  .projects {
    grid-template-columns: 1fr;
  }
}
</style>
