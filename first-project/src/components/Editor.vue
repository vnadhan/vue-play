<template>
    <div>
        <!-- v-model="codeAsString"
                    @input="$emit('input', codeAsString)" -->
        <input class="resize border rounded-md h-screen w-full"
                    v-mdoel:codeAsString="$emit('input', $event.target.value)" />
    </div> 
</template>
<script>
    import { defineComponent } from 'vue'

    export default defineComponent({
    props: ['value'],
    setup() {
        console.log('what is the value ?? ');
    },
    data() {
        return {
            codeAsString: this.value? JSON.stringify(this.value): ""
        }
    },
    watch: {
        codeAsString(newValue) {
            console.log('codeAsString has a new value? ', newValue, typeof(newValue));
        }
    }
    })
</script>
