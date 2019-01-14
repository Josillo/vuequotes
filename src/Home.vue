<template>
  <div>
    <p>Server status {{ status }}</p>
    <button @click="changeStatus">ChangeStatus</button>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      status: "Critical"
    };
  },
  methods: {
    changeStatus: function() {
      this.status = "Normal";
    }
  }
};
</script>
