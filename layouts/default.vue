<template>
  <div>
    <div class="pagesMenu">
      <nuxt-link to="/">Page 1</nuxt-link>
      <nuxt-link to="/page2">Page 2</nuxt-link>
    </div>
    <nuxt/>
  </div>
</template>

<style>
.pagesMenu
{
  text-align: center;
  background-color: #3b8070;
}
.pagesMenu a
{
  background: #FFFFFF;
  color: #3b8070;
  padding-left:20px;
  padding-right: 20px;
  padding-top: 10px;
  padding-bottom: 10px;
  text-decoration: none;
  display: inline-block;
  vertical-align: top;
  margin-left: 1px;
  margin-right: 1px;
}
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
