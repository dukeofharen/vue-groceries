<template>
  <div class="about">
    <h1>Groceries</h1>
    <input v-model="groceryInput" type="text" />
    <button v-on:click="addGrocery">Add grocery</button>
    <ul>
        <li v-for="grocery in groceries">{{grocery}}</li>
    </ul>
  </div>
</template>
<script>
export default {
    name: 'groceryList',
    data () {
        return {
            groceries: ["Ham", "Kaas", "Eieren"],
            groceryInput: ""
        }
    },
    methods: {
        addGrocery () {
            this.groceries.push(this.groceryInput);
            this.groceryInput = "";
        }
    }
}
</script>
<!-- Scoped is used when you only want to apply these styles to this specific component. -->
<style scoped>
li {
    color: red;
}
</style>