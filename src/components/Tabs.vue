<template>
    <div>
        <div v-for="tabTitle in tabTitles" :key="tabTitle" @click="selectedTab = tabTitle">
            {{ tabTitle }}
        </div>
        <slot/>
    </div>
</template>

<script>
import Tab from "./Tab";
import { ref, provide } from 'vue'

export default {
    name: "Tabs",
    components: {Tab},
    setup(props, context) {
        const tabTitles = ref(context.slots.default().map(tab => tab.props.title))
        const selectedTab = ref(tabTitles.value[0])

        provide('selectedTab', selectedTab)

        return {selectedTab, tabTitles}
    }
}
</script>

<style scoped>

</style>
