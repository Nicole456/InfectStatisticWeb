<template>
  <div id="wrap1">
    <div id="nav-bar">
      <div id="button" :style={opacity:router} @click="$emit('toAll')">
        <img src="../assets/arrow.svg" />
        <div>返回</div>
      </div>
      <div id="banner" :style="{'padding-left':getPL}">疫情实时动态</div>
    </div>
    <div id="line1"></div>
    <div id="title">
      <div></div>
      <div>{{banner}}<span style="color:#ddd;font-size:12px;padding-left:5px;font-weight:normal">
			--表示数据源未提供</span></div>
      <div id="line2"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "navi",
  props: {
    broad: String,
    banner: String,
    router:Number,
  },
  computed:{
     getPL(){
        return (parseInt(this.broad)/2 -150)+'px'
     }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
html,
body {
  margin: 0;
  padding: 0;
}

#wrap1 {
  display: flex;
  flex-direction: column;
  margin: 0;
  width: auto;
  /* width: 381px; */
}

#nav-bar {
  display: flex;
  height: 46px;
}
#button {
  width: 100px;
  height: 50px;
  clear: both;
  padding-top: 3px;
}
#button img {
  width: 12px;
  height: 18px;
  float: left;
  margin: 10px;
}
#button :hover {
  filter: brightness(1.4);
  color: rgb(43, 58, 133);
  cursor: pointer;
  transition: 0.15s all;
}
/* #banner:hover{
  filter: brightness(1.4);
  color: rgb(43, 58, 133);
  cursor: pointer;
  transition: 0.15s all;
} */
#button div {
  float: left;
  height: 30px;
  padding: 0;
  margin: 7px 24px 3px -5px;
}
#banner {
  width: auto;
  text-align: center;
  padding-top: 11px;
  transform: translateX(0);
}
#line1 {
  clear: both;
  height: 7px;
  background-color: rgba(242, 242, 242, 1);
}
#title {
  height: 50px;
}

#title div:nth-child(1) {
  float: left;
  width: 5px;
  height: 19px;
  background-color: rgba(65, 107, 221, 1);
  margin-bottom: 0px;
  margin-top: 17px;
  margin-left: 20px;
}

#title div:nth-child(2) {
  float: left;
  font-weight: bold;
  font-size: 19px;
  height: 40px;
  margin: 13px 20px 0px 7px;
}

#title div:nth-child(3) {
  clear: both;
  height: 2px;
  background-color: rgba(242, 242, 242, 1);
}

#wrap2 {
  display: flex;
  flex-direction: column;
  margin: 10px auto;
  width: auto;
  width: 366px;
}
#wrap2 .query {
  margin: 8px 0;
  /* width: 100%; */
  height: 112px;
  border-radius: 5px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
#wrap2 .query:nth-child(1) {
  background: rgba(165, 199, 108, 0.968627450980392);
}
#wrap2 .query:nth-child(2) {
  background-color: rgba(108, 179, 199, 1);
}
#wrap2 .query:nth-child(3) {
  background-color: rgba(199, 108, 108, 1);
}
.icon {
  width: 60px;
  height: 60px;
}
.text-wrapper {
  display: flex;
  flex-direction: column;
}
.text-wrapper div {
  display: inline-block;
  color: white;
}
.text-wrapper div:nth-child(1) {
  margin-top: -5px;
  display: inline-block;
  font-size: 20px;
  font-weight: bold;
}
.text-wrapper div:nth-child(2) {
  margin-top: 5px;
}

#pic {
  margin: 10px auto;
  display: flex;
  align-items: center;
  height: 228px;
  border-radius: 5px;
  border: 0px none;
}
</style>
