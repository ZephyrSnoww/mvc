<script setup>
import { reactive } from 'vue';

let state = reactive({
  modsList: [],
  search: ''
});

let localModsList = localStorage.getItem('modsList');

if (localModsList) {
  state.modsList = JSON.parse(localModsList);
}

function search() {
  alert(state.search);
}
</script>

<template>
  <input v-model="state.search" type="text" />
  <div @click="search">Submit</div>
</template>

<style scoped>

</style>
