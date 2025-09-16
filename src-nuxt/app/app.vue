<script setup lang="ts">
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/core";

const greetMsg = ref("");
const name = ref("");

async function greet() {
  // Learn more about Tauri commands at https://tauri.app/develop/calling-rust/
  greetMsg.value = await invoke("greet", { name: name.value });
}
</script>

<template>
  <UApp>
    <form class="row" @submit.prevent="greet">
      <UInput
        id="greet-input"
        v-model="name"
        placeholder="Enter a name..."
        :label="`Name`"
        :label-for="`greet-input`"
        :label-style="{ color: 'blue' }"
        :label-class="`greet-label`"
        :label-size="`lg`"
        :label-position="`top`"
        :label-width="`100px`"
        :label-align="`left`"
        :label-required="true"
        :label-required-text="`*`" />
      <!-- <input id="greet-input" v-model="name" placeholder="Enter a name..." /> -->
      <UButton type="submit">Greet</UButton>
    </form>
    <p>{{ greetMsg }}</p>
  </UApp>
</template>

<style scoped>
</style>