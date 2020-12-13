<template>
    <b-modal v-model="modalShow">
        ModalA
    </b-modal>
</template>
<script>
export default {
    name: 'ModalA',
    props: ['propsData'],
    data() {
        return {
            modalShow: false
        }
    },
    watch: {
        propsData(data) {
            // 當值被改變時
            console.log(data)
            this.modalShow = data
        },
        modalShow(data) {
            if(data === false)
                this.$emit('closeModal')
        }
    }
}
</script>