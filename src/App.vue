<template>
    <v-app>
        <v-main>
            <v-container>
                <v-row justify="center">
                    <v-col xl="7">
                        <v-card>
                            <v-toolbar>
                                <v-toolbar-items>
                                    <v-btn text @click="addData">Add</v-btn>
                                </v-toolbar-items>
                            </v-toolbar>
                            <v-card-text>
                                <v-list-item> </v-list-item>
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
        <Dialog ref="dlg" />
    </v-app>
</template>

<script>
import Dialog from "./components/Dialog.vue";
export default {
    name: "App",
    components: {
        Dialog,
    },
    data: () => ({
        items: [],
    }),
    methods: {
        addData() {
            this.$refs.dlg.open().then(() => {
                //
            });
        },
    },
};
</script>
