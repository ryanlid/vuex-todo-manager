<template>
  <div>
    <select @change="filterTodos">
      <option value="200">200</option>
      <option value="2">2</option>
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="50">50</option>
      <option value="100">100</option>

    </select>
  </div>

</template>

<script>
  import { mapActions } from 'vuex';
  export default {
    name: "FilterTodos",
    methods: {
      ...mapActions(['filterTodos'])
    }
  }
</script>

<style scoped>
  .todos {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 1rem;
  }

  .todo {
    border: 1px solid #ccc;
    background: #41b883;
    padding: 1rem;
    border-radius: 5px;
    text-align: center;
    position: relative;
    cursor: pointer;
  }

  i {
    position: absolute;
    bottom: 10px;
    right: 10px;
    color: #fff;
    cursor: pointer;
  }

</style>
