<template>
    <div v-show="title === selectedTab">
        <slot/>
    </div>
</template>

<script>
import { inject } from "vue";

export default {
    name: "Tab",
    props: {title: String},
    setup() {
        const selectedTab = inject('selectedTab')

        return {selectedTab}
    }
}
</script>

<style scoped>

</style>
