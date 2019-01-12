<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        Let's learn about NuxtJS, VueJS and Vuetify together
      </h1>
      <h2 class="subtitle">
        My geometric Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="/users"
          target=""
          class="button--green">Users</a>
        <a
          href="/vuetify"
          target=""
          class="button--green">vuetify</a>
        <a
          href="/booking"
          target=""
          class="button--green">Booking</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
