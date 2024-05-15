<template>
  <router-view />
</template>

<script>

export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  padding:0;
  margin:0;
}

.logo {
  width: 150px;
}

.register input, .login input, .add input {               /* to use same styles in multiple files */
width: 300px;
height: 40px;
padding-left: 20px;
display: block;
margin-bottom: 30px;
margin-right: auto;
margin-left: auto;
border: 1px solid skyblue;
}

.register button, .login button, .add button {
width: 320px;
height: 40px;
border: 1px solid skyblue;
background: skyblue;
color: #fff;
cursor: pointer;
}

.center {
  margin-left: auto;
  margin-right: auto;
}

</style>

<!-- json-server --watch db.json     to run db server-->