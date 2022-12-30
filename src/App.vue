<template>
  <h1 @click="increase">
    {{ count }}
  </h1>
  <div v-if="count > 4">
    4보다 큽니다
  </div>
  <ul>
    <Fruit
      v-for="fruit in fruits"
      :key="fruit"
      :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<script>

import Fruit from '~/components/Fruit'

export default {
  components: {
    Fruit: Fruit // 속성의 이름과 데이터의 이름이 같으면 : 뒤쪽을 생략해도 정상작동한다.
  },
  data() {
    return {
      count: 0,
      fruits: ['apple', 'banna', 'orange', 'cherry']
    }
  },
  methods: {
    increase() {
      this.count += 1
    }
  },
}
</script>

<style lang="scss">
  h1{
    font-size: 40px;
    font-weight:900;
    color: royalblue;
  }
  ul{
    li{
      font-size: 40px;
    }
  }
</style>