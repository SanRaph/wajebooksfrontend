<template>
  <div id="app">
    <Header />
    <AddBook v-on:add-book="addBook" />
    <Books v-bind:books="books" />
  </div>
</template>

<script>
import Header from "./components/layout/Header";
import Books from "./components/Books";
import AddBook from "./components/AddBook";

export default {
  name: "App",
  components: {
    Header,
    Books,
    AddBook,
  },
  data() {
    return {
      books: [
        {
          id: 1,
          name: "Fault in our stars",
          isbn: "7575757575",
          author: "Nadia",
        },
        {
          id: 1,
          name: "Angels and Demons",
          isbn: "75757576565",
          author: "Dan Brown",
        },
        {
          id: 1,
          name: "Hacking it",
          isbn: "75757575543",
          author: "Felicia Luman",
        },
        {
          id: 1,
          name: "Catch it",
          isbn: "7575757745",
          author: "Mercy John",
        },
      ],
    };
  },
  methods: {
    addBook(newBook) {
      this.books = [...this.books, newBook];
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Halvetical, sans-serif;
  line-height: 1.4;
}

.btn {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}


.btn:hover {
  background: #666;
}
</style>