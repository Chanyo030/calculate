<script>
export default {
    data() {
        return {
            // 物件 - 宣告變數
            num1: null,
            num2: null,
            sum: null
        }
    },
    methods: {
        calcSum() {
            // 指向data方法裡的參數
            // console.log("這是num1");
            // console.log(this.num1);

            // !用this才有辦法取上面的值!
            this.sum = this.num1 + this.num2;
        }
    }
}
</script>

<template>
    <div>
        計算機
    </div>
    <input type="number" v-model="num1">
    <p>+</p>
    <input type="number" v-model="num2">

    <!-- v-on:click 綁定按鈕 - 觸發事件 -->
    <button type="button" v-on:click="calcSum">計算</button>
    <h3>= {{ sum }}</h3>
</template>

<style></style>