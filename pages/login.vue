<template>
  <div>
    <a href="#" @click.prevent="login" class="p-8 text-3xl font-semibold text-gray-700 mx-auto w-full">Login</a>

    <div v-if="$auth.loggedIn" class="p-8 text-5xl font-bold text-blue-700 mx-auto w-full">{{ $auth.user.name }}</div>
  </div>

</template>

<script>
export default {
  methods: {
    login () {
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email: 'c.jeandey@gmail.com',
          password: 'password',
        }
      })
    }
  }

}
</script>
