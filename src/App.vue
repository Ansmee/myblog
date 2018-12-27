<template>
  <div id="app">
    <el-container>
        <div class="container">
            <el-aside width="240px">
                <top-title></top-title>
            </el-aside>
            <el-main>
                <router-view/>
            </el-main>
        </div>
    </el-container>
  </div>
</template>

<script>
import TopTitle from './components/TopTitle'

import {Container, Aside, Main} from 'element-ui'

export default {
  name: 'App',
  components: {
      'TopTitle': TopTitle,
      [Container.name]: Container,
      [Aside.name]: Aside,
      [Main.name]: Main
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  border-top: solid 2px #222;
  margin: auto;
}

.container {
    width: 1000px;
    text-align: center;
    margin: auto;
}
</style>
