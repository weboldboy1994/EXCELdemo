/**
* @author:      zhouzhonghao
* @Description:  excle
* @date:        2020/11/10
*/
<template>
    <div class="hello">
        <div
                id="zzh"
                style="margin:0px;padding:0px;position:absolute;width:100%;height:500px;left: 0px;top: 50px;"
        ></div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        data() {
            return {
            }
        },
        mounted() {
            this.init()
        },
        methods:{
            init(){
                var options = {
                    container: 'zzh', //luckysheet为容器id
                    title:'报表', //表头名
                    lang: 'zh' //中文
                }
                luckysheet.create(options)
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: inline-block;
        margin: 0 10px;
    }
    a {
        color: #42b983;
    }
</style>
