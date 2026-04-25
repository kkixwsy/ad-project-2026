<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" sm="8" lg="6">
        <h1 class="text--secondary mb-3 mt-3">My ads</h1>
        
        <v-card v-for="ad in ads" :key="ad.id" class="mb-3" max-width="1000">
          <v-row>
            <v-col xs="4">
              <v-img :src="ad.src" height="175px" cover>
              </v-img>
            </v-col>

            <v-col xs="8">
              <h2 class="text--primary">{{ ad.title }}</h2>
              <p style="height: 85px; overflow: hidden; text-overflow: ellipsis;">{{ ad.desc }}</p>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" variant="text" :to="'/ad/' + ad.id">
                  Open
                </v-btn>
              </v-card-actions>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      ads: [
        {
          title: "iPhone 15 Pro",
          desc: "Новый iPhone 15 Pro в отличном состоянии. Гарантия 1 год.",
          promo: true,
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
          id: "1"
        },
        {
          title: "Samsung Galaxy S24",
          desc: "Флагманский смартфон Samsung. Отличная камера и производительность.",
          promo: false,
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
          id: "2"
        },
        {
          title: "MacBook Pro 16",
          desc: "Мощный ноутбук для работы и творчества. M2 Pro, 16GB RAM, 512GB SSD.",
          promo: true,
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
          id: "3"
        }
      ]
    }
  }
}
</script>