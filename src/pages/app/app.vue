<template>
<div class="contaier" :class="{'contaierb':isvariety,'contaierc':!isvariety}">
      <lb-breakcrumb></lb-breakcrumb>
       <lb-header @variety="variety"></lb-header>
      <lb-body></lb-body>
      <lb-footer></lb-footer>
  </div>      
</template>
<script>
import header from './header.vue'
import body from './body.vue'
import footer from './footer.vue'
import breakcrumb from './breakcrumb.vue'
export default{
    name:'app',
    data(){
        return {
            isvariety:false
        }
    },
    components:{
        'lb-header':header,
        'lb-body':body,
        'lb-footer':footer,
        'lb-breakcrumb':breakcrumb
    },
    methods:{
        variety(){
            this.isvariety = !this.isvariety
        }
    }
}
</script>
