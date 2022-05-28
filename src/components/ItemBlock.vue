<template>
  <div class="item">
    <div class="head">
      <img src="@/assets/info.png" height="40px" alt />
    </div>
    <div class="body">
      <h5>BLOCK</h5>
      <p
        :style="{ maxHeight: seeMore ? '' : '43px'}"
      >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam tortor leo, porttitor vel dictum at, aliquam et augue. Duis vel molestie risus, ut lobortis felis.</p>
      <button @click="seeMore = !seeMore">
        <PlusIcon v-if="!seeMore" style="width:20px;hight:20px;color:white" />
        <MinusIcon v-else style="width:20px;hight:20px;color:white" />
      </button>
    </div>
  </div>
</template>

<script>
import PlusIcon from "@/components/icons/PlusIcon.vue";
import MinusIcon from "@/components/icons/MinusIcon.vue";
export default {
  components: {
    PlusIcon,
    MinusIcon,
  },
  data() {
    return {
      seeMore: false,
    };
  },
};
</script>

<style scoped>
.item {
  background: gray;
  border-radius: 4px 4px 0px 0px;
  overflow: hidden;
  background: #000000;
}

.item .head {
  text-align: center;
  font-size: 50px;
  height: 100px;
  background-color: #57655f;
  display: flex;
  align-items: center;
  justify-content: center;
}

.item .body {
  padding: 20px 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
}

.item .body h5 {
  font-weight: bold;
  margin: 0;
  padding-top: 7px;
  letter-spacing: 1px;
}
.item .body p {
  color: #65757e;
  line-height: 22px;
  margin: 0;
  overflow: hidden;
  text-align: center;
  max-height: 110px;
  transition: max-height 0.15s linear;
  max-width: 200px;
}
.item .body button {
  background: #1c2026;
  height: 35px;
  width: 35px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.25s ease-in-out;
}
.item .body button:hover {
  cursor: pointer;
  filter: brightness(120%);
}
.item .body button:active {
  transform: scale(0.9);
}
</style>