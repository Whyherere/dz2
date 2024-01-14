<template>
  <div>
    <input type="text" v-model="Input">
    <button @click="Item">Добавить</button>
    <ul>
      <li v-for="item in List" :key="item">{{ item }}</li>
    </ul>
  </div>
  
<hr>

  <div>
    <input type="text" v-model="newItem">
    <button @click="aItem">Добавить</button>
    <ul>
      <li v-for="item in Listitems" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<script>


export default {
  data() {
    return {
      List: ["Элемент 1", "Элемент 2", "Элемент 3"], 
      Input: "" ,
      Listitems: [ "Элемент 1", "Элемент 2", "Элемент 3"],
      newItem: '',
    };
  },
  methods: {
    Item() {
      this.List.push(this.Input); 
      this.Input = ""; 
    },
    aItem() {
      this.Listitems.unshift(this.newItem);
      this.newItem = '';
    }
  }
}
</script>

<style>

</style>
