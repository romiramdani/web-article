<template>
    <div class="mb-2">
        <div v-for="article in articles" :key="article.id" class="col-md-4" >
            <div v-if="article.id == paramId" class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative" >
                <div class="col-12 d-none d-lg-block">
                    <img :src="article.img" alt="#" class="img-thumbnail">
                </div>
                <div class="col-12 p-4 d-flex flex-column position-static">
                    <h4 class="mb-2">{{ article.title }}</h4>
                    <p class="card-text mb-auto">{{ article.content }}</p>
                </div>
            </div>
        </div>
        <div class="action mt-4 mx-4">
            <div class="btn btn-outline-secondary btn-sm mb-3" @click="$router.go(-1)">Kembali</div>
        </div>
    </div>
</template>
<script>
import {mapState} from 'vuex'
export default {
    data() {
        return {
            paramId: this.$route.params.id,
        }
    },
    computed: {
        ...mapState('articles', {
            articles: 'articles',
        })
    }
}
</script>