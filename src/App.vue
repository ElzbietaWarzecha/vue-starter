<template>
  <div class="my-app">
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <!-- <div>Zaloguj się e-mailem -->
    <!-- <input type="email" v-model="email"> -->
    <!-- <h1>Twój e-mail to {{ email }}</h1> -->
    <!-- <input type="email" v-model="email"> -->
    <!-- <button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button> -->
    <!-- <button @click="logIn()">Wchodzę</button> -->
    <div v-if="loggedIn">
      Witaj {{ email }} !!!
      <a @click="logOut()">Wyloguj</a>
      </div>
    <div v-else>
      <div>Zaloguj się e-mailem
      <input type="email" v-model="email">
      <button @click="logIn()">Wchodzę</button>
    </div>
    </div>
  </div>
  
    <!-- <div v-if="!email.includes('@')">Niepoprawny adres e-mail!</div>
    <div v-else-if="email.length < 10">Ale masz krótki adres! Ma {{ email.length }} znaków</div>
<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz. Ma {{ email.length }} znaków</div>
<div v-else>Twój adres e-mail jest stanowczo za długi. Ma {{ email.length }} znaków</div> -->
</template>

<script>
import "milligram";
export default {
  data() {
  return {
    // email: 'ewarzecha@agh.edu.pl',
    email: '',
    password: '',
    loggedIn: false
  };
},
methods: {
  alertMyEmail() {
    alert(this.email);
  },
  logIn() {
    this.loggedIn=true;
  },
  logOut() {
    this.loggedIn=false;
  }
}
}
</script>

<style>
.my-app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>
