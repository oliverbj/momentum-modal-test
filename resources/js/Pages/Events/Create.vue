<script setup>
import Modal from "@/Components/Modal.vue";
import {useForm} from "@inertiajs/inertia-vue3";
import TextInput from "@/Components/Input";
import Button from "@/Components/Button";
const form = useForm({
    name: null,
});

const submit = () => {
    form.post(route('event.store'));
};

</script>

<template>
    <Modal>
        <form class="mt-6" @submit.prevent="submit">
            <div class="grid grid-cols-2 gap-x-6 gap-y-8">
                <text-input v-model="form.name" :error="form.errors.name" label="Event Name" />
            </div>
            <div class="mt-6 flex justify-between">
                <Button :loading="form.processing" class="btn-indigo ml-auto" type="submit">Create Event</Button>
            </div>
        </form>
    </Modal>
</template>
