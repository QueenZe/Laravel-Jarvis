<script setup>
import { Head } from "@inertiajs/vue3";
import AuthenticationCardLogo from "@/Components/AuthenticationCardLogo.vue";

defineProps({
    terms: String,
});
</script>

<template>
    <Head :title="lang().label.terms_of_service" />

    <div class="font-sans text-slate-900 dark:text-slate-100 antialiased">
        <div class="pt-4 bg-slate-100 dark:bg-slate-900">
            <div class="min-h-screen flex flex-col items-center pt-6 sm:pt-0">
                <div>
                    <AuthenticationCardLogo />
                </div>

                <div
                    class="w-full sm:max-w-2xl mt-6 p-6 bg-white dark:bg-slate-800 shadow-sm overflow-hidden sm:rounded-sm prose dark:prose-invert"
                    v-html="terms"
                />
            </div>
        </div>
    </div>
</template>
