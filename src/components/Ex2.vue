<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem: ""
            }
            
        },
        methods: {
            removeItem(index){
                this.items.splice(index, 1)
            },
            addItem(newitem){
                this.items.push(newitem)
            }

        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul id="cart"> 
        <li v-for="(item, idx) in items"> 
                {{ item }} <button @click="removeItem(idx)">Delete!</button>
        </li> 
    </ul>  
    <input v-model="newItem" placeholder="Candy">
    <button @click = "addItem(newItem)">Add!</button>
   
</template>
