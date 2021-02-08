<template>
    <div name="show">
        <ul class="goodList">
            <li v-for="(good,index) in list" :key="index">
                <img v-bind:src="good.img">
                <p>{{good.goodName}}</p>
            </li>
        </ul>
    </div>
</template>
<style type="text/css">
    ul{
        padding: 0;
        margin: 0;
    }
.goodList li{
    width: 180px;
    height: 200px;
    list-style: none;
    float: left;
    font-size: 9px;
    color: red;
    margin: 10px;
}
.goodList li img{
    width: 180px;
    height:180px;
}
</style>
<script>
    export default {
        name: "show",
        data(){
            var obj=this;
            var url="";
            if(obj.goodId==1){
                url="json/tab1.json";
            }else if(obj.goodId==2){
                url="json/tab2.json";
            }else{
                url="json/tab1.json";
            }
            this.$http.get(url).then(function (res) {
                obj.list=res.data;
            })
            return{
                list:[]
            }
        },
        props:{
            goodId:Number
        },
        watch:{
            goodId(){
                var obj=this;
                var url="";
                if(obj.goodId==1){
                    url="json/tab1.json";
                }else if(obj.goodId==2){
                    url="json/tab2.json";
                }else{
                    url="json/tab1.json";
                }
                this.$http.get(url).then(function (res) {
                    obj.list=res.data;
                })
                return{
                    list:[]
                }
            }
        }
    }
</script>
