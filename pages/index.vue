<template>
  <div class="container">
    <div class="link__block">
      <p class="top-title">生徒一覧</p>
      <NuxtLink to="/students">生徒の情報を見る</NuxtLink>
    </div>
    <div class="link__block">
      <p class="top-title">管理者</p>
      <NuxtLink to="/management">管理画面を見る</NuxtLink>
    </div>
  </div>
</template>

<style>
.container {
  font-family: sans-serif;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.link__block{
  margin:auto 20px;
}
.top-title{
  font: size 24px;
  font-weight: bold;
}

</style>
