<template>
   
        <div class="mui-numbox" data-numbox-min='1' data-numbox-max='99'>
               <button class="mui-btn mui-btn-numbox-minus" type="button">-</button>
               <input id="test" class="mui-input-numbox" type="number"   value="1" @change="pushval" ref="nbox" />
               <button class="mui-btn mui-btn-numbox-plus" type="button">+</button>
		</div>
    
</template>

<script>

import mui from '../../lib/mui/js/mui.min.js'
import numberbox from '../overall/NumberBox.vue'
export default {
    data() {
        return {
            
        }
    },
    methods:{
        pushval(){
            this.$emit("getcount",parseInt(this.$refs.nbox.value))
        }
    },
    mounted() {
        mui(".mui-numbox").numbox()
    },
}
</script>

<style >
    
    .mui-numbox {
        height: 25px;
    }
</style>