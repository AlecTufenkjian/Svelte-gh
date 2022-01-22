

<script>
	let video;

	const constraints = {
	video: true
	};

	navigator.mediaDevices.getUserMedia(constraints).
		then((stream) => {video.srcObject = stream});
	
</script>
	
<video autoplay bind:this={video} width="100%" height="100%"></video>

<a-scene> 
	<a-entity id="hoop" rotation="90 0 0" position="0 2 -1.8"> 
		<a-torus scale="0.6 0.6 0.6" position="0 0.173 -0.1" color="#43A367" radius="0.25" radius-tubular="0.005"></a-torus>
		<a-plane
		 scale="0.6 0.6 0.6"
		 position="0 0 -0.3"
		 rotation="-90 0 0"
		 width="0.9"
		 height="0.9"
		 material="transparent: true; side: double;"
		 src="./backboard.png"
		></a-plane>
		<a-cone scale="0.6 0.6 0.6" position="0 0.173 -0.010" color="tomato" radius-bottom="0.25" radius-top="0.3" material="side: double; opacity:0.5; transparent: true;" geometry="height: 0.29; openEnded: true" rotation="90 0 0"></a-cone>
	</a-entity>
</a-scene>