<template>
  <heart />
  <div id="lisa"/>
</template>
<script setup>
import heart from "./components/heart.vue";
</script>

<style>
html {
  background: #ffb7e3;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  place-items: center;
  background: rgb(255, 236, 252);
  height: 100vh;
  overflow: hidden;
  position: relative;
}
.abs {
  position: absolute;
  z-index: 999;
}
.heart {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-block: 2rem;
  transition: all ease-in-out 0.5s;
}
.heart > * {
  transition: all ease-in-out 0.5s;
}
.clicked > #cat_left {
  margin-right: 32vw;
}
.clicked {
  scale: 1.2;
}
.finger {
  height: 10vh;
  animation: fingerMove 1s infinite;
}
@media screen and (max-width: 700px) {
  #cat_left,
  #cat_right {
    height: 20vh;
  }
  .finger {
    height: 5vh;
    transition: all ease 1s;
  }
}

@keyframes fingerMove {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(20%);
  }
}
.fingers_1,
.fingers_2 {
  display: flex;
  justify-content: space-between;
  gap: 3rem;
}
.fingers_1 {
  rotate: 180deg;
}
#lisa {
  height: 100px;
  background-image: url("./assets/lisa.png");
  background-size: cover;
  width: 60px;
  transition: all ease-out 1s;
}
</style>
