<script setup>
import { ref } from 'vue'

let notifications = ref(0)

function addValue() {
  notifications.value++
  console.log(notifications)
}
function minusValue() {
  if (notifications.value > 0) {
    notifications.value--
  }
}

addValue()
minusValue()
</script>

<template>
  <div class="wrapper">
    <div class="profile">
      <div class="notification" v-show="notifications > 0">{{ notifications }}</div>
    </div>
    <div class="button-wrapper">
      <button class="button" @click="minusValue">-</button>
      <button class="button" @click="addValue">+</button>
    </div>
    <div v-if="notifications == 0">Un video mas mi gente, Me encanta esta vaina😎</div>
    <div v-else>MMMMMMMMMMMMMMMMMMMMMMMM🤤</div>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: #80adbf;
  width: 60%;
  border-radius: 12px;
  margin: 0 auto;
  padding-top: 32px;
  overflow: hidden;
}
.profile {
  background-color: #070c0d;
  width: 120px;
  height: 120px;
  border-radius: 100%;
  margin: 0 auto;
  position: relative;
  background-image: url('https://us-tuna-sounds-images.voicemod.net/47aa6368-d200-43b2-b2c7-f85603cf932e-1696608463988.jpg');
  background-size: cover;
}
.profile img {
  width: 100%;
  height: 100%;
  border-radius: 100%;
}
.notification {
  position: absolute;
  background-color: #4a808c;
  min-width: 18px;
  height: 18px;
  border-radius: 100%;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  top: 0;
  right: 0;
}
.button-wrapper {
  margin-top: 12px;
  text-align: center;
  background-color: #80adbf;
  padding: 10px 0;
}
.button {
  background-color: #225459;
  border-radius: 4px;
  padding: 2px 0;
  font-weight: bold;
  color: white;
  display: inline-block;
  width: 40px;
  cursor: pointer;
  border: none;
  outline: none;
}
.button:first-child {
  margin-right: 32px;
}
.button:last-child {
  margin-left: 32px;
}
</style>
