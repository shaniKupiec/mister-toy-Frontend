<template>
  <section class="main-layout">
    <app-header />
    <main class="main-app">
    <router-view />
    </main>
    <app-footer />
  </section>
</template>

<script>
import appHeader from './components/app-header.vue'
import appFooter from './components/app-footer.vue'

export default {
  name: 'app',
  created() {
    this.$store.dispatch({ type: 'loadToys'})
    this.$store.dispatch({ type: 'loadLoggedInUser'})
  },
  methods: {},
  components: {
    appHeader,
    appFooter
  },
}
</script>