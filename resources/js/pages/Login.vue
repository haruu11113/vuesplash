<template>
  <div class="container--small">
    <ul class="tab">
      <li
        class="tab__item"
        :class="{'tab__item--active': tab === 1 }"
        @click="tab = 1"
      >Login</li>
      <li
        class="tab__item"
        :class="{'tab__item--active': tab === 2 }"
        @click="tab = 2"
      >Register</li>
    </ul>
    <div class="panel" v-show="tab === 1">
        <div class="panel" v-show="tab === 1">
          <form class="form">
            <label for="login-email">Email</label>
            <input type="text" class="form__item" id="login-email" v-model="loginForm.email">
            <label for="login-password">Password</label>
            <input type="password" class="form__item" id="login-password" v-model="loginForm.password">
            <div class="form__button">
                <form class="form" @submit.prevent="login">
            </div>
          </form>
        </div>
    </div>
    <div class="panel" v-show="tab === 2">
        login
    </div>
  </div>
</template>

<script>
export default {
    data () {
        return {
          tab: 1,
          loginForm: {
            email: '',
            password: ''
          },
        }
    },
    methods: {
        login () {
          console.log(this.loginForm)
        }
      }
}
</script>
