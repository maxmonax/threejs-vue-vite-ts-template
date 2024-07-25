<template>
  <div ref="sceneContainer" class="scene-container"></div>
</template>

<script lang="ts">
import { GameEngine } from '@/game/GameEngine';
import { defineComponent, onMounted, ref } from 'vue';

export default defineComponent({
  name: 'ThreeScene',
  setup() {
    const sceneContainer = ref<HTMLDivElement | null>(null);
    const game = ref<GameEngine | null>(null);

    onMounted(() => {
      if (sceneContainer.value) {
        game.value = new GameEngine({
          container: sceneContainer.value,
        });
      }
    });

    return {
      sceneContainer,
      game
    };
  }
});
</script>

<style scoped>

.scene-container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
}
</style>

<style scoped>
.scene-container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

</style>
