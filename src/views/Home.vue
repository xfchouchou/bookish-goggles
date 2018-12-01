<template>
    <div v-title data-title="登陆" class="login-page">
        <div class="block">
            <el-carousel trigger="click" height="450px">
                <el-carousel-item v-for="item in hover" :key="item">
                    <div class="grid-content">
                        <div class="hover_bgc" :style="{ 'background': 'url(' + item.src + ') center top no-repeat fixed', 'background-size': 'cover'}">
                                <div class="hover_text">{{item.txt}}</div>
                        </div>
                    </div>
                </el-carousel-item>
            </el-carousel>
        </div>
    </div>
</template>

<script>
    // @ is an alias to /src
    /* eslint-disable */
    export default {
        name: '',
        components: {},
        data: function () {
            return {
                hover: [
                    {
                        src: require('../assets/hover_1.png'),
                        txt: '"Sed semper lorem at felis. Vestibulum volutpat, lacus a ultrices sagittis, mi neque euismod dui, eu pulvinar nunc sapien ornare nisl. Phasellus pede arcu, dapibus eu, fermentum et, dapibus sed, urna."',
                        txt2: '一站式服务',
                        txt3: 'Miami, FL'
                }, {
                        src: require('../assets/hover_2.png'),
                        txt: '"Sed egestas, ante et vulputate volutpat, eros pede semper est, vitae luctus metus libero eu augue. Morbi purus libero, faucibus adipiscing, commodo quis, gravida id, est. Sed lectus. Praesent elementum hendrerit tortor."',
                        txt2: '国际服务',
                        txt3: 'Greensboro, NC'
                }, {
                        src: require('../assets/hover_3.png'),
                        txt: '"Praesent elementum hendrerit tortor. Sed semper lorem at felis. Vestibulum volutpat, lacus a ultrices sagittis eu pulvinar nunc sapien ornare nisl. Phasellus pede arcu, dapibus eu, fermentum et, dapibus sed, urna."',
                        txt2: '全网渠道',
                        txt3: 'Charlotte, NC'
                }, {
                    src: require('../assets/hover_4.png'),
                    txt: '"Praesent elementum hendrerit tortor. Sed semper lorem at felis. Vestibulum volutpat, lacus a ultrices sagittis eu pulvinar nunc sapien ornare nisl. Phasellus pede arcu, dapibus eu, fermentum et, dapibus sed, urna."',
                    txt2: '全网渠道',
                    txt3: 'Charlotte, NC'
                }
                ]
            }
        },
        methods: {},
        created() {
        },
        mounted() {
        }
    }
</script>

<style lang="scss">
    /*.el-carousel__item h3 {*/
        /*color: #475669;*/
        /*font-size: 14px;*/
        /*opacity: 0.75;*/
        /*line-height: 150px;*/
        /*margin: 0;*/
    /*}*/

    /*.el-carousel__item:nth-child(2n) {*/
        /*background-color: #99a9bf;*/
    /*}*/

    /*.el-carousel__item:nth-child(2n+1) {*/
        /*background-color: #d3dce6;*/
    /*}*/

    .hover_bgc{
        height: 450px;
        width: 100%;
        background-size:cover;
        display: flex;
        .hover_text {
            margin-left: 40px;
            width: 40%;
            color: #fff;
            font-size: 30px;
            font-weight: bolder;
        }
    }

    .el-carousel__arrow{
        font-size:40px !important;
        font-weight: bolder;
        height: 60px !important;
        width: 60px !important;
    }
</style>
