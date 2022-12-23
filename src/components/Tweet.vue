<template>
  <div class="tweet">
    <ProfileImage :img="user.image"/>

    <div class="body">
      <div class="top">
        <User :user="user" />
        <Timestamp :timestamp="timestamp" />
      </div>
      <div class="message">
        <Message :message="message" />
      </div>
      

      <div>
        <Actions />
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import Actions from "./Actions.vue"
import Message from "./Message.vue"
import ProfileImage from "./ProfileImage.vue"
import Timestamp from "./Timestamp.vue"
import User from "./User.vue"

export default {
  components: { 
    Actions,
    Message,
    ProfileImage,
    Timestamp,
    User
  },
  props: {
    user: Object,
    timestamp: String,
    message: String
  }
};
</script>

<style scoped>
</style>