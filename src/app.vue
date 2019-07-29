<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>
<style lang="scss">
// sass/scss用户请使用这段代码
$black: black;
$yellow: yellow;
h2 {
  color: $black;
  background: $yellow;
  transform: rotate(20deg);
}
</style>

<!--style lang="less">
// less用户请使用此代码
h2 {
  color: black;
  background: yellow;
  transform: rotate(20deg);
}
</style-->