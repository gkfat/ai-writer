<template>
    <v-app>
        <v-main class="gradient-background pb-10">
            <v-app-bar
                elevation="0"
                class="bg-transparent"
            >
                <template #prepend>
                    <v-btn
                        flat
                        variant="plain"
                        to="/"
                        class="opacity-100"
                        size="x-large"
                    >
                        <template #prepend>
                            <v-img
                                src="/logo.png"
                                width="40"
                                height="40"
                                aspect-ratio="1/1"
                            />
                        </template>

                        <span class="text-h5 font-weight-bold text-white letter-spacing-1">
                            AI 作家
                        </span>
                    </v-btn>
                </template>
            </v-app-bar>
            
            <router-view />
        </v-main>
    </v-app>
</template>
<script lang="ts" setup>
</script>
<style lang="scss" scoped>
.gradient-background {
    background: linear-gradient(45deg, #232527, #4f5353);
}
</style>