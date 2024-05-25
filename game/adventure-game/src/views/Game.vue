<template>
  <div class="game">
    <div class="image-display">
      <!-- placeholder for scene image -->
    </div>
    <div class="scene-description">
      <p>{{ description }}</p>
    </div>
    <div class="choices">
      <button
        v-for="(choice, index) in choices"
        :key="index"
        @click="makeChoice(choice)"
      >
        {{ choice.text }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Game",
  data() {
    return {
        description: 'You are in a dark forest. Paths lead in all directions.',
        choices: [
            { text: 'Go North', next: 'north' },
            { text: 'Go South', next: 'south' },
            { text: 'Go East', next: 'east' },
            { text: 'Go West', next: 'west'},
        ],
    };
  },
};
</script>

<style scoped>
    .game {
        color: white;
        background-color: midnightblue;
        text-align: center;
        padding: 20px;
    }
    .image-display {

    }
    .scene-description {
        margin-top: 20px;
    }
    .choices {
        margin-top: 20px;
    }
    .choices button {
        margin: 5px;
    }
</style>
