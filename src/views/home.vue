<template>
  <div class='main text' @click="gotoMain">
    <h1>안녕하세요<br>이번에 IWOP 24기에 지원하게 된<br>이상윤이라고 합니다</h1>
  </div>
</template>

<script>
export default {
  methods: {
    gotoMain() {
      localStorage.clear()
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

.text {
  text-align: center;
}

.text:hover {
  cursor: pointer;

  background-image: linear-gradient(90deg, red, orange, yellow, green, blue, navy, purple);
  -webkit-background-clip: text;
  color: transparent;
}
</style>