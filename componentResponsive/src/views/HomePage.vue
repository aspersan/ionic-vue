<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>SparkLine Component</ion-title>
      </ion-toolbar>
    </ion-header>


    <ion-content :fullscreen="true">
      <ion-grid>
        <ion-row class="ion-row-1">
          <ion-col size="6" size-lg="3">
            <div class="box">
              <spark-line
                title="CLICKS"
                value="1234"
                :chartOptions="sparkOptionsExample"
                :chartSeries="sparkSeriesExample"
                bgColor="gradient-blue"
                iconName="navigate-outline"
              />
            </div>
          </ion-col>
          <ion-col size="6" size-lg="3">
            <div class="box">
              <spark-line v-bind="sparkData2"/>
            </div>
          </ion-col>
          <ion-col size="6" size-lg="3">
            <div class="box">
              <spark-line v-bind="sparkData3"/>
            </div>
          </ion-col>
          <ion-col size="6" size-lg="3">
            <div class="box">
              <spark-line v-bind="sparkData4"/>
            </div>
          </ion-col>
        </ion-row>
        <ion-row class="ion-row-2">
          <ion-col size="6">
            <div class="box">
              <spark-line v-bind="sparkData1"/>
            </div>
          </ion-col>
        </ion-row>
        <ion-row class="ion-row-3">
          <ion-col size="12">
            <div class="box">
              <spark-line v-bind="sparkData1"/>
            </div>
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-content>
  </ion-page>
</template>


<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonGrid, IonRow, IonCol } from '@ionic/vue';


import { ref } from 'vue';
import SparkLine from '@/components/SparkLine.vue';


// 📊 Configuración del gráfico Sparkline
const sparkOptionsExample = ref({
  chart: {
    id: 'spark1',
    type: 'area',
    sparkline: { enabled: true },
    dropShadow: { enabled: true, top: 1, left: 1, blur: 2, opacity: 0.5 }
  },
  stroke: { curve: 'smooth', width: 3 },
  colors: ['#fff'],
 
  tooltip: {
    theme: 'dark',
    x: { show: false },
    y: { title: { formatter: () => '' } }
  },
 
});
const sparkSeriesExample = ref([{ data: [25, 66, 41, 59, 25, 44, 12, 36, 9, 21] }]);




const sparkData1 = ref({
  /* Propiedades del componente */
  title: "CLICKS",
  value: "1234",
  bgColor: "gradient-blue",
  textColor: "white",
  iconName: "navigate-outline",
  /* Propiedades del componentes interno de ApexChart */
  chartOptions: {
    chart: {
      id: 'clicks',
      type: 'area',
      sparkline: { enabled: true },
      dropShadow: { enabled: true, top: 1, left: 1, blur: 2, opacity: 0.5 }
    },
    stroke: { curve: 'smooth', width: 3 },
    colors: ['#fff'],
    tooltip: { theme: 'dark', x: { show: false }, y: { title: { formatter: () => '' } } }
  },
  chartSeries: [{ data: [25, 66, 41, 59, 25, 44, 12, 36, 9, 21] }],
});


const sparkData2 = ref({
  /* Propiedades del componente */
  title: "VIEWS",
  value: "1982",
  bgColor: "gradient-pink",
  textColor: "white",
  iconName: "eye-outline",
  /* Propiedades del componentes interno de ApexChart */
  chartOptions: {
    chart: {
      id: 'views',
      type: 'line',
      sparkline: { enabled: true },
      dropShadow: { enabled: true, top: 1, left: 1, blur: 2, opacity: 0.5 }
    },
    stroke: { curve: 'smooth', width: 3 },
    colors: ['#fff'],
    tooltip: { theme: 'dark', x: { show: false }, y: { title: { formatter: () => '' } } }
  },
  chartSeries: [{ data: [25, 66, 41, 59, 25, 44, 12, 36, 9, 21] }],
});


const sparkData3 = ref({
  /* Propiedades del componente */
  title: "LEADS",
  value: "2011",
  bgColor: "gradient-orange",
  textColor: "white",
  iconName: "people-outline",
  /* Propiedades del componentes interno de ApexChart */
  chartOptions: {
    chart: {
      id: 'leads',
      type: '',
      sparkline: { enabled: true },
      dropShadow: { enabled: true, top: 1, left: 1, blur: 2, opacity: 0.5 }
    },
    stroke: { curve: 'straight', width: 3 },
    colors: ['#fff'],
    tooltip: { theme: 'dark', x: { show: false }, y: { title: { formatter: () => '' } } }
  },
  chartSeries: [{ data: [25, 66, 41, 59, 25, 44, 12, 36, 9, 21] }],
});


const sparkData4 = ref({
  /* Propiedades del componente */
  title: "SALES",
  value: "627k€",
  bgColor: "gradient-green",
  textColor: "white",
  iconName: "cash-outline",
  /* Propiedades del componentes interno de ApexChart */
  chartOptions: {
    chart: {
      id: 'sales',
      type: 'area',
      sparkline: { enabled: true },
      dropShadow: { enabled: true, top: 1, left: 1, blur: 2, opacity: 0.5 }
    },
    stroke: { curve: 'smooth', width: 3 },
    colors: ['#fff'],
    tooltip: { theme: 'dark', x: { show: false }, y: { title: { formatter: () => '' } } }
  },
  chartSeries: [{ data: [25, 66, 41, 59, 25, 44, 12, 36, 9, 21] }],
});


</script>


<style scoped>


ion-row{
  overflow: hidden;
}


ion-col {
  max-height: 100%;
  --ion-grid-column-padding:10px;
}


/* El contenido real de cada columna */
.box {
  background: #1E1E1E;
  height: 100%;
  max-height: 100%;
  overflow: hidden;
  border-radius:5px;
  display: flex;
  justify-content: center;
  align-items: start;
}


/* Aplicar altura total y por filas, solo en pantallas ≥ lg=992 */
@media (min-width: 992px) {  
  ion-grid{height: 100%;}
  .ion-row-1{height: 20%; max-height: 20%;}
  .ion-row-2{height: 30%; max-height: 30%;}
  .ion-row-3{height: 50%; max-height: 50%;}
}


</style>
