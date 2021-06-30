<!--
 * @Author: hhhhhq
 * @Date: 2021-06-30 16:19:39
 * @LastEditors: hhhhhq
 * @LastEditTime: 2021-06-30 17:15:19
 * @Description: file content
-->
<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <div class="content">
    <router-link to="/">Home</router-link>
    <router-link to="/guide">Guide</router-link>

    <router-view v-slot="{ Component, route }">
      <transition
        :enter-active-class="route.meta.enterClass"
        :leave-active-class="route.meta.leaveClass"
      >
        <component :is="Component" />
      </transition>
    </router-view>
  </div>
</template>

<script setup>
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.content {
  width: 40%;
  max-width: 500px;
  margin: 0 auto;
  position: relative;
}

a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin-right: 1em;
}

.page {
  position: absolute;
  top: 30px;
}

a:hover,
a.router-link-active {
  border-bottom: 2px solid #3498db;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}
</style>
