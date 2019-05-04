<template>
    <div></div>
</template>

<script>
    export default {
        name: "tfxi",
        props: {
            name: String,
        },
        computed: {
            id: function () {
                return this.name;
            }
        },
        watch: {
            id: function () {
                window.postMessage({type: "FROM_APP_TFXI", id: this.id, name: this.name}, "*");
            }
        },
        created() {

            window.addEventListener("message", function (event) {
                // We only accept messages from ourselves
                if (event.source != window)
                    return;

                if (event.data.type && (event.data.type == "FROM_SANAZ")) {
                    console.log("App received: " + event.data.id + " " + event.data.action);
                    // port.postMessage(event.data.action);
                }
            }, false);
        }
    }
</script>

<style scoped>

</style>