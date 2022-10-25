<script setup>
import {
    ref
} from "vue";

const link = ref([{
        name: 'About Us',
        href: "/about"
    },
    {
        name: 'News',
        href: "/news"
    },
    {
        name: 'Resources',
        href: "/resources"
    },
    {
        name: 'Events',
        href: "/events"
    },
    {
        name: 'Education',
        href: "/education"
    },
])
</script>

<template>
<header class="py-3">
    <div class="container">
        <div class="flex justify-between ">
            <div class="w-[100px]">
                <router-link to="/"><img src="../assets/img/Без названия.png" alt="logo"></router-link>
            </div>

            <div class="items-center flex " v-for="item, index in link" :key="index">
                <router-link class="hover:border-b-4 hover:border-red-600 ease-in-out hover:translate-x-2" :to="item.name">{{ item.name }}</router-link>
            </div>

            <div class="items-center flex ">
                <el-dropdown split-button type="primary">
                    
                    <template #dropdown>
                        <el-dropdown-menu>
                            <el-dropdown-item>Action 1</el-dropdown-item>
                            <el-dropdown-item>Action 2</el-dropdown-item>
                            <el-dropdown-item>Action 3</el-dropdown-item>
                        </el-dropdown-menu>
                    </template>
                </el-dropdown>

            </div>
        </div>

    </div>

</header>
</template>

<style scoped>

</style>
