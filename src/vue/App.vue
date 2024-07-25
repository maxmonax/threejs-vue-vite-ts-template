<template>
  <div class="app-container">
    <ThreeScene />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import ThreeScene from './components/ThreeScene.vue';

export default defineComponent({
  name: 'App',
  components: {
    ThreeScene
  }
});
</script>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>