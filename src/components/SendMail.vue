<template>
    <div>
        <form @submit.prevent="sendmail" @reset="onReset">
            <div>
            <label>name</label>
            <input v-model="name" />
            </div>

            <div>
            <label>email</label>
            <input v-model="email" />
            </div>

            <div>
            <label>message</label>
            <textarea v-model="message"></textarea>
            </div>

            <button type="submit">submit</button>
            <button type="reset">reset</button>
        </form>
    </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: ""
    };
  },
  methods: {
    onReset() {
      this.name = "";
      this.email = "";
      this.message = "";
    },
    async sendmail(){
      console.log("Button Pushed...")
      // await fetch("/api/sendmail");
      await fetch(API + "/api/sendmail", {headers: HEADERS, method: "POST"});

    }
  },
}
</script>
