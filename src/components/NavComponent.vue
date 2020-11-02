<template>
  <div>
    <input v-model="wide" />
    <button @click="changeType">Change type</button>
  </div>
</template>
<script>
export default {
  name: "NavComponent",
  computed: {
    wide() {
      return this.$store.state.nav.type;
    },
  },
  methods: {
    changeType() {
      this.$store.state.nav.type = "wide";
    },
  },
};
</script>
