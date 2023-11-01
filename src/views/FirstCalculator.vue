<template>
  <main>
    <h1>Kalkulator</h1>

    <input type="number" v-model.number="input1" placeholder="Masukkan Angka-1" />
    <input type="number" v-model.number="input2" placeholder="Masukkan Angka-2" />
    <br/>
    <input type="button" value="+" @click="tambah" />
    <input type="button" value="-" @click="kurang" />
    <input type="button" value="*" @click="kali" />
    <input type="button" value="/" @click="bagi" />
    <br/>
    <input v-model="result" placeholder="Hasil : " readonly />
  </main>
</template>

<script>
export default {
  data() {
    return {
      input1: '',
      input2: '',
      result: ''
    }
  },
  methods: {
    tambah() {
      this.result = this.input1 + this.input2
    },
    kurang() {
      this.result = this.input1 - this.input2
    },
    kali() {
      this.result = this.input1 * this.input2
    },
    bagi() {
      this.result = this.input1 / this.input2
    }
  }
}
</script>
