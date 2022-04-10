<template>
  <h1>My name is {{ name }}</h1>
  <p>My hobbies are: {{ hobbies.join(", ") }}</p>
  <input
    type="text"
    class="input"
    v-bind:class="error && 'input--error'"
    v-bind:value="textInput"
  />
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Kikks",
      hobbies: ["Codeing", "Reading", "Gaming"],
      textInput: "This is supposed to be the default text.",
      error: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.input {
  width: 20rem;
  padding: 1rem;
  border: #8beaa4 solid 0.1rem;
  border-radius: 0.5rem;
  font: inherit;
  transition: all 0.1s;
}

.input:focus {
  outline: #3bb75e solid 0.17rem;
  outline-offset: 0.1rem;
}

.input--error {
  border: #eb7b7b solid 0.1rem;
}

.input--error:focus {
  outline: #d34343 solid 0.17rem;
  outline-offset: 0.1rem;
}
</style>
