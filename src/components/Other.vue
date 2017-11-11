<template>
  <div id="other">
    <h1>{{ show }}</h1>
    <button @click="toggleVisible()">Toggle Visible</button>
    <input v-model="text" placeholder="Text">
    <p>Text is: {{text}}</p>
    <button @click="submitText()">Submit Text</button>
  </div>
</template>

<script>
export default {
  name: 'Other',
  data: () => {
    return { show: false, text: '' }
  },
  methods: {
    toggleVisible: function() {
      this.show = !this.show
    },
    submitText: function() {
      console.log('text', this.text)
    }
  }
}
</script>
