<style>
    .recommend{
        display: flex;
        width: 100%     ;
        text-align: center;
        font-size: 13px;

        padding: 10px 0 20px 0;
        border-bottom: 10px solid #eee
    }

    .recommend-item{
        flex: 1;
    }

    .recommend-item img{
        height: 78px;
        width: 78px;
        margin-bottom: 10px;
    }
</style>

<template>
    <div class="recommend">
        <div class="recommend-item" v-for=" (item,index) in recommends" :key="index">
            <a :href="item.link">
                <img :src="item.image">
                <div>{{item.title}}</div>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "RecommendView",
    props: {
        recommends: {
            type: Array,
            default(){
                return []
            }
        }
    },
    data() {
        return {
        }
    },
}
</script>
