<script setup>
import BreezeGuestLayout from '@/Layouts/Guest.vue';
import { Head, Link, useForm } from '@inertiajs/inertia-vue3';
import Layout from "@/Pages/Layout";

</script>

<template>
    <Layout>
        <Head title="Create Event" />

        <div>
            <Link
                :href="route('event.create')"
                class="cursor-pointer text-blue-500">Create Event</Link>
        </div>


    </Layout>
</template>
