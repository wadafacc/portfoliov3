<template>
  <div class="container" @mousemove="move()">
    <div id="tracer" class="tracer-wrapper">
      <div class="tracer"></div>
    </div>
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
    <div @click="turn()">
      <div class="card" id="card">
      <div class="bg-image"></div>
      <div id="bg">
        <div class="bg-image"></div>
        <div>
          <h1>Hey! <span>I'm Timo.</span></h1>
          <div class="text">
            I'm a fullstack Dev with a passion for intricate design.
          </div>
          <br/>
          <div class="text">I have around 3 years experience in developing, maintaining, testing and breaking all sorts of applications, to make the</div>
          <span class="highlight">internet a better place.</span>
          <div class="text">
           Get in touch! Feel free to shoot me a DM on any of my socials.
          </div>
          <div class="text-footer">
            Cheers,<br/>
            functionizable
          </div>
        </div>
      </div>    
      <div class="content">
        <span id="click">CLICK ME</span>
        <div class="footer">
          <span class="title">ANOTHER WORLD</span>
          <a href="https://github.com/wadafacc" target="_blank">@functionizable</a>
        </div>
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
      let bg = document.getElementById("bg");
      if (card.style.scale != "0.8"){
        card.style.scale = "0.8 0.8";
        card.style.transform = "rotateY(180deg)";
        // change card back to black
        bg.style.zIndex = "10";
        bg.style.opacity = "100%";
        this.reveal();
      }else{
        card.style.scale = "1 1";
        card.style.transform = "rotateY(0deg)"; 
        bg.style.zIndex = "0";
        bg.style.opacity = "0%";
        this.unReveal();
      }
    },
    // not the most elegant solution, but works :D
    reveal(){
      let dc = document.getElementById("dc");
      let yt = document.getElementById("yt");
      let gh = document.getElementById("gh");
      let cat = document.getElementById("cat");
      let sp = document.getElementById("sp");
      let tw = document.getElementById("tw");

      dc.style.transform = "translate(-20rem, -23rem)";
      dc.style.opacity = "100%";

      cat.style.transform = "translate(-22rem, 18rem)";
      cat.style.opacity = "100%";

      yt.style.transform = "translate(15rem, -20rem)";
      yt.style.opacity = "100%";

      gh.style.transform = "translate(18rem, 16rem)";
      gh.style.opacity = "100%";

      sp.style.transform = "translate(20rem, 2rem)";
      sp.style.opacity = "100%";

      tw.style.transform = "translate(-25rem, -6rem)";
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
    },
    move() {
      let tracer = document.getElementById("tracer");
      let {clientX, clientY} = window.event;
      
      tracer.animate({
        left: `${clientX}px`,
        top: `${clientY}px`,
      },{duration:2000, fill:"forwards"});

    }
  }
};
</script>

<!-- <img src="~/assets/vibin2.gif" alt=""> -->
