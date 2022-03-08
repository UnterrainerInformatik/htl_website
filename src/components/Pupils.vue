<template>
  <v-container>
    <h2>
      Pupils
    </h2>
    <div class="">
      <v-card class="ma-2" v-for="(pupil, i) in pupils" :key="i">
        <v-card-title>{{pupil.name}}</v-card-title>
        <v-card-text>{{pupil.text}}</v-card-text>
      </v-card>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'Pupils',

  props: {
    pupils: {}
  },

  components: {
  },

  data: () => ({
  }),

  computed: {
  },

  watch: {
  },

  methods: {
  },

  mounted () {
  }
}
</script>

<style lang="scss">

</style>
