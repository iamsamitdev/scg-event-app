<template>
    <div>
        <h1>Event list #{{ id }}</h1>
    </div>
</template>

<script>
    export default {
        props: {
            id:{
                required: true
            }
        }
    }
</script>