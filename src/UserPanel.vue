<template>
    <div>
        Witaj {{ email }} !!!
      <a @click="leave()">Wyloguj</a>
    </div>
 </template>
 
 <script>
 export default {
  data() {
      return {
          email: this.email
      }
  },
  methods: {
    leave() {
          this.$emit('login', this.email);
      }
  }
  }
</script>