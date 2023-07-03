<script >
import CalcView from "./components/Calc.vue";

// !!!固定寫法!!
// 輸出
export default {

  // 如同 key:value (ex. CalcView:CalcView)，同名可省略(如下)
  components: {
    CalcView
  },

  // 方法，方法裡return物件 (物件用冒號)
  data() {
    return {
      name: "HRU"
    }
  },

}
</script>

<template>
  <!-- 下面那一行算是呼叫物件(帶入變數) -->
  <!-- {{ !不可在網頁隨意更改值! }} -->
  <h1>{{ name }}</h1>

  <!-- v-model 雙向綁定 (帶入對應變數) !可在網頁隨意更改值! -->
  <input type="text" v-model="name">

  <CalcView />
</template>

<style scoped></style>
