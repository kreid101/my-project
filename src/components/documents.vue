<template>
<div id="doc">
    <div id="btn">
    <button v-on:click="link1()">Договор об аренде</button>
    <button v-on:click="secondlink()">Учредительный договор</button>
    <button v-on:click="thirdlink()">Заявление о приеме на работу</button>
    <button v-on:click="forthlink()">Заявление о представлении отпуска</button>
    <button v-on:click="fifthlink()">Договор на производство работ (оказание услуг)</button>
    </div>
    
    
<iframe  v-bind:src="link" frameborder="0" id="frame"></iframe>
</div>
   
</template>

<script>
export default{
    name:'document',
    data() {
        return {
        link:"https://drive.google.com/file/d/1YjUJ_NbkU6qbzV--ZpIC9fRPm6QVbf3v/preview",
        link2:'https://drive.google.com/file/d/1D4OEbZVh56eeoWRDDay0fMauwSP93ulv/preview',
        link3:'https://drive.google.com/file/d/1EdyzhamXbPC241ypHlRQlI8_patBvGpa/preview',
        link4:'https://drive.google.com/file/d/1Y1UBuweeOeWGOIPmX1PnioduByvhL5Am/preview',
        link5:'https://drive.google.com/file/d/1nZH3hSrtdgTyBaI32Tzyudu4ySgTzInV/preview'

        }
      
    },
    methods:{
        link1:function(){
            document.getElementById('frame').setAttribute('src',this.link)
        },
        secondlink:function(){
            document.getElementById('frame').setAttribute('src',this.link2)
        },
        thirdlink:function(){
            document.getElementById('frame').setAttribute('src',this.link3)
        },
        forthlink:function(){
            document.getElementById('frame').setAttribute('src',this.link4)
        },
        fifthlink:function(){
            document.getElementById('frame').setAttribute('src',this.link5)
        }
    }
}
</script>

<style scoped>
iframe{
    display: block;
    width: 80%;
    height: 60%;
}
#doc{
    height: 100%;
}
#btn{
    display: flex;
    justify-content: center;
}
#btn button {
    margin-right: 10px;
    margin-bottom: 40px;
}
iframe{
    margin-left:150px;
}
</style>