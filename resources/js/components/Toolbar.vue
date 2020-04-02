<template>
    <div>
        <v-card color="grey lighten-4" tile>
            <v-toolbar dense>
                <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->
                <v-toolbar-title >
                    <v-btn text to="/">Larvupush</v-btn>
                </v-toolbar-title>

                <v-spacer></v-spacer>

                <v-toolbar-items>
                    <v-btn text to="/forum">Forum</v-btn>

                    <v-btn text to="/ask">Ask Question</v-btn>

                    <v-btn text to="/category">Category</v-btn>

                    <v-btn text to="/login">Login</v-btn>
                </v-toolbar-items>
            </v-toolbar>
        </v-card>
    </div>
</template>

<script>
export default {};
</script>
