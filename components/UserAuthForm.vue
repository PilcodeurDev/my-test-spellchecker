<template>
  <v-main>
    <v-container fluid fill-height>
      <v-layout align-center justify-center>
        <v-flex xs12 sm8 md4>
          <v-card class="elevation-12">
            <v-toolbar color="blue">
              <v-toolbar-title>Login form</v-toolbar-title>
            </v-toolbar>
            <v-card-text>
              <v-form>
                <v-text-field name="email" label="Email" type="text" v-model="email"></v-text-field>
                <v-text-field id="password" name="password" label="Password" type="password"
                  v-model="password"></v-text-field>
              </v-form>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <button @click="submitForm">Login</button>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-main>
</template>

<script>

export default {
  data() {
    return {
      showPassword: false,
      userInfo: {
        email: '',
        password: ''
      },
    }
  },
  props: ["submitForm"]
};
</script>

<style>
</style>
