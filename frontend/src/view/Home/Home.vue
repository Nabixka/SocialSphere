<script setup>
import Navbar from '../../components/Navbar/Navbar.vue';
import SideBar from '../../components/Navbar/SideBar.vue';

</script>

<template>
    <div class="dark:bg-gray-800 bg-gray-200 min-h-screen">
        <div class="flex flex-col lg:flex-row">

            <!-- Sidebar -->
            <SideBar class="hidden lg:block" />
            <Navbar  class="block lg:hidden"/>

            <!-- CRUD -->
            <div class="pl-2 pr-2 pt-2 lg:pl-5 w-full">
                <div class="bg-white rounded-md flex w-full pl-5 py-3">
                    <input class="pl-5 bg-gray-200 lg:w-2/3 rounded-2xl py-2 " type="text" placeholder="Search People, Posts, Communities">
                    <div class="flex justify-end w-full">
                        <h3 class="">Test</h3>
                    </div>
                </div>

                <div class="grid grid-cols-3 gap-2 w-full">
                    <div class="col-span-2 mt-5">
                        <div class="bg-white flex rounded-lg pl-5 py-2">
                            <div class="bg-gray-200 overflow-hidden rounded-full">
                                <img class="w-15 h-15 image-center" src="/src/assets/vue.svg">
                            </div>
                            <h3>What</h3>
                        </div>
                    </div>

                    <div class="bg-white rounded-lg mt-5">
                        <h3>Hai</h3>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>