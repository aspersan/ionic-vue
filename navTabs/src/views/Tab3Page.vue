<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 3 🥇 Principal</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <ion-button router-link="/tabs/tab3/secundaria">Tab 3 🥈 Secundaria (RL)</ion-button>
    </ion-content>
  </ion-page>
</template>


<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton } from '@ionic/vue';
</script>


<style>
  ion-content{ text-align: center; }
  ion-button{ margin-top:50px }
</style>