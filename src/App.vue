<template>
  <SendMail />
</template>

<script>
import SendMail from '@/components/SendMail.vue'
export default {
  name: "App",
  components: {
    SendMail
  }
  // data() {
  //   return {
  //     message: ""
  //   };
  // },
  // async mounted() {
  //   const { text } = await (await fetch("/api/message")).json();
  //   this.message = text;
  //   await (await fetch("/api/sendmail"));
  // }
};
</script>