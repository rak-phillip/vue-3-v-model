<script lang="ts">
import { defineComponent } from 'vue';
import MessageInput from './MessageInput.vue';

export default defineComponent({
  components: {
    MessageInput
  },
  props: {
    msg: {
      type: Object,
      required: true,
    }
  }
});
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg.message }}</h1>

    <MessageInput v-model="msg" />
    
    <div>
      {{ JSON.stringify(msg) }}
    </div>
    
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
