<template>
  <div class="h-screen bg-slate-200 flex items-center justify-center px-2">
    <div
      class="bg-gray-900 border border-slate-200 h-[400px] shadow-2xl w-[350px] rounded-tl-2xl rounded-tr-[100px] rounded-br-2xl rounded-bl-3xl"
    >
      <div class="mt-20 px-5">
        <div class="text-3xl font-bold leading-6 text-[#00DC82]">
          Hii, Sridharan
        </div>

        <div class="mt-10 text-xl font-bold leading-5 text-white">
          Here is your 2nd task
        </div>
        <div class="flex justify-center items-center mt-3 h-[200px]">
          <div
            class="flex px-5 py-2 bg-slate-700 rounded-lg border border-slate-700 cursor-pointer"
            @click="toggleBoxMove"
            :class="{ 'moved-box': isBoxMoved }"
          >
            <div
              class="text-[#E2E8F0] text-base font-semibold leading-5 hover:text-green-300"
            >
              Click to open
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isBoxMoved: false,
    };
  },
  methods: {
    toggleBoxMove() {
      this.isBoxMoved = !this.isBoxMoved;
    },
  },
};
</script>

<style scoped>
.moved-box {
  transform: translateY(-80px);
}
</style>
