
<template>
    <div class="homewrap">
        <Wallet
        :cardList="cardList"
        />
        <button @click="addCard"><h1> ADD CARD</h1></button>
    </div>
</template>

<script>
import Wallet from '../components/Wallet.vue'
export default {
/* eslint-disable */

    props:{
        cardList:Array
    },
    components:{Wallet},
    data() {return{
       
    } },
    methods:{
            addCard(){
            this.$emit('add-card')
            console.log("Hej")
        }
    } 

}
</script>

<style >
.homewrap{
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
}

</style>