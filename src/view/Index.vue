<template>
    <div>
        <Nav></Nav>
        <full-page :options="options" ref="fullpage">
                <div class="section">
                    <div class="slide">
                        <Mshose></Mshose>
                    </div>
                    <div class="slide">
                        <Mclothes></Mclothes>
                    </div>
                    <div class="slide">
                        <Mornaments></Mornaments> 
                    </div>
                </div>
                <div class="section">
                    <div class="slide">
                        <Wshose></Wshose>
                    </div>
                    <div class="slide">
                        <Wclothes></Wclothes>
                    </div>
                    <div class="slide">
                        <Wornaments></Wornaments> 
                    </div>
                </div>
                <div class="section">
                    <div class="publicity">
                        <Video class="publicity-video" loop autoplay>
                            <source src="../assets/Publicity video.mp4" type="video/mp4">
                        </Video>
                    </div>
                </div>
                <div class="section footerH">
                    <Footer></Footer>
                
                </div>
        </full-page>
    </div>
</template>

<script>
import '../css/fullpage.min.css'
import Nav from '../components/Nav'
import Mshose from './Mshose'
import Mclothes from './Mclothes'
import Mornaments from './Mornaments'
import Wshose from './Wshose'
import Wclothes from './Wclothes'
import Wornaments from './Wornaments'
import Footer from '../components/Footer'



export default {
    name:'index',
    components:{
        Nav,Mshose,Mclothes,Mornaments,Wornaments
        ,Wclothes,Wshose,Footer
    },
    data(){
        return{
            options:{
                licenseKey: null,
                verticalCentered: false, //??????????????????????????????????????????
                afterLoad: this.afterLoad, //????????????????????????????????????
                controlArrows: true, //????????????????????????slide?????????
                loopHorizontal: false, //slide???????????????????????????
                mscrollBar: true, //true??????????????????????????????
                monLeave: this.onLeave, //???????????????????????????
                navigation: true,
            }
        }
    }
}
</script>

<style scoped>
.publicity{
    width: 100%;
    height: 100%;
}
.publicity-video{
    width: 100%;
    height: 100%;
    object-fit: fill;
}
</style>