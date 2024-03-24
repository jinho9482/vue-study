<template>
  <div class="menu">
    <!-- 반복문을 쓸 때 항상 key를 써줘야 함, a tag간 구분을 하기 위함  -->
    <a v-for="(name, id) in menu" :key="id" href=""> {{ name }} </a>
  </div>

  <div>
    <h4 :style="style">{{ products[0] }}</h4>
    <p>{{ price1 }} 만원</p>
    <!-- 데이터 바인딩 : 변경이 용이함, 실시간 자동 렌더링으로 값을 변경하면 그 즉시 웹사이트에 반영됨 -> 자주 변경될 애들을 이렇게 해놓으면 좋다. -->
    <button @click="claim[0]++">허위 매물 신고</button>
    <span>신고 수 : {{ claim[0] }} </span>
  </div>

  <div>
    <h4 :style="style">{{ products[1] }}</h4>
    <p>{{ price2 }} 만원</p>
    <button @click="claim[1]++">허위 매물 신고</button>
    <span>신고 수 : {{ claim[1] }} </span>
  </div>

  <div>
    <h4 :style="style">{{ products[2] }}</h4>
    <p>{{ price3 }} 만원</p>
    <button @click="claim[2]++">허위 매물 신고</button>
    <span>신고 수 : {{ claim[2] }} </span>
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
      menu: ["Home", "Shop", "About"],
      claim: [0, 0, 0],
    };
  },

  // methods: {
  //   increase() {
  //     this.claim++;
  //   },
  // },

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
}

.menu {
  background-color: rgb(2, 2, 2);
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
