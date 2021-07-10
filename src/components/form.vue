<template>
  <div>
    <form class="mt-6">
      <input
        class="p-2 bg-white rounded-xl shadow-md border border-transparent focus:outline-none focus:ring-2 focus:ring-gray-600 focus:border-transparent"
        v-model="message"
      />
      <button
        class="p-2 ml-2 bg-white text-white rounded-xl shadow-md bg-gray-600 hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-600 focus:ring-opacity-50 font-medium"
        v-bind:disabled="!message"
        v-on:click.prevent="add"
      >
        Send
      </button>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    message: '',
  }),
  methods: {
    add() {
      this.$emit('add', this.message);
      this.message = '';
    },
  },
};
</script>
