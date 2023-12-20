<template>
  <div class="flex items-center justify-center h-screen bg-blue-600">
    <div class="grid w-full gap-6 px-3 md:fled md:justify-center">
      <div class="text-3xl font-bold leading-7 text-white">
        Enter your password:
      </div>
      <input
        v-model="password"
        type="password"
        placeholder="Password"
        class="md:w-[400px] w-full h-9 rounded-md px-3"
      />

      <div
        @click="submitForm"
        :class="{ 'cursor-not-allowed opacity-50': !isValidPassword }"
        class="flex justify-end mt-12 text-base font-bold leading-6 text-white"
      >
        Submit
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
      return this.password === "Indha task pannalana mukkula ratham varum";
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
