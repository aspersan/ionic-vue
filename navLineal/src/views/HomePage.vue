<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Página 1</ion-title>
      </ion-toolbar>
    </ion-header>


    <ion-content :fullscreen="true">
      <div style="text-align: center;">
        <h2>Página 1</h2>
        <ion-button router-link="/">Go 1</ion-button>
        <ion-button router-link="/page2">Go 2</ion-button>
        <ion-button router-link="/page3">Go 3</ion-button>
      </div>
    </ion-content>
  </ion-page>
</template>


<script setup lang="ts">
import { IonBackButton, IonButtons, IonButton, IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
</script>


<style scoped>
</style>