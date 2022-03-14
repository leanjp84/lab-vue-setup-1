<template>
  <div id="app">
    <h1>My Component</h1>

    <NewComponent></NewComponent>

    <p>Aqui abajo se va a mostrar mi texto en javascript:</p>
    <p class="bold">{{ text }}</p>
    <br />
    <button @click="helloWorld">click me</button><br />
    <router-link to="AboutUs"> About Us </router-link>
    <router-view />
  </div>
</template>

<script>
import NewComponent from "./components/NewComponent.vue";
export default {
  name: "app",
  components: {
    NewComponent,
  },
  data() {
    return {
      text: "Hola texto javascript",
    };
  },
  methods: {
    helloWorld() {
      console.log("Hello World");
    },
  },
};
</script>

<style>
.bold {
  font-style: oblique;
  color: rgb(50, 105, 87);
}
p {
  font-family: sans-serif;
  font-size: 20px;
  color: blueviolet;
}
h1 {
  font-family: sans-serif;
  color: dimgray;
}

label {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  color: rgb(249, 249, 249);
  padding: 15px;
}
button {
  padding: 10px;
  background-color: blue;
  color: white;
  margin: 20px;
}
</style>
