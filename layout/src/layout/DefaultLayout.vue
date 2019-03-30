<template>
  <div id="default">
    <!-- ナビとかフッターのコンポーネントを追加したりする。 -->
    <div id="nav">
      <router-link to="/home">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/">Logout</router-link>
    </div>
    <router-view />
  </div>
</template>

<style scoped>
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
