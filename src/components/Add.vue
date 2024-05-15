<template>
  <Header />
  <h2>Hello, welcome to add restro page</h2>
  <form class="add">
    <input type="text" name="name" placeholder="Enter Name" v-model="restaurant.name" />
    <input type="text" name="address" placeholder="Enter address" v-model="restaurant.address" />
    <input type="text" name="contact" placeholder="Enter contact" v-model="restaurant.contact" />
    <button v-on:click="addRestaurant" type="button">Add new Restaurant</button>
  </form>
</template>

<script>
import Header from "./Header.vue";
import axios from "axios"

export default {
  name: "AddPage",
  data() {
    return {
      restaurant: {
        name: "",
        address: "",
        contact: "",
      },
    };
  },
  methods: {
    async addRestaurant() {
      console.warn(this.restaurant);
      const result = await axios.post("http://localhost:3000/restaurant", {
        name:this.restaurant.name,
        address:this.restaurant.address,
        contact:this.restaurant.contact,
      });
      if(result.status==201){
        this.$router.push({ name: "Home" });
      }
      console.warn("result",result)
    }
  },
  components: {
    Header,
  },
  mounted() {
    let user = localStorage.getItem("user-info");
    if (!user) {
      this.$router.push({ name: "SignUp" });
    }
  },
};
</script>

<style scoped>
</style>