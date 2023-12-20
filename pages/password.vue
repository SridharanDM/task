<template>
  <div
    class="flex items-center justify-center h-screen overflow-hidden bg-blue-600"
  >
    <div class="grid w-full gap-6 px-3 md:fled md:justify-center md:gap-8">
      <div class="text-3xl font-bold leading-7 text-white md:text-4xl">
        Enter your password:
      </div>
      <input
        v-model="password"
        type="password"
        placeholder="Inge oruthan irruken"
        class="md:w-[400px] w-full h-9 rounded-md px-3"
      />

      <div
        @click="submitForm"
        :class="{ 'cursor-not-allowed opacity-50': !isValidPassword }"
        class="flex justify-end mt-12 text-base font-bold leading-6 text-white md:mt-16 md:text-xl"
      >
        Aduthu >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: "",
    };
  },
  computed: {
    isValidPassword() {
      return this.password === "JEE BOOM BAA";
    },
  },
  methods: {
    submitForm() {
      if (this.isValidPassword) {
        this.$router.push("/samp");
      }
    },
  },
};
</script>
