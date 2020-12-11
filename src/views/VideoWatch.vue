<template>
  <div class="video">
      <font color="green">
        <div class="image">
          <img :src="video.thumbnailUrl" alt="">
        </div>

          <div class="text">
             {{video.id}}
        <span>{{video.title}}</span>
          </div>
      </font>

      <span>{{this.$route.params.name}}</span>
  </div>
</template>

<script>
export default {
  computed: {
    video(){
      return this.$store.state.videos.find(vid => vid.id == this.$route.params.id);
    }
  }
}
</script>

