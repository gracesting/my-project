<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="clickMe()">{{msgFromFather}}</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'msg from ComponentA',
    }
  },
  props: ['msgFromFather'],
  methods: {
    clickMe() {
      //console.log(this.msgFromFather)
      this.$emit('son-say-sth', this.msg)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
