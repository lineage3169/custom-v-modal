<template>
    <b-modal v-model="modalShow">
        ModalB
    </b-modal>
</template>
<script>
export default {
    name: 'ModalB',
    props: ['value'],
    data() {
        return {
            modalShow: false
        }
    },
    watch: {
        value(data) {
            // 父層props
            this.modalShow = data
        },
        modalShow(data) {
            this.$emit('input',data)
        }
    }
}
</script>