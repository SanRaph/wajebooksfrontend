<template>
 <div>
    <form @submit="addBook">
        <input type="text" v-model="name" name="title" placeholder="Add Book">
        <input type="submit" value="Submit" class="btn"> 
    </form>
 </div>
</template>

<script>
import uuid from 'uuid';
export default {
    name: "myAddBook",
    data() {
        return {
            name: ''
        }
    },
    methods: {
        addBook(e){
            e.preventDefault();
            const newBook = {
                id: uuid.v4(),
                name: this.name
            }
            //send to parent
            this.$emit('add-book', newBook);
            this.title = '';
        }
    }
}
</script>

<style>
 form {
    display: flex;
 }

 input[type="text"] {
    flex: 10;
    padding: 5px;
 }

 input[type="submit"] {
    flex: 2;
 }
</style>