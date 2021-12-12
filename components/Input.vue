<template>
  <div>
    input
    <input
      :value="startInput"
      @input="$emit('startInput', $event.target.value)"
    />
    <input
      v-bind:value="endInput"
      v-on:input="onInput"
    />
    {{ startInput }}
    {{ endInput }}
  </div>
</template>
<script>
export default {
  props: ["startInput", "endInput"],
  data() {
    return {};
  },
  mounted() {
    console.log(this.$props);
  },
  methods: {
    onInput(event) {
      // update value of input and if they have , or - remove them
      const newValue = event.target.value.replace(/,/g, "").replace(/-/g, "");
      this.$emit("endInput	", newValue);
    },
  },
};
</script>
