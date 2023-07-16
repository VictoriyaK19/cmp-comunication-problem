<template>
  <active-user :username="user.name" :userage="user.age"></active-user>
  <user-data @add-user="addUser"></user-data>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: 'Viktoria',
        age: '19',
      }
    }
  },
  methods: {
    addUser(name, age) {
      this.user = {name: name,
      age : +age};
    }
  }
}
</script>

<style>
html {
  font-family: sans-serif;
}
div {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid#ccc;
  padding: 1rem;
}
</style>
