<template>
    <Tabs>
        <Tab title="First">First data</Tab>
        <Tab title="Second">Second data</Tab>
        <Tab title="Third">Third data</Tab>
    </Tabs>
</template>

<script>

import Tabs from "./components/Tabs";
import Tab from "./components/Tab";
export default {
    name: 'App',
    components: {Tabs, Tab},
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
