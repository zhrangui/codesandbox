<template>
  <div>
    <input v-model="wide" />
    <input v-model="wide" />
    <button @click="changeType">Change type</button>
  </div>
</template>
<script>
export default {
  name: "NavComponent",
  computed: {
    wide: {
      get() {
        return this.$store.state.nav.type;
      },
      set(value) {
        this.$store.state.nav.type = value;
      },
    },
  },
  methods: {
    changeType() {
      this.$store.state.nav.type = "wide";
    },
  },
};
</script>
