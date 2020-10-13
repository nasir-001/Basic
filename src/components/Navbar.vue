<template>

    <header class="px-4 py-3 bg-gray-900 sm:px-4 sm:items-center sm:py-3 sm:flex sm:justify-between">
        <div class="flex items-center px-4 py-3 sm:p-0 justify-between">
            <div>
                <img class="" src="/img/logo2.jpg" alt="Logo">
            </div>       
            <div class="sm:hidden">
                <button @click="isOpen = !isOpen" class="text-gray-500 block h-6 w-6 hover:text-white focus:outline-none focus:text-white" type="button">
                    <svg v-if="isOpen" class="h-6 w-6 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 352 512"><path d="M242.72 256l100.07-100.07c12.28-12.28 12.28-32.19 0-44.48l-22.24-22.24c-12.28-12.28-32.19-12.28-44.48 0L176 189.28 75.93 89.21c-12.28-12.28-32.19-12.28-44.48 0L9.21 111.45c-12.28 12.28-12.28 32.19 0 44.48L109.28 256 9.21 356.07c-12.28 12.28-12.28 32.19 0 44.48l22.24 22.24c12.28 12.28 32.2 12.28 44.48 0L176 322.72l100.07 100.07c12.28 12.28 32.2 12.28 44.48 0l22.24-22.24c12.28-12.28 12.28-32.19 0-44.48L242.72 256z"/></svg>
                    <svg v-else class="h-6 w-6 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M16 132h416c8.837 0 16-7.163 16-16V76c0-8.837-7.163-16-16-16H16C7.163 60 0 67.163 0 76v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16z"/></svg>
                </button>
            </div>
        </div>

        <div :class="isOpen ? 'block' : 'hidden'" class="sm:block">
            <div class="px-2 sm:p-0 pt-2 pb-2 sm:flex">
                <a class="block text-white font-semibold hover:bg-gray-800 py-1 px-2 mt-1 sm:ml-2 rounded" href="#">Trips</a>
                <a class="block text-white font-semibold hover:bg-gray-800 py-1 px-2 mt-1 sm:ml-2 rounded" href="#">Messages</a>
                <a class="block text-white font-semibold hover:bg-gray-800 py-1 px-2 mt-1 rounded" href="#">List your property</a>
            <AccountDropdown class="hidden sm:block sm:ml-6"/>
            </div>

            <div class="px-4 py-5 border-t border-gray-800 sm:hidden">
                <div class="flex items-center">
                    <img class="border-2 h-8 w-8 border-gray-600  rounded-full object-cover" src="../face1.jpg" alt="">
                    <span class="font-semibold ml-3 text-white">Nasir Lawal</span>
                </div>
                <div class="mt-4">
                    <a class="text-gray-400 block hover:text-white" href="">Account settings</a>
                    <a class="mt-2 text-gray-400 block hover:text-white" href="">Support</a>
                    <a class="mt-2 text-gray-400 block hover:text-white" href="">Sign out</a>
                </div>
            </div>        

        </div>

    </header>
</template>

<script>
import AccountDropdown from './AccountDropdown'

    export default {
        components: {
            AccountDropdown,
        },
        data() {
            return {
                isOpen: false,
            }
        },
    }
</script>
