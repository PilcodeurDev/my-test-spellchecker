<template>
  <div class="contained">
    <!-- Header -->
    <div class="d-flex justify-content-between align-items-center m-3 mb-5">
      <nuxt-link to="/" class="mx-2 text-decoration-none fw-bold">
        <h1>My SpellChecker</h1>
      </nuxt-link>

      <div v-if="$auth.loggedIn" class="m-2">
        {{ $auto.user.email }}
        <v-btn text>Logout</v-btn>
        <nuxt-link to="/" class="mx-2 text-decoration-none fw-bold">Logout</nuxt-link>
      </div>
      <div v-else>
        <nuxt-link to="/login" class="mx-2 main_color">Login</nuxt-link>
      </div>
    </div>
    <nuxt />
  </div>
</template>

<style scoped>
.contained {
  min-height: 100vh;
  background: #16ae6f;
}
</style>
