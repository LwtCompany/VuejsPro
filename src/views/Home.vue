<template>
  <div class="home">
  <h2>Assalomu alaykum</h2>
    <div class="myvideos">

        <template v-for="video of videos" :key="video.id">
          <div class="myvideo">
            <div class="up">

            <img :src="video.thumbnailUrl" alt="">
            </div>
            <div class="down">

            <h3>{{video.id}}</h3>
            <span>{{video.title}}</span>
              <router-link :to="{name: 'Video-watch', params:{id: video.id, name: 'HUnter'}}">Go To</router-link>
            </div>

          </div>
        </template>
    </div>
  </div>
</template>

<script>



export default {
  name: 'Home',
  components: {

  },
  data () {
    return {
      videos: this.$store.state.videos
    }
  }
}
</script>


<style lang="scss" scoped>
  .myvideos{

    width: 600px;
    margin: 0 auto;
    .myvideo{
         justify-items: center;
         justify-self: center;
      display: flex;
      border: 1px solid #eee;
      border-radius: 15px;
      margin: 10px;
      justify-content: right;
      img{
        width: 120px;
      }
      .down{
        margin: 5px;
       text-align: left;

      }
    }
  }
</style>
