<template>
    <p>Reaction Time : {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: [
        'score'
    ],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250) {
            this.rank = 'Light Speed'
        } else if(this.score < 400){
            this.rank = 'Pretty Fast'
        } else {
            this.rank = 'Slot...'
        }
    }
}
</script>
