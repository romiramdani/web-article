<template>
  <div id="app">
    <Header/>
    <main class="container">
      <Hero />
      <Article />
    </main>
  </div>
</template>

<script>
  import Header from "@/components/TheHeader.vue"
  import Hero from "@/components/TheHero.vue"
  import Article from "@/components/CardArticle.vue"
  export default {
    components: {
      Header,
      Hero,
      Article
    },
  }
</script>