<template>
    <v-dialog v-model="dialog" width="600">        
        <v-card>
            <v-toolbar>
                <v-toolbar-title>Tambah data</v-toolbar-title>
            </v-toolbar>
            <v-card-text>
                <v-text-field label="Nama"></v-text-field>
                <v-textarea label="Alamat"></v-textarea>
            </v-card-text>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn>Simpan</v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>

<script>
export default {
    data() {
        return {
            nama: "",
            alamat: "",

            resolve: null,
            reject: null,
            dialog: false,
        };
    },
    methods: {
        open() {
            return new Promise((resolve, reject) => {
                this.resolve = resolve;
                this.reject = reject;

                this.dialog = true;
            });
        },
    },
};
</script>

<style></style>
