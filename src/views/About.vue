<template>
  <div>
    <h1>About</h1>
    <h3>Hi {{ name }}!</h3>
    <h4>{{ student.name }}</h4>
    <h4>{{ student.school }}</h4>
    <p>Here is the about page</p>
    <button @click="changeName">Change Name</button>
    <!-- <button @click="changeStudent">Change Student</button> -->
    <router-link to="/">Home</router-link>
  </div>
</template>

<script setup>
import { ref, reactive } from "@vue/reactivity";
const name = ref("Vlad");

const student = reactive({
  name: "Vlad",
  school: "AltSchool",
});

const changeName = () => {
  name.value = "Abiodun Vlad";
};

// const changeStudent = () => {
//   student.value = { name: "Titi", school: "OAU" };
// };
</script>
