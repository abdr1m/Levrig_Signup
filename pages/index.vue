<template>
    <!-- app container -->
    <div class="app">
        <heading />
        <signup />
    </div>
</template>
<script>
    import heading from "../components/header.vue"
    import signup from "../components/signup_form.vue"
    export default { 
        components: {
            heading,
            signup
        }
    } 
</script>
