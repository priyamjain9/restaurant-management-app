<template>
<div class="nav">
<router-link to="/" href="#">Home</router-link>
<router-link to="/add" href="#">Add Restaurant</router-link>
<router-link to="/update" href="#">Update Restaurant</router-link>
<a v-on:click="logout" href="#">Logout</a>
</div>
</template>
<script>
export default {
name: 'HeaderPage',
methods:{
    logout(){
        localStorage.clear();
        this.$router.push({name:'Login'})
    }
}
}
</script>

<style>
.nav{
    background-color:#333;
    overflow:hidden;
}
.nav a {
    float: left;
    color: #f2f2f2f2;
    padding: 20px 26px;
    text-align: center;
    font-size: 17px;
    text-decoration: none ;
    margin-right: 5px;
}
.nav a:hover{
    background:#ddd;
    color:#333
}
</style>