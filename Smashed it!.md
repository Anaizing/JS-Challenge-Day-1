# JS-Challenge-Day-1
A javascript drumkit that makes sounds and lights up via keyboard interaction
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
					<span class="sound">boom</span>
				</div>

				<div data-key="83" class="key">
					<kbd>S</kbd>
					<span class="sound">snare</span>
				</div>

				<div data-key="68" class="key">
					<kbd>D</kbd>
					<span class="sound">doof</span>
				</div>

				<div data-key="70" class="key">
					<kbd>F</kbd>
					<span class="sound">smack</span>
				</div>

				<div data-key="71" class="key">
					<kbd>G</kbd>
					<span class="sound">boing</span>
				</div>

				<div data-key="72" class="key">
					<kbd>H</kbd>
					<span class="sound">bang</span>
				</div>

				<div data-key="74" class="key">
					<kbd>J</kbd>
					<span class="sound">ling</span>
				</div>

				<div data-key="75" class="key">
					<kbd>K</kbd>
					<span class="sound">poof</span>
				</div>

				<div data-key="76" class="key">
					<kbd>L</kbd>
					<span class="sound">tiss</span>
				</div>

				<audio data-key="65" src="boom.wav"></audio>
				<audio data-key="83" src="snare.wav"</audio>
				<audio data-key="68" src="doof.wav"></audio>
				<audio data-key="70" src="smack.wav"></audio>
				<audio data-key="71" src="boing.wav"></audio>
				<audio data-key="72" src="bang.wav"></audio>
				<audio data-key="74" src="ling.wav"></audio>
				<audio data-key="75" src="poof.wav"></audio>
				<audio data-key="76" src="tss.mp3"></audio>
				
				

	</div><!--boss-->
</body>
</html>




window.addEventListener('keydown', function(e){
	const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
	const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);
	if(!audio) return; //stop the function from running all together
	audio.currentTime = 0; //rewind to the start
	audio.play();
	key.classList.add('pressed');
});

window.addEventListener('keyup', function(e){
	const offKey = document.querySelector(`.key[data-key="${e.keyCode}"]`);
	offKey.classList.remove('pressed');

});

	
	
	
@import url('https://fonts.googleapis.com/css?family=Alegreya');

.boss {
	display: grid;
	grid-template-columns:  repeat(9, 1fr);
	grid-template-rows: 200px 100px 90px;
	grid-gap: 10px;
}


.key {
	transition:all .07s ease;
	background-color: rgba(0,0,0,0.7);
	grid-row-start: 3;
	grid-row-end: 4;	
	color: pink;
	word-wrap: break-word;
	text-align: center;
	border-radius: 10%;
	white-space: pre-line;
	text-shadow: 0 0 5px black;
}

kbd {
	font-size: 200%;
	font-family: 'Alegreya';

}

.pressed {
	background-color: rgba(0,0,0,0.9);
	box-shadow: 10px 10px 5px #333333;
	transform: scale(1.1);
	border: 3px solid #D3394C;

}


body{
	background-image: url("http://davefarmersblog.files.wordpress.com/2012/03/dead_bunny_by_ravrilavren.jpg");
	background-size: 600px;
	background-attachment: fixed;
	background-repeat: no-repeat;
	background-position: center;
	
}



