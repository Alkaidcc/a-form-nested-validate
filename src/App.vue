<script setup lang="ts">
import { ref } from 'vue';

const info = ref({
  name: '',
  person: {
    sex: ''
  }
})
</script>

<template>
  <a-form :model="info">
    <a-form-item name="name" :rules="[{required: true,message: 'name required',trigger: 'blur'}]">
      <a-input v-model:value="info.name"></a-input>
    </a-form-item>
    <a-form-item name="person.sex" :rules="[{required: true,message: 'sex required',trigger: 'blur'}]">
      <a-input v-model:value="info.person.sex"/>
    </a-form-item>
  </a-form>
</template>

