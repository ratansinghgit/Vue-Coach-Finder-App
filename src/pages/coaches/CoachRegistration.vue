<template>
<section>
    <base-card>
    <h2>Register as a coach</h2>
    <coach-form @save-data="saveData"></coach-form>
    </base-card>
</section>
</template>
<script>
import CoachForm from '../../components/coaches/CoachForm.vue'
export default {
    components:{
        CoachForm
    },
    methods:{
        saveData(data){
            console.log("data",data)
            this.$store.dispatch('coaches/registerCoach',data)
            this.$router.replace('coaches')
        }
    }
}
</script>