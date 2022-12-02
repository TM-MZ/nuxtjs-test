<template>
  <div class="student_id">
    <h1>{{ getName() }}</h1>
    <div class="nav">
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink> |
      <NuxtLink to="/">トップページへ</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    return /^[a-zA-Z0-9]{16}/.test(params.id);
  },
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
  methods: {
    getName() {
      const item = this.students.find((elm) => {
        return elm.id == this.$route.params.id;
      });
      if (item) {
        return item.name;
      } else {
        return "該当の生徒は存在しません"      
      }
    },
  },
};
</script>

<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
  text-align: center;

  font-family: sans-serif;
}
</style>
