<template>
    <section>
        <ul>
            <li v-for="todoItems in todoItems">{{ todoItems }}</li>
            
        </ul>
    </section>
</template>

<script>
export default {
    data(){
        return{
            todoItems: []
        }
    },
    created(){
        if(localStorage.length > 0){
            for(var i = 0; i < localStorage; i++){
                this.todoItems.push(localStorage.key(i))
            }
        }
    },

}
</script>

<style>
</style>