<template>
  <div class="container">
    <section>
      <h1>HeadTextコンポーネント</h1>
      <HeadText text="ここはh1で指定" level="1" />
      <HeadText text="ここはh2で指定" level="2" />
      <HeadText text="ここはh3で指定" level="3" />
      <HeadText text="ここはh4で指定" level="4" />
      <HeadText text="ここはh5で指定" level="5" />
      <HeadText text="ここは指定なし" />
    </section>
  </div>
</template>

<script>
import HeadText from '../components/HeadText.vue';

export default {
  components: {
    HeadText
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
