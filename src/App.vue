<template>
  <div id="app">
    <section class="container">
      <header>
        <h5 class="title">Experienced & Multi-Talented</h5>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam tortor leo, porttitor vel dictum at, aliquam et augue. Duis vel molestie risus, ut lobortis felis.</p>
      </header>

      <div class="parent">
        <ItemBlock v-for="n in 8" :key="n" class="item" />
      </div>
    </section>
  </div>
</template>

<script>
import ItemBlock from "@/components/ItemBlock";

export default {
  components: {
    ItemBlock,
  },
  name: "App",
};
</script>


<style>
/* import fonts  */
@font-face {
  font-family: "ProximaNova";
  src: url(./fonts/ProximaNova.ttf);
}
@font-face {
  font-family: "Gotham";
  src: url(./fonts/Gotham-Bold.ttf);
}

.container {
  max-width: 1536px;
  padding: 0 20px;
  margin: auto;
}

body {
  background-color: #1c1f26;
  /* font-family: "Gotham", sans-serif; */
  font-family: "ProximaNova", sans-serif;
  color: white;
}

.title {
  font-size: 37px;
  font-weight: 500;
  text-align: center;
  margin-bottom: 50px;
  position: relative;
  /* font-family: "Gotham", sans-serif; */
}
.title::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: -25px;
  margin: auto;
  width: 40px;
  height: 2px;
  background: white;
}

header {
  max-width: 700px;
  margin: auto;
}
header p {
  color: #65757e;
  text-align: center;
  font-size: 19px;
  line-height: 25px;
  letter-spacing: -0.6px;
}

.parent {
  margin-top: 50px;
  display: grid;
  grid-template-columns: repeat(1, minmax(0, 1fr));
  align-items: flex-start;
  gap: 25px;
}

/* Responsive section  */
@media (min-width: 768px) {
  .parent {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
@media (min-width: 1024px) {
  .parent {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}
@media (min-width: 1280px) {
  .parent {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}
</style>
