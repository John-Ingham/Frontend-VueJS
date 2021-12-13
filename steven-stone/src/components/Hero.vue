<script lang="ts">
import { defineComponent } from "vue"
import useRouter from "vue-router"

// declare imports, functions and states in here

export default defineComponent ({
  setup() {
    // const router = useRouter()
    const navigateFunction1 = () => {
      console.log("Button 1 pressed")
      // navigate to desired page/component
    }
    const navigateFunction2 = () => {
      console.log("Button 2 pressed")
      // navigate to desired page/component
    }
    return {navigateFunction1, navigateFunction2 }
  }
})
</script>


<template>
<div  class="backdrop"> <!-- image url -->
    <div class="textContainer">
    <p class="lead">DISCOVER</p> <!-- //lead text -->
    <p class="title">YOUR STONE</p> <!-- // title text -->
    <p class="description"> Let us take you on a journey to discover the pefect stone for you as a person and to most suit your personality and complexion </p> <!-- // Description text -->
    </div>

    <div class="buttonContainer" >
    <!-- //button, boolean, background colour, text colour, text, onClick -->
    <!-- //emit onClick to parent, console.log emit & receipt -->
    <button class="button1" v-if="true" @click="navigateFunction1"> Go to page 1 </button> 
    
    <!-- //button, boolean, background colour, text colour, text, onClick -->
    <!-- //emit onClick to parent, console.log emit & receipt -->
    <button class="button2" v-if="true" @click="navigateFunction2"> Go to page 2 </button>
    </div>
    </div>
</template>

<!-- styling and CSS upon items -->
<style >
.backdrop {
    margin:0px;
    top:0;
    position: absolute;
    width:100%; 
     height:100%;
    display: fill;
    background-repeat: no-repeat; 
    background-size: cover;
    position: relative;
    background: url("https://cdn.stevenstone.co.uk/website_steven_stone/static/src/images/london/store-london-hero.jpg"); 
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
    
 }
 .textContainer {
   
   display: flex;
   flex-direction:column;
   justify-content: flex-start;
   align-items: left;
   margin-left: 10rem;
 }
 .lead {
   color: #4d84bb;
   font-family: arial;
   font-size: 36px;
   font-weight: 400;
   padding: 0;
   margin:0;
 }
 .title {
   color: #4d84bb;
   font-family: arial;
   font-size: 72px;
   font-weight: bold;
   padding: 0;
   margin: 0;

 }
 .description {
   color: #4d84bb;
   font-family: arial;
   font-size: 20px;
   padding: 0;
   margin: 0;
 }
 .buttonContainer {
   margin-left: 10rem;;
   display:  flex;
   flex-direction: row;
   justify-content: flex-start;
   
 }
 .button1 {
   display: flex;
   justify-content: left;
   
   flex-wrap: wrap;
   background-color: #0891B2 ;
  color: white;
  border: 1px solid r#034a5c ;
  padding: 0.5em 1em;
  border-radius: 5px;
  font-size: 1.1rem;
  transition: 150ms;
  margin: 1em 0;
}
.button2 {
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   background-color: transparent;
  color: white;
  border: 1px solid r#034a5c ;
  padding: 0.5em 1em;
  border-radius: 5px;
  font-size: 1.1rem;
  transition: 150ms;
  margin: 1em 1.2em;
}
button:hover {
  cursor: pointer;
  background-color: #034a5c ;
  opacity: 0.9;
  transition: 150ms;
}

@media screen and (max-width: 600px) {
  .description {
    display: none;
  }
  
}
@media screen and (max-width: 600px) {
  div.buttonContainer {
   margin-left: 2rem;
   display:  flex;
   flex-direction: column;
   justify-content: center;
   flex-wrap: wrap;
   
 }
}
@media screen and (max-width: 600px) {
  .button1 {
   display: flex;
   justify-content: center;
   flex-wrap: wrap;
   background-color: #0891B2 ;
  color: white;
  border: 1px solid r#034a5c ;
  padding: 0.25em 0.25em;
  border-radius: 5px;
  font-size: 1.1rem;
  transition: 150ms;
  margin: 0em 1.5em 0.5em 1.5em;
}
}
@media screen and (max-width: 600px) {
  .button2 {
   display: flex;
   flex-wrap: wrap;
   justify-content:center;
   background-color: transparent;
  color: white;
  border: 1px solid r#034a5c ;
  padding: 0.25em 0.25em;
  border-radius: 5px;
  font-size: 1.1rem;
  transition: 150ms;
  margin: 0em 1.5em 0.5em 1.5em;
}
}
@media screen and (max-width: 600px) {
  .textContainer {
   
   display: flex;
   flex-direction:column;
   justify-content: flex-start;
   align-items: left;
   margin-left: 2rem;
 }
}

 
</style>