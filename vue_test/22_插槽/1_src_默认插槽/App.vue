<template>
    <div class="container">
        <!-- 插槽 -->
        <Category title="美食">
            <img src="https://s3.ax1x.com/2021/01/16/srJ1q0.jpg" alt="">
        </Category>
        <Category title="游戏">
            <ul>
                <li v-for="(item,index) of games" :key="index">{{item}}</li>
            </ul>
        </Category>
        <Category title="电影">
            <img src="https://s3.ax1x.com/2021/01/16/srJ1q0.jpg" alt="">
        </Category>
    </div>
</template>

<script>
    import Category from './components/Category.vue'
    export default {
        name:'App',
        components:{
            Category
        },
        data() {
            return {
                foods:['火锅','烧烤','小龙虾','牛排'],
                games:['红色警戒',' 穿越火线','劲舞团','超级玛丽'],
                films:['《教父》','《拆弹专家》','《你好，李焕英》','《肖申克的救赎》']
            }
        },
    }
</script>

<style>
    .container{
        display: flex;
        justify-content: space-around;
    }
</style>