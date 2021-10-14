<template>
    <div>
        {{msg}}
    </div>
</template>

<script>
    /*
    * 不管是单文件对的template形式生成模板还是使用template属性，最终都是生成一个render函数
    * render函数中会调用createElement(...)，方法返回值就是该组件的VNode模板
    * 如果再el挂在了原生html对象，或可在new Vue().$mount(...)中指定原生html对象
    * 则createElement生成的VNode树会生成html串挂载到指定原生html对象，
    * 挂载过程其实也是调用vm的update方法
    * */
    /*
    * 组件就是维护自身的响应式data与methods等，改变之后再调用render生成新的VNode树，再和旧的VNode对比进行
    * 两颗VNode之间有不同的则对应去修改，再把修改后的节点赋值给当前vm的$el
    * */
    export default {
        props: ["msg"],
        data: function () {
            return {}
        },
        methods: {},
        computed: {}
    }
</script>

<style scoped>

</style>