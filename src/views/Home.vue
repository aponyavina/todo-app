<template>
    <div>
        <h2>Home page</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores consectetur dolor dolores eius esse eveniet natus officia porro quae sapiente.</p>
        <router-link to="/todos">Todos</router-link>
    </div>
</template>

<script>
    export default {
        name: "Home"
    }
</script>

<style scoped>
    p {
        max-width: 500px;
        margin: 0 auto 20px auto;
    }
</style>