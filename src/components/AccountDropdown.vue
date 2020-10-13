<template>
    <div class="">
        <button @click="isOpen = !isOpen" class="relative z-10 block h-8 w-8 rounded-full overflow-hidden border-2 border-gray-600 focus:outline-none focus:border-white">
            <img class="h-full w-full object-cover" src="../face1.jpg" alt="">
        </button>
        <button v-if="isOpen" @click="isOpen = false" class="fixed inset-0 w-full h-full bg-black opacity-50"></button>
        <div v-if="isOpen" class="fixed right-0 w-48 mt-2 shadow-xl bg-white rounded-lg py-2">
            <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="">Account settings</a>
            <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="">Support</a>
            <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="">Sign out</a>
        </div>
        
    </div>
</template>
<script>
    export default {
       data() {
           return {
               isOpen: false,
           }
       },
       created() {
           const handleEscape = (e) => {
               if (e.key === 'Esc' || e.key === 'Escape') {
                   this.isOpen = false
               }
           }
           document.addEventListener('keydown', handleEscape)

           this.$once('hook:boforeDestroy', () => {
               document.removeEventListener('keydown', handleEscape)
           })
       }
    }
</script>
