<template>
  <div>
    <div v-if="!profile">Need to authorize via <a href="/login">Google</a></div>
    <div v-else>
      <div>{{ profile.name }}&nbsp;<a href="/logout">Log Out</a></div>
      <div>&nbsp;</div>
      <messages-list :messages="messages"/>
    </div>
  </div>
</template>

<script>
  import MessagesList from "components/messages/MessageList.vue";

  export default {
    components: {
      MessagesList
    },
    data() {
      return {
        messages: frontendData.messages,
        profile: frontendData.profile
      }
    }
  }
</script>

<style>

</style>