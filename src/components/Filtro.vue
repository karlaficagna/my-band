<template>
  <div class="filtro">
    <ul>
      <li v-for="item in items" :key="item">
        {{ item }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "Filtro",
  data: function () {
    return {
      items: ["Brasil", "Argentina", "Paraguai", "Uruguai"],
    }
  },
  computed: {
    itemsFiltered: function () {
      return this.items.filter((itemArray) => {
       return itemArray.indexOf(this.searchItem) > -1;
      });
    },
  },
};
</script>
<style>
.filtro {
  padding: 30px;
}
</style>

  
