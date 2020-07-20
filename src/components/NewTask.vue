<template>
  <div class="new-task">
    <input
      v-model="name"
      @keydown.enter="add"
      type="text"
      class="form-element"
      placeholder="Nova Tarefa ?"
    />
    <button class="form-element" @click="add">+</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ""
    };
  },
  methods: {
    add() {
      this.$emit("taskAdded", { name: this.name });
      this.name = "";
    }
  }
};
</script>

<style>
.new-task {
  margin: 35px;
}
.form-element {
  outline: none;
  font-size: 2rem;
  border: 1px solid white;
  padding: 5px 10px 8px;
  color: #fff;
}
input.form-element {
  width: 500px;
  background-color: #fff2;
  border-top-left-radius: 8px;
  border-bottom-left-radius: 8px;
}
button.form-element {
  border-left: none;
  background-color: #2196f3;
  border-top-right-radius: 8px;
  border-bottom-right-radius: 8px;
}
</style>