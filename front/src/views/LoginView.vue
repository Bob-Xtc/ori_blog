<template>
  <div class="login">
    <h1 class="title">Ori Blog</h1>
    <div class="login-wrapper">
      <a-form>
        <a-form-item>
          <p class="login-username">Username</p>
          <a-input v-model="username"></a-input>
        </a-form-item>
        <a-form-item>
          <p class="login-password">Password</p>
          <a-input-password v-model="password"></a-input-password>
        </a-form-item>
        <a-form-item>
          <a-button type="primary">Login</a-button>
        </a-form-item>
      </a-form>
    </div>
    <div class="to-register-wrap">
      <p>
        Don't have an account? Click
        <a href="/register">here</a>
        to create
      </p>
    </div>
  </div>
</template>

<script>
import { reactive, toRefs } from "vue";

export default {
  name: "LoginView",
  setup() {
    const loginFrom = reactive({
      username: "",
      password: "",
    });

    return {
      ...toRefs(loginFrom),
    };
  },
};
</script>

<style lang="stylus" scoped>
.login-wrapper {
  border: 1px solid #c8c9cc;
  border-radius: 5px;
  width: 400px;
  padding: 40px 30px;
  margin: 0 auto;
  text-align: left;
}

.ant-btn {
  width: 100%;
  margin-top: 20px;
}

.to-register-wrap {
  border: 1px solid #c8c9cc;
  border-radius: 5px;
  width: 400px;
  font-size: 14px
  padding: 15px 30px 0;
  margin: 20px auto;
}
</style>