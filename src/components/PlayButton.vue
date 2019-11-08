<template>
  <div>
    <el-button @click="modal1 = true" inlet="{prop.data}">&#9654;</el-button>
    <Modal v-model="modal1" title="Common Modal dialog box title" @on-ok="ok" @on-cancel="cancel">
      <p>Content of dialog</p>
      <p>Content of dialog</p>
      <p>Content of dialog</p>
    </Modal>
  </div>
</template>
<style scoped>
button {
  border: 2px solid black;
  border-radius: 50%;
  width: 2em;
  height: 2em;
  display: block;
}
button:active {
  background-color: #666;
}
button:hover {
  background-color: #ccc;
}
</style>
<script>
export default {
  data() {
    return {
      modal1: false
    };
  },
  methods: {
    ok() {
      this.$Message.info("Clicked ok");
    },
    cancel() {
      this.$Message.info("Clicked cancel");
    }
  }
};
</script>
