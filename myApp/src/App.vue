
<template>
  <ion-app>
    <ion-router-outlet />
  </ion-app>
</template>

<script setup>
import { getAuth, signInWithEmailAndPassword } from "firebase/auth"
import { IonApp, IonRouterOutlet } from '@ionic/vue';

const auth = getAuth();
signInWithEmailAndPassword(auth, "ximety@nct.mx",
"ximety")
.then((userCredential) => {
// Signed in
const user = userCredential.user;
if(user== null)
{
console.log("no autenticado") }
else
{
console.log("usuario autenticado", user);
}
});



</script>
