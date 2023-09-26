<template>
    <div class="row mb-2">
        <div v-for="(article, i) in articles" :key="i" class="col-md-4">
            <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
                <div class="col-12 p-4 d-flex flex-column position-static">
                    <h4 class="mb-2">
                        <nuxt-link class="mb-1 text-decoration-none text-dark" :to="'detail/' + article.id">
                            {{ article.title }}
                        </nuxt-link>
                    </h4>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import {mapState} from 'vuex'
export default {
    computed: {
        ...mapState('articles', {
            articles: 'articles',
        })
    }
}
</script>