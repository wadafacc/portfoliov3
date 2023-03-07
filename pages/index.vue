<template>
  <div class="container">
    <div class="link-container" id="links">
        <a class="link" id="yt" href="https://youtube.com/@tnksboi" target="_blank">
          <img src="~/assets/youtube.png" alt="">
        </a>
        <a class="link" id="gh" href="https://github.com/wadafacc" target="_blank">
          <img src="~/assets/github.png" alt="">
        </a>        
        <a class="link" id="tw" href="https://twitter.com/Wadafacc_" target="_blank">
          <img src="~/assets/twitter.png" alt="">
        </a>
        <a class="link" id="dc" href="https://discord.com/users/286888695879958530" target="_blank">
          <img src="~/assets/discord.png" alt="">
        </a>        
        <a class="link" id="sp" href="https://open.spotify.com/user/wiad858gtdujymm1qhgp5fbex?si=6aacc31d17524838" target="_blank">
          <img src="~/assets/spotify.png" alt="">
        </a>
        <a class="link" id="cat" href="https://www.youtube.com/watch?v=CbozHK38jDc" target="_blank">
          <img id="cat-img" src="~/assets/vibin2.gif" alt="">
        </a>
      </div>
    <div class="card" id="card">      
      <div class="bg-image"></div>
      <div class="bg-effect"></div>
      <div class="content" @click="turn()">
        <span id="click">CLICK ME</span>
        <div class="footer">
          <span class="title">ANOTHER WORLD</span>
          <a href="https://github.com/wadafacc" target="_blank">@functionizable</a>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  mounted(){
    console.log("Hey! No, this is not responsive just yet. ");
  },
  methods:{
    turn(){
      let card = document.getElementById("card");
      if (card.style.scale != "0.8"){
        card.style.scale = "0.8 0.8";
        card.style.transform = "rotateY(180deg)";
        this.reveal();
      }else{
        card.style.scale = "1 1";
        card.style.transform = "rotateY(0deg)"; 
        this.unReveal();
      }
    },
    reveal(){
      let dc = document.getElementById("dc");
      let yt = document.getElementById("yt");
      let gh = document.getElementById("gh");
      let cat = document.getElementById("cat");
      let sp = document.getElementById("sp");
      let tw = document.getElementById("tw");

      dc.style.transform = "translate(-25rem, -25rem)";
      dc.style.opacity = "100%";

      cat.style.transform = "translate(-24rem, 22rem)";
      cat.style.opacity = "100%";

      yt.style.transform = "translate(15rem, -28rem)";
      yt.style.opacity = "100%";

      gh.style.transform = "translate(18rem, 24rem)";
      gh.style.opacity = "100%";

      sp.style.transform = "translate(24rem, 2rem)";
      sp.style.opacity = "100%";

      tw.style.transform = "translate(-30rem, -6rem)";
      tw.style.opacity = "100%";

    },
    unReveal(){
      let dc = document.getElementById("dc");
      let yt = document.getElementById("yt");
      let gh = document.getElementById("gh");
      let cat = document.getElementById("cat");
      let sp = document.getElementById("sp");
      let tw = document.getElementById("tw");


      dc.style.transform = "translate(0rem,0rem)";
      dc.style.opacity = "0%";

      cat.style.transform = "translate(0rem,0rem)";
      cat.style.opacity = "0%";

      yt.style.transform = "translate(0rem,0rem)";
      yt.style.opacity = "0%";

      gh.style.transform = "translate(0rem,0rem)";
      gh.style.opacity = "0%";

      sp.style.transform = "translate(0rem,0rem)";
      sp.style.opacity = "0%";

      tw.style.transform = "translate(0rem,0rem)";
      tw.style.opacity = "0%";
    }
  }
};
</script>

<!-- <img src="~/assets/vibin2.gif" alt=""> -->
