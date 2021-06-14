<template>
  <div>
    <div
      class="
        max-w-4xl
        flex
        items-center
        h-auto
        lg:h-screen
        flex-wrap
        mx-auto
        my-32
        lg:my-0
      "
    >
      <intro-card data-aos="fade-up" />
      <intro-image data-aos="fade-left" />

      <!-- Pin to top right corner -->
      <div class="absolute top-0 right-0 h-12 w-18 p-4">
        <button
          class="js-change-theme focus:outline-none"
          @click="switchThemeMode()"
        >
          🌙
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggle: '',
      body: '',
      profile: '',
    }
  },
  mounted() {
    this.toggle = document.querySelector('.js-change-theme')
    this.body = document.getElementsByTagName('body')[0]

    setTimeout(() => {
      this.profile = document.getElementById('profile')
    }, 2000)
  },
  methods: {
    switchThemeMode() {
      if (this.body.classList.contains('text-gray-900')) {
        this.toggle.innerHTML = '☀️'
        this.body.classList.remove('text-gray-900')
        this.body.classList.add('text-gray-100')
        this.profile.classList.remove('bg-white')
        this.profile.classList.add('bg-gray-900')
      } else {
        this.toggle.innerHTML = '🌙'
        this.body.classList.remove('text-gray-100')
        this.body.classList.add('text-gray-900')
        this.profile.classList.remove('bg-gray-900')
        this.profile.classList.add('bg-white')
      }
    },
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;1,100;1,200;1,300;1,400;1,500&display=swap');
html,
body * {
  font-family: 'Poppins', sans-serif;
}
</style>
