<template>
  <section class="contact p-5 my-5 text-center">
    <h3>CONTACT US</h3>
    <p
      class="w-75 my-5 mx-auto"
    >Have a property that you can be proud of. A property that is not only beautiful, but can also endure the test of time. With over 25 years of experience, our team will work with you to design and build your dream property.</p>

    <form class="row justify-content-center" action="send" method="POST">
      <input
        v-model="user_data.name"
        class="col-md-8 col-12 m-3"
        type="text"
        required
        name="name"
        placeholder="Name"
      />
      <input
        v-model="user_data.tel"
        class="col-md-8 col-12 m-3"
        type="tel"
        name="tel"
        placeholder="Phone Number ( optional )"
      />
      <input
        v-model="user_data.email"
        class="col-md-8 col-12 m-3"
        type="email"
        required
        name="email"
        placeholder="E-mail"
      />
      <textarea
        v-model="user_data.message"
        required
        class="col-md-8 col-12 m-3"
        style="resize: none;"
        name="message"
        placeholder="Message..."
      ></textarea>
      <ul class="col-12" v-if="errors.length">
        <li v-for="error in errors" :key="error">{{error}}</li>
      </ul>
      <p class="col-12" v-else>{{isSent}}</p>
      <button @click.prevent="onSubmit" class="mt-5 col- 6 col-md-4 submit">Send</button>
    </form>
  </section>
</template>


<script>
export default {
  name: "Form",
  data() {
    return {
      user_data: {
        name: "",
        email: "",
        tel: "",
        message: ""
      },
      errors: [],
      isSent: ""
    };
  },

  methods: {
    onSubmit() {
      this.errors = [];
      if (!this.user_data.name) {
        this.errors.push("Please fill out your name");
      }
      if (!this.user_data.email) {
        this.errors.push("Please fill out your email");
      }
      if (!this.user_data.message) {
        this.errors.push("Please fill out your message");
      }

      this.isSent = "Thank you for contacting us";

      (this.user_data.name = ""),
        (this.user_data.tel = ""),
        (this.user_data.email = ""),
        (this.user_data.message = "");
    }
  }
};
</script>



<style>
.contact h3 {
  font-size: 50px;
  font-weight: 700;
  color: #464646;
}

.contact p {
  color: #464646;
}

input,
textarea {
  height: 50px;
  border: none;
  background: #d8d8d8;
  color: white;
}

textarea {
  height: 200px;
}

form button {
  border: 1px solid #44ad96;
  border-radius: 0px;
  background: none;
  padding: 10px 40px;
  color: #44ad96;
}

form button:hover {
  background: #44ad96;
  color: white;
}

li {
  list-style-type: none;
}
</style>