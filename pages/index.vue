<template>
  <div>
    <div id="homeBg">
      <div class="content-parent">
      <div class="content">
		<h2>Hello</h2>
		<h2>Hello</h2>
    <h1 class="d-block" data-text="hi.......">Hi.......</h1>
    </div>
   
	</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head() {
      return {
        script: [
          {
            src: 'https://cdnjs.cloudflare.com/ajax/libs/three.js/r134/three.min.js',
          },
          {
            src: 'https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.net.min.js',
          },
        ]
      }
    },
    mounted(){
      VANTA.NET({
  el: "#homeBg",
  mouseControls: true,
  touchControls: true,
  gyroControls: false,
  minHeight: 200.00,
  minWidth: 200.00,
  scale: 1.00,
  scaleMobile: 1.00,
  color: 0x4a3fff,
  backgroundColor: 0x20005
})
    }
}
</script>

<style>
#homeBg{
  height: 500px;
  position: relative;
}
@import url("https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900");

.content-parent {
  height: 500px;
	display: flex;
	align-items: center;
	justify-content: center;
}

.content {
	position: relative;
}

.content h2 {
	color: #fff;
	font-size: 8em;
	position: absolute;
	transform: translate(0%, -50%);
}

.content h2:nth-child(1) {
	color: transparent;
	-webkit-text-stroke: 2px #8338ec;
}

.content h2:nth-child(2) {
	color: #c19bf5;
	animation: animate 4s ease-in-out infinite;
}

@keyframes animate {
	0%,
	100% {
		clip-path: polygon(
			0% 45%,
			16% 44%,
			33% 50%,
			54% 60%,
			70% 61%,
			84% 59%,
			100% 52%,
			100% 100%,
			0% 100%
		);
	}

	50% {
		clip-path: polygon(
			0% 60%,
			15% 65%,
			34% 66%,
			51% 62%,
			67% 50%,
			84% 45%,
			100% 46%,
			100% 100%,
			0% 100%
		);
	}
}

/* neon text */


h1{
  margin-top: 40px;
    position: relative;
    font-size: 8em;
    color: #252839;
    text-transform: uppercase;
}
h1::before{
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    color: #c19bf5;
    overflow: hidden;
    animation: animateing 6s linear infinite;

}
@keyframes animateing{
    0%,10%,100%{
        width: 0;
    }
    70%,90%{
        width: 100%;
    }
}

</style>