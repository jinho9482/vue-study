<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <h4 :style="style">{{ products[0] }}</h4>
    <p>{{ price1 }} 만원</p>
    <!-- 데이터 바인딩 : 변경이 용이함, 실시간 자동 렌더링으로 값을 변경하면 그 즉시 웹사이트에 반영됨 -> 자주 변경될 애들을 이렇게 해놓으면 좋다. -->
  </div>
  <div>
    <h4 :style="style">{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4 :style="style">{{ products[2] }}</h4>
    <p>{{ price3 }} 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  // 데이터 보관함
  data() {
    return {
      price1: 50,
      price2: 70,
      price3: 90,
      style: "color: blue",
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  components: {},
};
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
</style>
