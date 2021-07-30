<template>
  <ion-page>
    <ion-content>
      <div class="custom-scroll">
        <p v-for="i in 50" :key="i">{{ i }}</p>
      </div>

      <p v-for="i in 50" :key="i">{{ i }}</p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonPage
  },

  created() {
    document.addEventListener('scroll', e => {
      console.log(e.target); // Does nothing if ion-content scrolls
    }, true);
  }
});
</script>

<style scoped>
.custom-scroll {
  height: 50vh;
  overflow: auto;
}
</style>