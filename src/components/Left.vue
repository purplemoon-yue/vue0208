<template>
     <div>
         <div class="title">热门推荐</div>
         <ul class="menu">
             <li @click="menu1">切换1</li>
             <li @click="menu2">切换2</li>
             <li @click="menu3">切换3</li>
             <li @click="menu4">切换4</li>
             <li @click="menu5">切换5</li>
             <li>切换6</li>
             <li>切换7</li>
             <li>切换8</li>
             <li>切换9</li>
             <li>切换10</li>
             <li>切换11</li>
         </ul>
     </div>
</template>

<script>
    import Msg from './msg.js'
    export default {
        methods:{
            menu1:function () {
                Msg.$emit("val","1");
            },
            menu2:function () {
                Msg.$emit("val","2");
            },
            menu3:function () {
                Msg.$emit("val","3");
            },
            menu4:function () {
                Msg.$emit("val","4");
            },
            menu5:function () {
                Msg.$emit("val","5");
            },
        }
    }
</script>

<style type="text/css">
    .title{
        width: 100px;
        color: red;
    }
    .menu{
        padding: 0;
        margin: 0;
    }
    .menu li{
        width: 100px;
        list-style: none;
        height: 50px;
        margin-bottom: 2px;
        background-color: #ffffff;
        line-height: 50px;
        cursor: pointer;
    }
</style>
