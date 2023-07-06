<template>
  <base-layout page-title="All Memories">
    <ion-list>
      <ion-item
        v-for="memory in memories"
        :key="memory.id"
        :router-link="`/memories/${memory.id}`"
      >
        <ion-thumbnail slot="start">
          <ion-img :src="memory.image"></ion-img>
        </ion-thumbnail>
        <ion-label>
          {{ memory.title }}
        </ion-label>
      </ion-item>
    </ion-list>
  </base-layout>
</template>

<script>
import { IonList, IonItem, IonImg, IonThumbnail, IonLabel } from "@ionic/vue";

export default {
  components: {
    IonList,
    IonItem,
    IonImg,
    IonThumbnail,
    IonLabel,
  },
  data() {
    return {
      memories: [
        {
          id: "m1",
          title: "A trip to the mountains",
          description: "It was a realy nice trip!",
          image:
            "https://hips.hearstapps.com/hmg-prod/images/alpe-di-siusi-sunrise-with-sassolungo-or-langkofel-royalty-free-image-1623254127.jpg",
        },
        {
          id: "m2",
          title: "Surfing the sea side",
          description: "Feeling the breeze!",
          image:
            "https://images.pexels.com/photos/96377/pexels-photo-96377.jpeg?cs=srgb&dl=pexels-francesco-ungaro-96377.jpg&fm=jpg",
        },
        {
          id: "m3",
          title: "Good eating",
          description: "It was tasty!",
          image:
            "https://cdn.who.int/media/images/default-source/imported/behealthy/nutrition.tmb-768v.jpg?sfvrsn=6d120e2b_9",
        },
      ],
    };
  },
};
</script>