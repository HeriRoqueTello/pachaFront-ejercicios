<script setup>
import { storeToRefs } from 'pinia';

import { useAuthStore } from '@/stores';

const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>

<template>
    <div v-if="user">
        <h1>Bienvenido {{user.firstName}}!</h1>
        <p>Pagina principal</p>
        <p><router-link to="/users">Manage Users</router-link></p>
    </div>
</template>
