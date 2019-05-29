<template>
  <div id="app">
    <form action="">
      <div>
        名前 <input type="text" name="name" v-model="form.name">
        お問いあわせないよう <input type="text" name="name" v-model="form.name">
        <div v-if="error.name">名前を入力して下さい。</div>
      </div>
      <input type="submit" value="送信" @click="submit">

    </form>
  </div>
</template>

<script>
  export default {
    data(){
      return {
        form: {
          name: ""
        },
        error: {
          name: false
        }
      }
    },
    methods: {
      submit(e) {
        this.error.name = true
        e.preventDefault()
      }
    }
  }
</script>

<style>
</style>