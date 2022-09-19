<template>
  <div class="card">
      <a :href="anime.url" target="_blank">
          <img :src="anime.image_url" />
          <h3> {{anime.title}}</h3>
      </a>
  </div>
</template>

<script>
export default {
    props:['anime']
}
</script>

<style lang='scss' scoped>
.card{
     flex: 1 1 33%;
     width: 33%;
     max-width: 33%;
     padding: 0 8px;
     margin: 0 0 16px 0;

     img{
         width: 100%;
         height: 300px;
         object-fit: cover;
         border-radius: 14px;
         box-shadow: 0 4px 8px rgba($color: #000000, $alpha: 0.15);

         transition:0.4s;
     }

     h3{
         padding: 16px;
         color: #313131;
         transition: 0.5s;
     }

     &:hover{
         img{
             transform: scale(1.05);
         }

         h3{
             color: #24C444;
         }
     }
}
</style>
