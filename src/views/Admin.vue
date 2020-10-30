<template>
  <div class="about">
    <button @click="Logout">Cerrar sesion</button>
  </div>
</template>

<script>
  import firebase from "firebase"

  export default {
    name: "Admin",
    created(){
      console.log(firebase.auth().currentUser)
    },
    methods:{
      Logout(){
        firebase.auth().signOut()
        .then(() => alert("Usuario Deslogueado"))
      }
    }
  }
</script>    
