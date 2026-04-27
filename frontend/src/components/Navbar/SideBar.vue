<script setup>
import { Icon } from '@iconify/vue';
import { useDark, useToggle} from '@vueuse/core';
import { ref } from 'vue';
import { useRoute, useRouter } from 'vue-router'

const isDark = useDark()
const toogleDark = useToggle(isDark)

const route = useRoute()
const router = useRouter()

const handleNaviagate = (url) => {
    router.push(url)
}

</script>

<template>
    <div class="bg-white dark:bg-gray-950/60 w-1/5 h-screen top-0 left-0">
        <div class="flex flex-col justify-between h-full">
            <div class="w-full flex flex-col gap-5 pt-5 items-center">
                <h3 class="dark:text-white text-black text-2xl font-semibold flex">Social<p class="text-purple-500">Sphere</p>
                </h3>

                <div class="flex flex-col w-full pl-5 pr-5 gap-3">
                    <button @click="handleNaviagate('/')" class="flex items-center bg-gray-100/90 rounded w-full py-2 pl-3 gap-3 ">
                        <Icon icon="material-symbols:home-rounded" width="24" height="24" />
                        <h4>Home</h4>
                    </button>
                    <button @click="handleNaviagate('/notification')" class="flex items-center bg-gray-100/90 rounded w-full py-2 pl-3 gap-3 ">
                        <Icon icon="mdi:bell-outline" width="24" height="24" />
                        <h4>Notification</h4>
                    </button>
                    <button @click="handleNaviagate('/message')" class="flex items-center bg-gray-100/90 rounded w-full py-2 pl-3 gap-3 ">
                        <Icon icon="uiw:message" width="20" height="20" />
                        <h4>Message</h4>
                    </button>
                    <button @click="handleNaviagate('/profile')" class="flex items-center bg-gray-100/90 rounded w-full py-2 pl-3 gap-3 ">
                        <Icon icon="iconamoon:profile-fill" width="24" height="24" />
                        <h4>Profile</h4>
                    </button>
                    <button @click="handleNaviagate('/setting')" class="flex items-center bg-gray-100/90 rounded w-full py-2 pl-3 gap-3 ">
                        <Icon icon="weui:setting-filled" width="24" height="24" />
                        <h4>Setting</h4>
                    </button>
                </div>
            </div>

            <div class="pl-5 pr-5 w-full pb-5">
                <div class="flex items-center w-full pl-5 pr-5 justify-between bg-gray-300 rounded-lg py-2">
                    <div>
                        <Icon icon="tabler:sun" width="24" height="24" />
                    </div>
                    <button @click="toogleDark()" :class="isDark ? 'justify-end bg-gray-400': 'justify-start bg-yellow-500'" class="flex bg-gray-300 rounded-full w-1/2 h-5 relative transition-colors duration-300">
                        <div class="bg-white rounded-full w-1/2 h-5">
                        </div>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>