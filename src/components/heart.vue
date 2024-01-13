<script setup>
const useConfetti = () => {
  const defaults = {
    spread: 360,
    ticks: 100,
    gravity: 0.2,
    decay: 0.94,
    startVelocity: 30,
    shapes: ["heart"],
    colors: ["FFC0CB", "FF69B4", "FF1493", "C71585"],
  };

  confetti({
    ...defaults,
    particleCount: 70,
    scalar: 2,
  });

confetti({
  ...defaults,
  particleCount: 50,
  scalar: 3,
});

confetti({
  ...defaults,
  particleCount: 25,
  scalar: 4,
});

confetti({
  ...defaults,
  particleCount: 10,
  scalar: 5,
});
};

const expandHeart = () => {
  useConfetti();
  document.getElementById("heart").classList.add("clicked");
  document.getElementById("lisa").style.scale = "3.3";
  document.getElementById("lisa").style.zIndex = "1000";
  let elements = document.querySelectorAll('.finger');

// Применяем свойства ко всем найденным элементам
elements.forEach(function(element) {
    element.style.marginTop = "1000px ";  // Пример добавления свойства color
    // Добавьте здесь другие свойства по необходимости
});
};
</script>

<template>
  <div class="abs">
    <div class="fingers_1">
      <img
        src="../assets/finger.png"
        alt=""
        class="finger"
        v-for="index in 3"
        :key="index"
      />
    </div>
    <div class="heart" @click="expandHeart" id="heart">
      <img src="../assets/1.png" alt="" id="cat_left" />
      <img src="../assets/2.png" alt="" id="cat_right" />
    </div>
    <div class="fingers_2">
      <img
        src="../assets/finger.png"
        alt=""
        class="finger"
        v-for="index in 3"
        :key="index"
      />
    </div>
  </div>
</template>

<style></style>
