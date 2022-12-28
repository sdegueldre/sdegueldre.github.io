<script setup lang="ts">
import backgroundPositioningUtilityVideo from "../assets/video/background positioning utility.mp4";
import backgroundShapesVideo from "../assets/video/background shapes.mp4";
import animatedCutoutsVideo from "../assets/video/animated cutouts.mp4";
import webGlFiltersVideo from "../assets/video/webGL filters.mp4";
import imageGridVideo from "../assets/video/image grid.mp4";
import imageOptimizationVideo from "../assets/video/image optimization.mp4";
</script>

<template>
  <main id="about">
    <h1 class="text-primary">Hi, I'm Sam!</h1>
    <p class="intro">
      I'm a web developer currently working at
      <a href="https://odoo.com" target="_blank">Odoo</a>. Most of the work I do
      is open source, you can find me on
      <a href="https://github.com/sdegueldre" target="_blank">GitHub</a> and
      <a href="https://www.linkedin.com/in/samueldegueldre/" target="_blank"
        >LinkedIn</a
      >. I like tinkering with various things.
    </p>
  </main>
  <section id="work">
    <h2 class="section-title">Work</h2>
    <div class="details">
      <h3 class="role">
        Senior full-stack developer @<a
          class="company"
          href="https://odoo.com"
          target="_blank"
          >Odoo</a
        >
      </h3>
      <small class="team">JS framework team</small>
    </div>
    <div class="description">
      <small class="team-description">
        The JS framework team maintains the client side application framework
        used within the company as well as the web client, including
        <a href="https://github.com/odoo/owl" target="_blank">Owl</a>, our
        component-based UI library.
      </small>
      <p class="my-contribution">
        I personally wrote almost the entirety of the
        <a
          href="https://github.com/odoo/owl/blob/master/doc/reference/reactivity.md"
          target="_blank"
          >Owl reactivity system</a
        >, it is a mostly transparent, proxy-based reactivity system that can be
        used on its own or be integrated within other libraries. It is optimized
        for rendering: components are only subscribed to what they read, and
        only the components that depend on the specific piece of state that
        changed gets rerendered. Check out
        <a
          href="https://sdegueldre.github.io/react-owl-reactivity/"
          target="_blank"
          >this demo</a
        >
        to see it in action in React.
      </p>
      <p class="my-contribution">
        My responsibilities included onboarding newcomers, reviewing and merging
        pull-requests, conducting technical interviews, writing tests and
        documentation, giving internal and external training on the framework,
        assisting other teams in their usage of the framework and its tools,
        profiling and optimizing client-side code to reduce memory footprint and
        much more.
      </p>
    </div>
    <div class="details">
      <h3 class="role">
        Junior full-stack developer @<a
          class="company"
          href="https://odoo.com"
          target="_blank"
          >Odoo</a
        >
      </h3>
      <small class="team">Website team</small>
    </div>
    <div class="description">
      <small class="team-description">
        The website team is responsible for the website application, including a
        full-featured WYSIWYG website creation tool.
      </small>
      <p class="my-contribution">
        During my time in the website team, I developed some really cool
        features, including
        <a target="_blank" :href="backgroundPositioningUtilityVideo"
          >a better background positioning system</a
        >,
        <a target="_blank" :href="backgroundShapesVideo"
          >theme-synchronized background shapes</a
        >,
        <a target="_blank" :href="animatedCutoutsVideo">animated SVG cutouts</a
        >, <a target="_blank" :href="webGlFiltersVideo">WebGL image filters</a>,
        <a target="_blank" :href="imageGridVideo">a much better image grid</a>
        and
        <a target="_blank" :href="imageOptimizationVideo"
          >automatic image optimization</a
        >.
      </p>

      <p class="my-contribution">
        My responsibilities included improving the robustness of existing code
        to asynchronous race conditions, writing unit and end-to-end tests, and
        towards the end of my stay, onboarding newcomers as well as reviewing
        and merging their code.
      </p>
    </div>
  </section>
  <section id="tinkerings">
    <h2 class="section-title">Tinkerings</h2>
    <h3 class="subtitle">random things I've done for fun</h3>
    <div class="details">
      <h3 class="project">DFT visualizer</h3>
      <small class="team"
        >A simple spectrogram visualizer using the WebAudio API</small
      >
    </div>
    <div class="description">
      <a href="https://sdegueldre.github.io/DFT-visualizer/" target="_blank">
        <img src="../assets/img/dft-visualizer.png" />
      </a>
    </div>
  </section>
  <footer>
    <span class="copyright">© Samuel Degueldre 2022 </span>
  </footer>
</template>

<style scoped>
main {
  height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

h1.text-primary {
  font-size: 4rem;
  text-align: center;
}

.intro {
  text-align: left;
  max-width: 35em;
  margin-left: auto;
  margin-right: auto;
}

.section-title {
  width: 100%;
  border-bottom: 1px solid var(--color-text);
  padding-left: 1rem;
}

section {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}

.details,
.description {
  width: 100%;
  padding-top: 1rem;
  padding-bottom: 1rem;
}
@media screen and (min-width: 890px) {
  .details {
    width: 30%;
    padding-right: 1rem;
  }
  .description {
    width: 70%;
    padding-left: 1rem;
  }
}

.details {
  text-align: right;
}

p {
  margin-bottom: 0.5rem;
  margin-top: 0.5rem;
}

.team-description {
  display: block;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--color-border);
}

img {
  width: 100%;
}

footer {
  height: 10rem;
  border-top: 1px solid var(--color-border);
  max-width: 100%;
  position: relative;
  padding: 0;
}

footer > * {
  margin-left: auto;
  margin-right: auto;
  display: block;
  padding-left: 2rem;
  padding-right: 2rem;
  max-width: var(--content-width);
}

.copyright {
  padding-top: 1rem;
  padding-bottom: 1rem;
  margin-top: auto;
  text-align: right;
}

.subtitle {
  font-weight: 100;
  font-size: small;
  font-family: Roboto;
  width: 100%;
  padding-left: 1rem;
}
</style>
