<template>
  <div id="app">
     <div class="top" aspectratio w-750-320>
       <div aspectratio-content>宽高比750:320的布局</div>
     </div>
     <div class="middle" aspectratio w-450-230>
       <div aspectratio-content>中间内容区450:230</div>
     </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: blue;
  width: 750px;
  height: 1334px;
}
</style>

<!--默认设置的通用的CSS-->
<style>
  html {
    margin: 0;
    padding: 0;
    height: 100vh;
    box-sizing: border-box;
  }
  body {
    margin: 0;
    padding: 0;
    min-height: 100vh;
    background-color: #f4f4f4;
  }
  * {
    box-sizing: inherit;

    &:before,
    &:after {
     box-sizing: inherit;
    }
  }
  img {
    width: 100%;
    height: auto;
    vertical-align: top;
    content: normal !important;
  }
  [aspectratio] {
    position: relative;
  }
  [aspectratio]::before {
    content: '';
    display: block;
    width: 1px;
    margin-left: -1px;
    height: 0;
  }

  [aspectratio-content] {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
  }
  [flexContainer] {
    display: flex;
    width: 750px;
  }
  .block {
    margin-top: 15px;
  }
  ul,li {
    list-style: none outside none;
    margin: 0;
    padding: 0;
  }
  figure {
    display: block;
    margin: 0;
  }
</style>

<style>
  [w-750-320] {
    aspect-ratio:'750:320';
  }
  [w-750-320] {
    width: 750px;
    z-index: 5000;
  }
  .top{
    background: red;
  }
  .middle{
    background: greenyellow;
  }
  [w-450-230] {
    aspect-ratio:'450:230';
  }
  [w-450-230] {
    width: 450px;
    z-index: 5000;
  }
</style>
