<template>
    <v-app-bar :elevation="1" app color="secondary" dark>
        <v-toolbar-title>
            <v-icon icon="mdi-video"/> After Effects Render
        </v-toolbar-title>
        <template v-slot:append>
            <v-btn :icon="!showConfig ? 'mdi-cog': 'mdi-window-close'" @click="toggleConfig"></v-btn>
        </template>
    </v-app-bar>
</template>

<script>
export default {
    props: ['toggleConfig', 'showConfig'],
}
</script>