<template>
    <div class="alert">
      <div class="box">{{msg}}</div>
      <Button type="success" @click="hidden">ok</Button>
    </div>

</template>

<script>
export default {
    name: 'Alert',
    props:['msg'],
    data () {
        return {

        }
    },
    methods: {
      hidden(){
        this.$emit('fromChild',false)
      }
    },
}

</script>

<style scoped>
.alert{
    font-size: 30px;
    text-align: center;
    width: 300px;
    height: 200px;
    border: 1px solid #aaa;
    border-radius: 5px;
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
    z-index: 99;
    background-color: gray;
}

</style>
