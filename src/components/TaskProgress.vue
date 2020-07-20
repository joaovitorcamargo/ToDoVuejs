<template>
  <div class="tasks-progress">
    <span class="progress-value">{{progress}}%</span>
    <div class="progress-bar" :style="{width: progress + '%'}"></div>
  </div>
</template>

<script>
export default {
  props: {
    progress: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style>
.tasks-progress {
  position: relative;
  width: 80%;
  border: 1px solid white;
  color: white;
  border-radius: 8px;
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.progress-bar {
  position: absolute;
  border-radius: 8px;
  height: 100%;
  background-color: green;
  z-index: -1;
  align-self: flex-start;
}
.progress-value {
  font-size: 1.5rem;
}
</style>