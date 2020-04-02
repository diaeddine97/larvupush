<template>
    <div>
        <v-container grid-list-xs>
            <v-form ref="form" @submit.prevent="login">
                <v-text-field
                    v-model="form.email"
                    label="E-mail"
                    type="email"
                    required
                    clearable
                ></v-text-field>

                <v-text-field
                    v-model="form.password"
                    label="Password"
                    type="password"
                    required
                    clearable
                ></v-text-field>

                <v-btn
                    color="success"
                    class="mr-4"
                    type="submit"
                >
                    Login
                </v-btn>

            </v-form>
        </v-container>
    </div>
</template>

<script>
export default {
    data(){
        return {
            form:{
                email: null,
                password:null,
            }
        }
    },
    methods:{
        login(){
            axios.post('/api/auth/login',this.form)
                .then(res => console.log(res.data))
                .catch(error => console.log(error.response.data))
        }
    }
};
</script>
