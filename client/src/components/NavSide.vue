<template>
  <!-- Sidebar/menu -->
  <nav
    class="w3-sidebar w3-red w3-collapse w3-top w3-large w3-padding"
    style="z-index: 3; width: 300px; font-weight: bold"
    id="mySidebar"
  >
    <br />
    <div class="w3-container" id="title">
      <h3 class="w3-padding-64">
        <b>Used<br />Aircraft</b>
      </h3>
    </div>
    <div class="w3-bar-block">
      <a
        href="#showcase"
        @click="toHome"
        class="w3-bar-item w3-button w3-hover-white"
        >Home</a
      >
      <a
        href="#showcase"
        onclick=""
        class="w3-bar-item w3-button w3-hover-white"
        >Showcase</a
      >
      <a
        href="#Stocks"
        @click="toHome"
        class="w3-bar-item w3-button w3-hover-white"
        >Stocks</a
      >
      <a
        href="#Information"
        @click="toHome"
        class="w3-bar-item w3-button w3-hover-white"
        >Information</a
      >
      <a
        href=""
        @click="toBanner"
        class="w3-bar-item w3-button w3-hover-white"
        >Banner</a
      >
      <a
        href="#contact"
        @click="logout"
        class="w3-bar-item w3-button w3-hover-white"
        >Logout</a
      >
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavSide',
  methods: {
    logout () {
      this.$store.dispatch('logout')
    },
    toBanner () {
      this.$store.dispatch('route', 'banner')
    },
    toHome () {
      this.$store.dispatch('route', 'home')
    }
  }
}
</script>

<style>
</style>
