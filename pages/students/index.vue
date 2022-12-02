<template>
  <div class="students">
    <h1>生徒一覧</h1>
    <ul>
        <li v-for="student in students" :key="student.id">
            <NuxtLink :to="{path: '/students/' + student.id}">{{student.name}}</NuxtLink>
            </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
};
</script>

<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items:center;
  
  flex-flow: column;

  font-family: sans-serif;
}
</style>
