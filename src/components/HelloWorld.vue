/**
* @author:      zhouzhonghao
* @Description:  excle
* @date:        2020/11/10
*/
<template>
    <div class="hello">
        <div
                id="zzh"
                style="margin:0px;padding:0px;position:absolute;width:100%;height:100%;left: 0px;top: 50px;"
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
                    title:'zzh', //表 头名
                    lang: 'zh', //中文
                    column: 10,//列数
                    row:30,//行数
                    showtoolbar:true,//是否显示工具栏
                    showinfobar:true,//是否显示顶部信息栏
                    showsheetbar:true,//是否显示底部sheet按钮
                    allowEdit:true,//是否允许前端编辑
                    myFolderUrl:'https://www.cnblogs.com/javascript9527/',//<左上角的“后退”按钮的链接
                    functionButton:'<button id="" class="btn btn-primary" style="padding:3px 6px;font-size: 12px;margin-right: 10px;">download</button> <button id="" class="btn btn-primary btn-danger" style=" padding:3px 6px; font-size: 12px; margin-right: 10px;">share</button> <button id="luckysheet-share-btn-title" class="btn btn-primary btn-danger" style=" padding:3px 6px; font-size: 12px; margin-right: 10px;">show data</button>',//右上角按钮
                    cellRightClickConfig:{//自定义配置单元右键菜单
                        copy: true, // 复制
                        copyAs: true, // 复制为
                        paste: true, // 粘贴
                        insertRow: true, // 插入行insert row
                        insertColumn: true, // 插入列insert column
                        deleteRow: true, // 删除选中行的数据 delete the selected row
                        deleteColumn: true, // 删除选中列的数据delete the selected column
                        deleteCell: false, // delete cell
                        hideRow: true, // hide the selected row and display the selected row
                        hideColumn: true, // hide the selected column and display the selected column
                        rowHeight: true, // 设置行高
                        columnWidth: true, // 设置行宽
                        clear: true, // 清空选定内容clear content
                        matrix: false, //矩阵 matrix operation selection
                        sort: false, // 排序sort selection
                        filter: false, //筛选 filter selection
                        chart: false, //图表生成 chart generation
                        image: false, //插入图片 insert picture
                        link: false, // 插入连接，比如网址之类insert link
                        data: false, //数据校验 data verification
                        cellFormat: false //设置单元格格式，锁定单元格格式，隐藏公示等 Set cell format
                    },

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
