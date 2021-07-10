<template>
  <div
    class="p-6 w-full max-w-sm mx-auto bg-white rounded-xl shadow-md divide-y divide-gray-400"
  >
    <div class="text-xl font-medium text-black p-1">
      <h1>Chat</h1>
    </div>
    <div class="overflow-y-auto max-h-52">
      <p class="text-gray-500 p-1 animate-pulse" v-if="!data.length">
        Send your message...
      </p>
      <p
        class="text-gray-500 p-1"
        v-for="(message, index) in data"
        v-bind:key="index"
      >
        {{ message.content }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['data'],
};
</script>
