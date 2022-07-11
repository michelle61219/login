<template>
    <form @submit.prevent="Submit">
    <label for ="">Email</label>
    <input type ="text" v-model="form.email" required>
    <br><br>
    <label for=""> Password</label>
    <input type ="password" v-model ="form.password" required>
    <br><br>
    <button type ="submit">Login</button>
    <br><br>
    </form>
</template>

<script>
export default{
    data() {
        return {
            form:{
                email:"",
                password:"",
            }
        }
    },

    methods:{
        Submit(){
            this.$store.commit('login', this.form.email)
        }
    }
}
</script>
