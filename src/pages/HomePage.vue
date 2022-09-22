<template>
  <div class="home flex-grow-1 d-flex flex-column align-items-center justify-content-center">
    <img alt="Vue logo" @click="play" src="https://external-preview.redd.it/a5Bwlqmz2DLkXbHWyekuWnAEPa06zrugGYORGiiuvDA.jpg?width=960&crop=smart&auto=webp&s=bcf88bf04acf77801ea3e9055c1d0e96a9a77af5">
    <div class="home-card p-5 bg-white rounded elevation-3">
    
    </div>
  </div>
</template>

<script>
  import useSound from 'vue-use-sound';
  import buttonSfx from '../assets/Y2Mate.is - Tubby custard Injecting into the bowl full sound effect-TkDWv2PaYgM-128k-1660269860851.mp3';

export default {
  name: 'Home',
  setup(){
    const [play] = useSound(buttonSfx);
    return {play}
  }
}
</script>

<style scoped lang="scss">
.home{
  display: grid;
  height: 80vh;
  place-content: center;
  text-align: center;
  user-select: none;
  .home-card{
    width: 50vw;
    > img{
      height: 200px;
      max-width: 200px;
      width: 100%;
      object-fit: contain;
      object-position: center;
    }
  }
}
</style>
