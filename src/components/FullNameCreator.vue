<template>
  <span>{{ firstName }} {{ lastName }}</span>
</template>

<script>
export default {
  props: {
    firstName: String,
    lastName: String,
  }
}
</script>

<style></style>