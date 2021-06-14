<template>
  <!-- template를 사용하면 렌더링이 되지 않는다, 최상위 template부분엔 사용하면 안된다-->
  <!-- <template v-if="isShow"> -->
    <button @click="handler">
      Click me!
    </button>
    <!-- <template v-if="isShow">
    <h1>Title</h1>
    <p>Paragraph1</p>
    <p>Paragraph2</p>
    </template> -->
  <!-- </template> -->
  
  <!-- v-show를 사용하면 true나 false에 상관없이 구조적으로 항상 렌더링을한다, 단 display:none으로 display속성만을 전환한다 -->
  <!-- v-if는 전환비용이 높기 때문에 상황에따라 사용한다. -->
  <h1 v-show="isShow">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script>