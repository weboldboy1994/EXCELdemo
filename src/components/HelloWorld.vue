/**
* @author:      zhouzhonghao
* @Description:  excle
* @date:        2020/11/10
*/
<template>
    <div class="hello">
        <div
                id="luckysheet"
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
                options:[
                    {
                        "name": "Cell", //Worksheet name
                        "color": "", //Worksheet color
                        "index": 0, //Worksheet index
                        "status": 1, //Worksheet active status
                        "order": 0, //The order of the worksheet
                        "hide": 0,//Whether worksheet hide
                        "row": 36, //the number of rows in a sheet
                        "column": 18, //the number of columns in a sheet
                        "defaultRowHeight": 19, //Customized default row height
                        "defaultColWidth": 73, //Customized default column width
                        "celldata": [], //Initial the cell data
                        "config": {
                            "merge":{}, //merged cells
                            "rowlen":{}, //Table row height
                            "columnlen":{}, //Table column width
                            "rowhidden":{}, //hidden rows
                            "colhidden":{}, //hidden columns
                            "borderInfo":{}, //borders
                            "authority":{}, //Worksheet protection
                        },
                        "scrollLeft": 0, //Left and right scroll bar position
                        "scrollTop": 315, //Up and down scroll bar position
                        "luckysheet_select_save": [], //selected area
                        "calcChain": [],//Formula chain
                        "isPivotTable":false,//Whether is pivot table
                        "pivotTable":{},//Pivot table settings
                        "filter_select": {},//Filter range
                        "filter": null,//Filter configuration
                        "luckysheet_alternateformat_save": [], //Alternate colors
                        "luckysheet_alternateformat_save_modelCustom": [], //Customize alternate colors
                        "luckysheet_conditionformat_save": {},//condition format
                        "frozen": {}, //freeze row and column configuration
                        "chart": [], //Chart configuration
                        "allowEdit": true, //is editable
                        "zoomRatio":1, // zoom ratio
                        "image":[], //image
                        "showGridLines": 1, //Whether to show grid lines
                    },
                    {
                        "name": "Sheet2",
                        "color": "",
                        "index": 1,
                        "status": 0,
                        "order": 1,
                        "celldata": [],
                        "config": {}
                    },

                ]
            }
        },
        mounted() {
            this.init()
        },
        methods:{
            init(){
                var options = {
                    container: 'luckysheet', //luckysheet为容器id
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
