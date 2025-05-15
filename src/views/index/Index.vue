<template>
    <v-container
        class="articles-container py-10"
    >
        <v-row
            v-if="articles?.length"
        >
            <v-col
                v-for="article in articles"
                :key="article._path"
                cols="12"
                sm="6"
                variant="outlined"
            >
                <ArticleCard :article="article" />
            </v-col>
        </v-row>
    </v-container>
</template>
<script lang="ts" setup>
import ArticleCard from './components/ArticleCard.vue';
import { useArticleSnapshots } from '@/composables/useArticleSnapshots';

const { articles } = useArticleSnapshots();
</script>
<style lang="scss" setup>
.articles-container {
    width: 95%;

    @media (min-width: 768px) {
        width: 70%;
    }
}
</style>
