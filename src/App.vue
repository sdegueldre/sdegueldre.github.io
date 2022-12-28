<script setup lang="ts">
import { ref } from "vue";
import type { Ref } from 'vue'
import HomeView from "./views/HomeView.vue";

const nav: Ref<HTMLElement | null> = ref(null);
const scrollToAnchor = (ev: MouseEvent) => {
  ev.preventDefault();
  const target: HTMLElement = document.querySelector(
    (ev.target as unknown as HTMLAnchorElement).getAttribute("href") as string
  )!;
  window.scrollTo({
    top:
      target.getBoundingClientRect().y +
      window.scrollY -
      nav.value!.clientHeight,
    behavior: "smooth",
  });
};
</script>

<template>
  <header>
    <nav ref="nav">
      <a href="#about" v-on:click="scrollToAnchor">About</a>
      <a href="#work" v-on:click="scrollToAnchor">Work</a>
      <a href="#tinkerings" v-on:click="scrollToAnchor">Tinkerings</a>
    </nav>
  </header>
  <HomeView />
</template>

<style scoped>
header {
  position: fixed;
  left: 0;
  right: 0;
}

nav {
  text-align: right;
  padding-top: 0.5rem;
  padding-bottom: 1rem;
  background: linear-gradient(
    to top,
    transparent,
    var(--color-background) 1rem
  );
  margin-right: -1rem;
  margin-left: -1rem;
}

a.router-link-exact-active {
  color: var(--color-text);
}

nav a {
  display: inline-block;
  padding: 0 1rem;
}

nav a:not(:first-of-type) {
  border-left: 1px solid var(--color-border);
}
</style>
