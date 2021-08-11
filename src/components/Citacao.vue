<template>
<section class="citacao">
<div class="container">
    <div class="row">
<div class="col-md-12">
<p class="citacao__text">
“Lorem Ipsum is simply dummy text of the printing
and typesetting industry. Lorem Ipsum has been the
industry's standard dummy text ever since the 1500s,
when an unknown printer took a galley of type and
scrambled it to make a type specimen book. “
</p>
<p class="citacao__author">(Mano Bronw)</p>
</div>
</div>
</div>
</section>
</template>
<script>
export default {
name : "Citacao"
}
</script>
<style>
html, body {
margin: 0px;
padding: 0px;
font-family: sans-serif
}
.container {
width: 100%;
max-width: 960px;
height: 100%;
display: flex;
margin: auto;
flex-wrap: wrap;
}
.row {
display: flex;
flex-direction: row;
flex-wrap: wrap;
align-items: center;
flex: 1;
width: 100%;
}
.col-md-1{
width: calc(960px/12 * 1);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-2{
width: calc(960px/12 * 2);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-3{
width: calc(960px/12 * 3);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-4{
width: calc(960px/12 * 4);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-5{
width: calc(960px/12 * 5);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-6{
width: calc(960px/12 * 6);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-7{
width: calc(960px/12 * 7);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-8{
width: calc(960px/12 * 8);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-9{
width: calc(960px/12 * 9);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-10{
width: calc(960px/12 * 10);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-11{
width: calc(960px/12 * 11);
box-sizing: border-box;
padding: 0px 10px
}
.col-md-12{
width: calc(960px/12 * 12);
box-sizing: border-box;
padding: 0px 10px
}
.citacao {
background-color : #0A0A0A;
width: 100%;
height: 255px;
}
.citacao .citacao__text {
color: #C3121C;
font-size : 24px;
font-style: italic;
}
.citacao .citacao__author {
color: #C3121C;
font-size : 16px;
text-align: right;
}
</style>
