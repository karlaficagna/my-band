<template>
<section class="news">
<div class="container">
<div class="row">
<div class="col-md-12">
<h2 class="news__title">Notícias </h2>
</div>
</div>
<div class="row">
<div
v-for="myNew in newsFiltered"
:key="myNew.id"
:class="{'col-md-12' : myNew.title === 'Noticia 01' ,'col-md-6' : myNew.id !== 1}"
>
<div class="news__box">
<img :src="myNew.img" />
<h3>{{myNew.title}}</h3>
<p>{{myNew.text}}</p>
<router-link :to="{name: 'noticias-detalhe', params : { id : myNew._id}}"><span>Leia mais</span></router-link>
</div>
</div>
<div class="col-md-12" v-if="isButton">
<router-link to="/noticias" class="news__btn"><button>Veja mais</button></router-link>
</div>
</div>
</div>
</section>
</template>
<script>
export default {
name: "NewsComponent",
props : {
isButton : Boolean
},
data: function () {
return {
news: []
}
},
computed : {
newsFiltered : function (){
const news = this.news;
if(this.isButton){
return news.slice(0,3);
}
return news
}
},
methods : {
getNews : async function(){
const result = await fetch('http://localhost:3000/noticias')
.then(res => res.json())
.catch(error => {
return {
error: true,
message: error
}
});
if(!result.error){
this.news = result
}
}
},
created : function(){
this.getNews();
}
}

</script>
<style>
.news {
  background-color: #212121;
  padding: 56px 0;
  color: #e2e2e2;
}

.news__title {
  font-size: 36px;
}

.news h3 {
  font-size: 26px;
}

.news p {
  font-size: 16px;
}

.news span {
  color: #c3121c;
  font-size: 14px;
}

.news img {
  width: 100%;
}

.news__box {
  margin-bottom: 30px;
}

.news button {
  width: 170px;
  height: 40px;
  cursor: pointer;
  background: #c3121c;
  color: #212121;
  border-radius: 6px;
  border: none;
  font-weight: bold;
}

.news__btn {
  display: block;
  text-align: center;
  margin: 30px auto;
  width: 170px;
  height: 40px;
}
</style>