//# JS-Challenge-Day-1
//A javascript drumkit that makes sounds and lights up via keyboard interaction
<!DOCTYPE html>
<html>
<head>
	<title>JS DAY1 Drumkit</title>
	<link rel="stylesheet" type="text/css" href="style.css">
	<script src="script.js"></script>
</head>
<body>
	<div class="boss">
		
				<div data-key="65" class="key">
					<kbd>A</kbd>
					<span class="sound">clap</span>
				</div>

				<div data-key="83" class="key">
					<kbd>S</kbd>
					<span class="sound">hihat</span>
				</div>

				<div data-key="68" class="key">
					<kbd>D</kbd>
					<span class="sound">kick</span>
				</div>

				<div data-key="70" class="key">
					<kbd>F</kbd>
					<span class="sound">openhat</span>
				</div>

				<div data-key="71" class="key">
					<kbd>G</kbd>
					<span class="sound">boom</span>
				</div>

				<div data-key="72" class="key">
					<kbd>H</kbd>
					<span class="sound">ride</span>
				</div>

				<div data-key="74" class="key">
					<kbd>J</kbd>
					<span class="sound">snarf</span>
				</div>

				<div data-key="75" class="key">
					<kbd>K</kbd>
					<span class="sound">tom</span>
				</div>

				<div data-key="76" class="key">
					<kbd>L</kbd>
					<span class="sound">tink</span>
				</div>

				<audio data-key="65" src="boom.wav"></audio>
				<audio data-key="83" src="boom.wav"</audio>
				<audio data-key="68" src="boom.wav"></audio>
				<audio data-key="70" src="boom.wav"></audio>
				<audio data-key="71" src="boom.wav"></audio>
				<audio data-key="72" src="boom.wav"></audio>
				<audio data-key="74" src="boom.wav"></audio>
				<audio data-key="75" src="boom.wav"></audio>
				<audio data-key="76" src="boom.wav"></audio>
				

			

	</div><!--boss-->
</body>
</html>


.boss {
	display: grid;
	grid-template-columns:  repeat(9, 1fr);
	grid-template-rows: 200px 100px 50px;
	grid-gap: 10px;
	
}



.key {
	background-color: rgba(0,0,0,0.7);
	grid-row-start: 3;
	grid-row-end: 4;	
	color: pink;
	text-align: center;
}




body{
	background-image: url("http://davefarmersblog.files.wordpress.com/2012/03/dead_bunny_by_ravrilavren.jpg");
	background-size: 600px;
	background-attachment: fixed;
	background-repeat: no-repeat;
	background-position: center;
	
}



<script>
window.addEventListener('keydown', function(e){
	const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
	if(!audio) return; //stop the function from running all together
	audio.play();
});
  </script>
