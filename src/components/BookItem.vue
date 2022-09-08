<template>
  <div class="book-item">
    <h3>{{ book.name }}</h3>
    <p>{{ book.isbn }}</p>
    <p>{{ book.author }}</p>
  </div>
</template>

<script>
export default {
  name: "BookItem",
  props: ["book"],
};
</script>

<style scoped>
.book-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
</style>