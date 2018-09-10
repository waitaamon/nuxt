<template>
    <div>
        <input type="text" v-model="userId">
        <button @click="onloadUser">Load user</button>
        <nuxt-child/>
    </div>
</template>
<script>
export default {
    data() {
        return {
            userId: '',
        }
    },
    methods: {
        onloadUser() {
            this.$router.push('/users/' + this.userId);
        }
    }
}
</script>

