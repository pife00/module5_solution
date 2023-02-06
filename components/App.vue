<template>
    <div>

    </div>
</template>

<script>
export default {
    name: "App",

    data() {
        return {
            message: 'Hello Vue!',
            catagory: '',
            dishes: [],
            categoryDishes: [],
            showCategory: false,
        }
    },
    mounted() {
        this.getData()
    },
    methods: {
        async getData() {
            const url = "https://coursera-jhu-default-rtdb.firebaseio.com/categories.json"
            const response = await fetch(url)
            const json = await response.json()
            this.dishes = await json
        },

        async categoryHandler(value) {
            this.categoryDishes = await data[value]

        }
    },
}


</script>

<style lang="scss" scoped>

</style>