<template>
    <div>
      <h2>By Iqbal</h2>
      <div class="avatar">
      <input v-model="inputText" type="text" placeholder="Ketik Nama Anda...">
      <br>
      <button @click="generateAvatar">Buat Profile Picture!</button>
      <br>
      <img v-if="avatarUrl" :src="avatarUrl" alt="Avatar">
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        inputText: '',
        avatarUrl: ''
      }
    },
    methods: {
      generateAvatar() {
        const baseUrl = 'https://robohash.org/'
        const input = this.inputText.trim() || 'default'
        const size = '200x200'
        const format = 'png'
        this.avatarUrl = `${baseUrl}${input}.${format}?size=${size}`
      }
    }
  }
  </script>
  
  <style scoped>
  h1 {
    margin-bottom: 20px;
  }
  input {
    margin:auto;
    width: 30%;
    height: 30px;
  }
  button {
    margin: auto;
    width: 20%;
    height: 40px;
    background-color: rgb(0, 188, 66);
    cursor: pointer;
  }
  button:hover {
    border: 1px solid rgb(133, 255, 137);
  }
  .avatar img {
    margin-top: 20px;
    max-width: 20%;
    margin: auto;
  }
  .avatar {
    display: flex;
    flex-direction: column;

  }
  </style>