
<template>
  <div class="subbreedbtn">
    <v-btn
      class="white--text"
      color="#264653"
      width="200px"
      @click="showSubbreeds = !showSubbreeds"
    >
      {{ nameOverallBreed }}
    </v-btn>
    <div v-if="showSubbreeds">
      <Breed
        v-for="(item, index) in subbreeds"
        :key="index"
        :subbreed="item"
        :breed="nameOverallBreed"
      />
    </div>
  </div>
</template>
<script>
import Breed from '../components/Breed'
export default {
    name: 'Subbreed',
    components: {
        Breed
    },
    props: {
        nameOverallBreed: {
            type: String,
            required: true
        },
        subbreeds: {
            type: Array,
            required: true
        }
    },
    data () {
        return {
            showSubbreeds: false
        }
    },
    methods: {
    }
}
</script>
<style scoped>

</style>
