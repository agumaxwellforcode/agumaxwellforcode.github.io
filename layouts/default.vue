<template>
  <div>
    <Nuxt />
  </div>
</template>
<script>
export default {
  mounted() {
    const body = document.getElementsByTagName('body')[0]
    body.classList.add('font-sans')
    body.classList.add('antialiased')
    body.classList.add('text-gray-900')
    body.classList.add('leading-normal')
    body.classList.add('tracking-wider')
    body.classList.add('bg-cover')
    body.setAttribute(
      'style',
      "background-image: url('https://source.unsplash.com/1L71sPT5XKc')"
    )
    console.log(body)
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;1,100;1,200;1,300;1,400;1,500&display=swap');
html {
  font-family: 'Poppins', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  /* box-sizing: border-box; */
}
</style>
