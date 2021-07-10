<template>
  <div class="grid place-content-center w-screen h-screen bg-gray-300">
    <Content v-bind:data="messages" />
    <Form v-on:add="add" />
  </div>
</template>

<script>
import Content from './components/content';
import Form from './components/form';

export default {
  components: {
    Content,
    Form,
  },
  data: () => ({
    messages: [],
  }),
  methods: {
    add(message) {
      this.messages.push({
        content: message,
      });
    },
  },
};
</script>
