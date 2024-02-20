<script setup lang="ts">
import VButton from './components/VButton.vue';
import VCard from './components/VCard.vue';
import VAdditional from './components/VAdditional.vue';
import { ref } from 'vue';

const btnHandler = () => {
  alert("Btn is clicked");
}

const cardText = ref<string>("Card text from prop variable");

</script>

<template>
  <div>
    <VButton @click="btnHandler">
      Some text
      <VAdditional>5 free spins</VAdditional>
    </VButton> <!--- Button component with additional content -->
    <VButton @click="btnHandler" outline>Some text</VButton> <!--- Button component with outline -->
    <VButton @click="btnHandler">Some text</VButton> <!--- Default Button component -->
    <VCard /> <!--- Default Card component -->
    <VCard text="Card text from prop" /> <!--- Card component with text prop -->
    <VCard :text="cardText" /> <!--- Card component with ref text prop -->
  </div>
</template>

<style>
</style>
