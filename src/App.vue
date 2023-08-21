<template>
  <div class="flex flex-col items-center justify-center mt-2">
    <!-- title -->
    <h1 class="font-bold text-[3rem]">BISc Calculator</h1>
    <div class="mt-2 flex flex-col justify-center items-center">
      <label for="penjumlahan" class="font-semibold text-[1.5rem]">sum</label>
      <div class="flex lg:flex-row flex-col lg:gap-x-2 items-center mt-1">
        <input
          type="number"
          placeholder="0"
          class="p-2 border-2 border-gray-300 rounded-md outline-none"
          v-model="count1"
        />
        <span class="font-bold text-[1.5rem]">+</span>
        <input
          type="number"
          placeholder="0"
          class="p-2 border-2 border-gray-300 rounded-md outline-none"
          v-model="count2"
        />
        <span class="font-bold text-[1.5rem]">=</span>
        <div class="p-2 border-2 border-gray-300 rounded-md w-[10rem]">
          {{ result }}
        </div>
        <button
          @click="sum()"
          class="cursor-pointer px-6 py-2 mt-2 lg:mt-0 bg-red-500 rounded-md text-white font-semibold"
        >
          +
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count1: null,
      count2: null,
      result: 0,
    };
  },
  methods: {
    sum() {
      this.result = parseInt(this.count1) + parseInt(this.count2);
    },
  },
};
</script>
