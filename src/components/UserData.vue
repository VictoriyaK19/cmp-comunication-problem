<template>
  <div>
    <form @submit.prevent="submitData">
      <input type="text" placeholder="Your name" v-model="enteredName" />
      <input type="text" placeholder="Your age" v-model="enteredAge" />
      <button>Add User</button>
    </form>
  </div>
</template>

<script>
export default {
  emits: ["add-user"],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("add-user", this.enteredName, this.enteredAge);
    },
  },
};
</script>
