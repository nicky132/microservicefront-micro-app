<template>
  <div>
    <h1>child-vue2-page2</h1>
    <div class="child-vue2-test-btn" @click="sendData">test</div>
    <img src="../assets/micro-app-logo.png" alt="micro-app-logo" />
  </div>
</template>

<script>

export default {
  name: 'page2',
  data() {
    return {
    }
  },
  methods: {
    sendData() {
      //console.log('sendData');
      window.microApp.dispatch({ myname: 'child-vue-- 子应用向基座发送消息' })
    }
  }
}
</script>

<style>
.child-vue2-test-btn {
  height: 40px;
  width: 100px;
  background-color: red;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  font-size: 20px;
  font-weight: bolder;
  margin: 0 auto;
  user-select: none;
}
</style>
