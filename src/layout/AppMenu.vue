<script setup>
import { ref } from 'vue';

import AppMenuItem from './AppMenuItem.vue';

const model = ref([
    {
        label: 'Home',
        items: [{ label: 'DAHS', icon: 'pi pi-fw pi-home', to: '/' }]
    },
    {
        label: 'Practica',
        items: [
            // { label: 'Demo RFC', icon: 'pi pi-fw pi-id-card', to: '/uikit/formlayout' },
            //{ label: 'Demo Punto De Venta', icon: 'pi pi-fw pi-check-square', to: '/uikit/input' },
            { label: 'Demo API', icon: 'pi pi-fw pi-check-square', to: '/uikit/floatlabel' },
            { label: 'Demo UIChart', icon: 'pi pi-fw pi-check-square', to: '/uikit/charts' },
        ]
    }
]);
</script>

<template >
    <ul class="layout-menu">
        <template v-for="(item, i) in model" :key="item">
            <app-menu-item v-if="!item.separator" :item="item" :index="i"></app-menu-item>
            <li v-if="item.separator" class="menu-separator"></li>
        </template>
        <li>
            <!--
                            <a href="https://www.primefaces.org/primeblocks-vue/#/" target="_blank">
                                <img src="/layout/images/banner-primeblocks.png" alt="Prime Blocks" class="w-full mt-3" />
                            </a>
                        -->
        </li>
    </ul>
</template>

<style lang="scss" scoped></style>