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
                    <v-btn v-for="item in items" :key="item.title" text :to="item.to" v-if="item.show">{{item.title}}</v-btn>
                </v-toolbar-items>
            </v-toolbar>
        </v-card>
    </div>
</template>

<script>
export default {
    data(){
        return {
            items: [
                {title: 'Forum', to: '/forum', show: true, },
                {title: 'Ask Question', to: '/ask', show: User.loggedIn(), },
                {title: 'Category', to: '/category', show: User.loggedIn(), },
                {title: 'Login', to: '/login', show: !User.loggedIn(), },
                {title: 'Logout', to: '/logout', show: User.loggedIn(), },
            ]
        }
    },
    created(){
        EventBus.$on('logout', () => User.logout())
    }
};
</script>
