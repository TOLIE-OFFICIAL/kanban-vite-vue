<script setup>
import Tasks from "./Tasks.vue";
// import Section from './components/Section.vue'
</script>

<template>
  <aside>
    <logo>Board</logo>
    <list>
      <li>11111</li>
      <li>22222</li>
    </list>
  </aside>
  <section>
    <header>
      <logo></logo>
      <button>Remove this Event</button>
    </header>
    <article>
      <Tasks></Tasks>
      <Tasks></Tasks>
      <Tasks></Tasks>
    </article>
  </section>
</template>

<style scoped>
aside {
  width: 200px;
  height: 100%;
  background-color: aquamarine;
}
section {
  flex: 1;
  height: 100%;
}
header{
  height: 10%;
}
article {
  width: 100%;
  height: 90%;
  padding: 0 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
