<template>
  <div class="main">
      <h1>회원가입</h1>
      
      <div class="flex">
        <div class="flex login-box">
          <span>아이디 </span>
          <input class="margin" type="text" v-model="username">
        </div>
        <div class="flex login-box">
          <span>비밀번호 </span>
          <input class="margin" type="password" v-model="password">
        </div>
      </div>
      <div class="flex">
          <input class="margin" type="button" value="회원가입" @click="register">

      </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      username: '',
      password:'',
    }
  },
  methods: {
    register() {
      if (this.username.length <= 0) {
        window.alert('아이디를 확인해주세요')
        return
      }
      else if (this.password.length <= 0) {
        window.alert('비밀번호를 확인해주세요')
        return
      }
      localStorage.setItem('id', this.username)
      localStorage.setItem('pwd',this.password )
      this.$router.push('/')
    }
  }
}
</script>


<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  
}

.flex {

  display: flex;
  flex-direction: column;
}

.margin {
  margin-bottom: 20px;
}

.display-flex{
  display: flex;
}

.login-box{
 min-width: 250px;
 justify-content: space-between;
}

</style>