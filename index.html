<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Wumpus World!</title>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<style>
body {
	text-align:center;
	background-color:#666;
	margin:0;
	font-family:"Lucida Console", Monaco, monospace;
}
#cont {
	display:inline-block;
	background-color:#DDD;
	padding:20px;
}
#console {
	font-family:"Lucida Console", Monaco, monospace;
	font-size:12px;
	
}
#pos {
	width:300px;
	height:1000px;
	float:left;
	background-color:#FFF;
}
h2 {
	background-color:#000;
	margin:0;
	color:#FFF;
}
#header {
	background-color:#000;
	color:white;
	font-size:52px;
	padding:10px;
	margin:0;
	text-align:center;
	font-family:impact;
}
.hidden {
	background-color:#333;
	color:#333;
}
.caution {
	background-color:#FF0;
	color:#FF0;
}
.danger {
	background-color:#F00;
	color:#F00;
}
table {
	margin: auto;
	/* [disabled]display:inline-block; */
}
table,tr,td {
	border:2px solid black;
	background-color:#FFF;
}
td {
	width:85px;
	height:85px;
	text-align:center;
}
button {
	display:inline-block;
}
input {
	display:inline-block;
	width:30px;
	text-align:center;
}
</style>
</head>

<body>
<div id="header">Wumpus World!</div>
<div id="pos"><h2>CONSOLE</h2><br/>
<div id="console"></div>
</div>
<div id="cont">
<table>
<script type="text/javascript">
//Runs the code inside every 100 milliseconds; used for the auto play function
window.setInterval(function(){
	if (!gameOver && auto)
  		move();
}, 100);

//Generates the table with uniquely ID'd cells in which for the game to take place
for (i=0; i<7;i++) {
	document.write("<tr>");
	for (q=0; q < 7; q++) {
			document.write('<td id="r'+i+'c'+q+'" class="hidden"></td>');
	}
	document.write("</tr>");
}
$(r6c0).removeClass("hidden");
$(r6c0).html("HERO");

//Arrays
pos = [6,0];
prevPos = [6,0];
desPos = [];
moves = [[6,0]];
visited = [[6,0]];
prevPathing = [];
pathing = [];
danger = [];
danger2 = [];
breeze = [];
stench = [];

//Other stuff
gameOver = false;
ref=false;
auto=false;

//Methods
generateWorld();
function resetWorld() {
	pos = [6,0];
	prevPos = [6,0];
	desPos = [];
	moves = [[6,0]];
	visited = [[6,0]];
	prevPathing = [];
	pathing = [];
	danger = [];
	danger2 = [];
	breeze = [];
	stench = [];
	gameOver = false;
	ref=false;
	auto=false;
}
//////////////////////////////// IF THERE ARE NO COMMENTS BELOW THIS LINE, IT'S BECAUSE I RAN OUT OF TIME ////////////////////////////////////////////
function generateWorld() {
	dangerChance = 8;

	g = [Math.round(Math.random()*6),Math.round(Math.random()*6)];
	while(g[1] == 0 || (g[0] == 6 && g[1] == 1)) {
		g = [Math.round(Math.random()*6),Math.round(Math.random()*6)];
	}
	$('#r'+g[0]+'c'+g[1]).prepend("GOLD<br/>");
	for (i=0;i<7;i++) {
		for (q=0;q<7;q++) {
			rand = Math.round(Math.random()*100);
			if (rand >= (100-dangerChance) && ((i!=5 || q != 0) && (i!=6 || q!=1) && (i!=6 || q!=0) && (i!=g[0] || q!=g[1]))) {
				$('#r'+i+'c'+q).prepend("WUMPUS<br/>");
				if (i > 0) $('#r'+(i-1)+'c'+q).prepend("STENCH<br/>");
				if (i < 6) $('#r'+(i+1)+'c'+q).prepend("STENCH<br/>");
				if (q > 0) $('#r'+i+'c'+(q-1)).prepend("STENCH<br/>");
				if (q < 6) $('#r'+i+'c'+(q+1)).prepend("STENCH<br/>");
			} else if (rand >= (100-(dangerChance*2)) && ((i!=5 || q != 0) && (i!=6 || q!=1) && (i!=6 || q!=0) && (i!=g[0] || q!=g[1]))) {
				$('#r'+i+'c'+q).prepend("PIT<br/>");
				if (i > 0) $('#r'+(i-1)+'c'+q).prepend("BREEZE<br/>");
				if (i < 6) $('#r'+(i+1)+'c'+q).prepend("BREEZE<br/>");
				if (q > 0) $('#r'+i+'c'+(q-1)).prepend("BREEZE<br/>");
				if (q < 6) $('#r'+i+'c'+(q+1)).prepend("BREEZE<br/>");
			}
		}
	}
	$('#console').prepend("World generated!<br/>");
}
function move() {
	if (gameOver && !ref) {
		resetPage();
		ref=true;
	} else if (gameOver && ref) {}
	else {
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace("HERO","\r"));
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace(/STENCH/g,"STENCH\r"));
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace(/BREEZE/g,"BREEZE\r"));
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace(/PIT/g,"PIT\r"));
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace(/WUMPUS/g,"WUMPUS\r"));
	$('#r'+pos[0]+'c'+pos[1]).html($('#r'+pos[0]+'c'+pos[1]).text().replace("GOLD","GOLD\r"));
	if (desPos.length > 1 && checkArray(visited,desPos)) {
		$('#console').prepend("desPos = [" + desPos[0] + "," + desPos[1] + "]<br/>");
		if (desPos[0] > pos[0] && checkArray(visited, [pos[0]+1,pos[1]]) && !checkArray(pathing,[pos[0]+1,pos[1]])) {
			moveDown();
		} else if (desPos[0] < pos[0] && checkArray(visited, [pos[0]-1,pos[1]]) && !checkArray(pathing,[pos[0]-1,pos[1]])) {
			moveUp();
		} else if (desPos[1] > pos[1] && checkArray(visited, [pos[0],pos[1] + 1]) && !checkArray(pathing,[pos[0],pos[1] + 1])) {
			moveRight();
		} else if (desPos[1] < pos[1] && checkArray(visited, [pos[0],pos[1] - 1]) && !checkArray(pathing,[pos[0],pos[1] - 1])) {
			moveLeft();
		} else {
			if (checkArray(visited, [pos[0]+1,pos[1]]) && !checkArray(pathing,[pos[0]+1,pos[1]])) {
				moveDown();
			} else if (checkArray(visited, [pos[0]-1,pos[1]]) && !checkArray(pathing,[pos[0]-1,pos[1]])) {
				moveUp();
			} else if (checkArray(visited, [pos[0],pos[1] + 1]) && !checkArray(pathing,[pos[0],pos[1] + 1])) {
				moveRight();
			} else if (checkArray(visited, [pos[0],pos[1] - 1]) && !checkArray(pathing,[pos[0],pos[1] - 1])) {
				moveLeft();
			} else {
				
			}
		}
		pathing.push(pos);
	} else if (desPos.length > 1 && !checkArray(visited,desPos)) {
		if ((desPos[0] > pos[0] && checkArray(visited, [pos[0]+1,pos[1]]) && !checkArray(pathing,[pos[0]+1,pos[1]])) || ((pos[0] + 1) == desPos[0] && pos[1] == desPos[1])) {
			moveDown();
			removeFrom(danger,pos);
			$('#console').prepend("Removed ["+pos[0]+","+pos[1]+"] from danger<br/>");
		} else if ((desPos[0] < pos[0] && checkArray(visited, [pos[0]-1,pos[1]]) && !checkArray(pathing,[pos[0]-1,pos[1]])) || ((pos[0] - 1) == desPos[0] && pos[1] == desPos[1])) {
			moveUp();
			removeFrom(danger,pos);
			$('#console').prepend("Removed ["+pos[0]+","+pos[1]+"] from danger<br/>");
		} else if ((desPos[1] > pos[1] && checkArray(visited, [pos[0],pos[1] + 1]) && !checkArray(pathing,[pos[0],pos[1] + 1])) || ((pos[1] + 1) == desPos[1] && pos[0] == desPos[0])) {
			moveRight();
			removeFrom(danger,pos);
			$('#console').prepend("Removed ["+pos[0]+","+pos[1]+"] from danger<br/>");
		} else if ((desPos[1] < pos[1] && checkArray(visited, [pos[0],pos[1] - 1]) && !checkArray(pathing,[pos[0],pos[1] - 1])) || ((pos[1] - 1) == desPos[1] && pos[0] == desPos[0])) {
			moveLeft();
			removeFrom(danger,pos);
			$('#console').prepend("Removed ["+pos[0]+","+pos[1]+"] from danger<br/>");
		} else {
			if (checkArray(visited, [pos[0]+1,pos[1]]) && !checkArray(pathing,[pos[0]+1,pos[1]])) {
				moveDown();
			} else if (checkArray(visited, [pos[0]-1,pos[1]]) && !checkArray(pathing,[pos[0]-1,pos[1]])) {
				moveUp();
			} else if (checkArray(visited, [pos[0],pos[1] + 1]) && !checkArray(pathing,[pos[0],pos[1] + 1])) {
				moveRight();
			} else if (checkArray(visited, [pos[0],pos[1] - 1]) && !checkArray(pathing,[pos[0],pos[1] - 1])) {
				moveLeft();
			} else {
				pathingReset();
			}
		}
		pathing.push(pos);
	} else {
		if (!checkArray(danger,[(pos[0]-1),pos[1]]) && pos[0] > 0 && !checkArray(visited, [(pos[0]-1),pos[1]])) {
			moveUp();
		} else if (!checkArray(danger,[pos[0],(pos[1]+1)]) && pos[1] < 6 && !checkArray(visited, [pos[0],(pos[1]+1)])) {
			moveRight();
		} else if (!checkArray(danger,[(pos[0]+1),pos[1]]) && pos[0] < 6 && !checkArray(visited, [(pos[0]+1),pos[1]])) {
			moveDown();
		}
		else if (!checkArray(danger,[pos[0],(pos[1]-1)]) && pos[1] > 0 && !checkArray(visited, [pos[0],(pos[1]-1)])) {
			moveLeft();
		} else {
			checkLast();
		}
	}
	$('#console').prepend("Moved to: [" + pos[0] + "," + pos[1] + "]<br/>");
	if (pos.join() == desPos.join()) {
		desPos = [];
	}
	if ($('#r'+pos[0]+'c'+pos[1]).text().search("GOLD") >= 0) {
		$('#console').prepend("<h1>YOU WIN!</h1>");
		$("#movebutton").html("Reset");
		gameOver = true;
		
	}
	if ($('#r'+pos[0]+'c'+pos[1]).text().search("WUMPUS") >= 0) {
		$('#console').prepend("<h1>YOU LOSE! Good day sir!</h1><br/>");
		$("#movebutton").html("Reset");
		gameOver = true;
	}
	if ($('#r'+pos[0]+'c'+pos[1]).text().search("PIT") >= 0) {
		$('#console').prepend("<h1>YOU LOSE! Good day sir!</h1><br/>");
		$("#movebutton").html("Reset");
		gameOver = true;
	}
	if ($('#r'+pos[0]+'c'+pos[1]).text().search("STENCH") >= 0 && !checkArray(visited,pos)) {
		dubs = false;
		if ($('#r'+pos[0]+'c'+pos[1]).text().search("STENCHSTENCH") >= 0)
			dubs = true;
		stench.push(pos);
		$('#console').prepend("Stench at: [" + pos[0] + "," + pos[1] + "]<br/>");
		if (!checkArray(visited,[pos[0]-1,pos[1]]) && pos[0] > 0) {
			if (!checkArray(danger, [pos[0]-1,pos[1]]) && !dubs) {
				danger.push([pos[0]-1,pos[1]]);
				$('#r'+(pos[0]-1)+'c'+pos[1]).removeClass("hidden");
				$('#r'+(pos[0]-1)+'c'+pos[1]).addClass("caution");
			} else if (!checkArray(danger2, [pos[0]-1,pos[1]]) || dubs) {
				if (dubs) danger.push([pos[0]-1,pos[1]]);
				danger2.push([pos[0]-1,pos[1]]);
				$('#r'+(pos[0]-1)+'c'+pos[1]).removeClass("caution");
				$('#r'+(pos[0]-1)+'c'+pos[1]).addClass("danger");
			} 
			$('#console').prepend("Potential Wumpus At: " + "[" + (pos[0]-1) + "," + pos[1] + "]<br/>");
		}
		if (!checkArray(visited,[pos[0]+1,pos[1]]) && pos[0] < 6) {
			if (!checkArray(danger, [pos[0]+1,pos[1]]) && !dubs) {
				danger.push([pos[0]+1,pos[1]]);
				$('#r'+(pos[0]+1)+'c'+pos[1]).removeClass("hidden");
				$('#r'+(pos[0]+1)+'c'+pos[1]).addClass("caution");
			} else if (!checkArray(danger2, [pos[0]+1,pos[1]]) || dubs) {
				if (dubs) danger.push([pos[0]+1,pos[1]]);
				danger2.push([pos[0]+1,pos[1]]);
				$('#r'+(pos[0]+1)+'c'+pos[1]).removeClass("caution");
				$('#r'+(pos[0]+1)+'c'+pos[1]).addClass("danger");
			} 
			$('#console').prepend("Potential Wumpus At: " + "[" + (pos[0]+1) + "," + pos[1] + "]<br/>");
		}
		if (!checkArray(visited,[pos[0],pos[1]-1]) && pos[1] > 0) {
			if (!checkArray(danger, [pos[0],pos[1]-1]) && !dubs) {
				danger.push([pos[0],pos[1]-1]);
				$('#r'+pos[0]+'c'+(pos[1]-1)).removeClass("hidden");
				$('#r'+pos[0]+'c'+(pos[1]-1)).addClass("caution");
			} else if (!checkArray(danger2, [pos[0],pos[1]-1]) || dubs) {
				if (dubs) danger.push([pos[0],pos[1]-1]);
				danger2.push([pos[0],pos[1]-1]);
				$('#r'+pos[0]+'c'+(pos[1]-1)).removeClass("caution");
				$('#r'+pos[0]+'c'+(pos[1]-1)).addClass("danger");
			}
			$('#console').prepend("Potential Wumpus At: " + "[" + pos[0] + "," + (pos[1]-1) + "]<br/>");
		}
		if (!checkArray(visited,[pos[0],pos[1]+1]) && pos[1] < 6) {
			if (!checkArray(danger, [pos[0],pos[1]+1]) && !dubs) {
				danger.push([pos[0],pos[1]+1]);
				$('#r'+pos[0]+'c'+(pos[1]+1)).removeClass("hidden");
				$('#r'+pos[0]+'c'+(pos[1]+1)).addClass("caution");
			} else if (!checkArray(danger2, [pos[0],pos[1]+1]) || dubs) {
				if (dubs) danger.push([pos[0],pos[1]+1]);
				danger2.push([pos[0],pos[1]+1]);
				$('#r'+pos[0]+'c'+(pos[1]+1)).removeClass("caution");
				$('#r'+pos[0]+'c'+(pos[1]+1)).addClass("danger");
			}
			$('#console').prepend("Potential Wumpus At: " + "[" + pos[0] + "," + (pos[1]+1) + "]<br/>");
		}
	}
	if ($('#r'+pos[0]+'c'+pos[1]).text().search("BREEZE") >= 0 && !checkArray(visited,pos)) {
		dubs = false;
		if ($('#r'+pos[0]+'c'+pos[1]).text().search("BREEZEBREEZE") >= 0)
			dubs = true;
		breeze.push(pos);
		$('#console').prepend("Breeze at: [" + pos[0] + "," + pos[1] + "]<br/>");
		if (!checkArray(visited,[pos[0]-1,pos[1]]) && pos[0] > 0) {
			if (!checkArray(danger, [pos[0]-1,pos[1]]) && !dubs) {
				danger.push([pos[0]-1,pos[1]]);
				$('#r'+(pos[0]-1)+'c'+pos[1]).removeClass("hidden");
				$('#r'+(pos[0]-1)+'c'+pos[1]).addClass("caution");
			} else if (!checkArray(danger2, [pos[0]-1,pos[1]]) || dubs) {
				if (dubs) danger.push([pos[0]-1,pos[1]]);
				danger2.push([pos[0]-1,pos[1]]);
				$('#r'+(pos[0]-1)+'c'+pos[1]).removeClass("caution");
				$('#r'+(pos[0]-1)+'c'+pos[1]).addClass("danger");
			}
			$('#console').prepend("Potential Pit At: " + "[" + (pos[0]-1) + "," + pos[1] + "]<br/>");
		}
		if (!checkArray(visited,[pos[0]+1,pos[1]]) && pos[0] < 6) {
			if (!checkArray(danger, [pos[0]+1,pos[1]]) && !dubs) {
				danger.push([pos[0]+1,pos[1]]);
				$('#r'+(pos[0]+1)+'c'+pos[1]).removeClass("hidden");
				$('#r'+(pos[0]+1)+'c'+pos[1]).addClass("caution");
			} else if (!checkArray(danger2, [pos[0]+1,pos[1]]) || dubs) {
				if (dubs) danger.push([pos[0]+1,pos[1]]);
				danger2.push([pos[0]+1,pos[1]]);
				$('#r'+(pos[0]+1)+'c'+pos[1]).removeClass("caution");
				$('#r'+(pos[0]+1)+'c'+pos[1]).addClass("danger");
			} 
			$('#console').prepend("Potential Pit At: " + "[" + (pos[0]+1) + "," + pos[1] + "]<br/>");
		}
		if (!checkArray(visited,[pos[0],pos[1]-1]) && pos[1] > 0) {
			if (!checkArray(danger, [pos[0],pos[1]-1]) && !dubs) {
				danger.push([pos[0],pos[1]-1]);
				$('#r'+pos[0]+'c'+(pos[1]-1)).removeClass("hidden");
				$('#r'+pos[0]+'c'+(pos[1]-1)).addClass("caution");
			} else if (!checkArray(danger2, [pos[0],pos[1]-1]) || dubs) {
				if (dubs) danger.push([pos[0],pos[1]-1]);
				danger2.push([pos[0],pos[1]-1]);
				$('#r'+pos[0]+'c'+(pos[1]-1)).removeClass("caution");
				$('#r'+pos[0]+'c'+(pos[1]-1)).addClass("danger");
			}
			$('#console').prepend("Potential Pit At: " + "[" + pos[0] + "," + (pos[1]-1) + "]<br/>");
		}
		if (!checkArray(visited,[pos[0],pos[1]+1]) && pos[1] < 6) {
			if (!checkArray(danger, [pos[0],pos[1]+1]) && !dubs) {
				danger.push([pos[0],pos[1]+1]);
				$('#r'+pos[0]+'c'+(pos[1]+1)).removeClass("hidden");
				$('#r'+pos[0]+'c'+(pos[1]+1)).addClass("caution");
			} else if (!checkArray(danger2, [pos[0],pos[1]+1]) || dubs) {
				if (dubs) danger.push([pos[0],pos[1]+1]);
				danger2.push([pos[0],pos[1]+1]);
				$('#r'+pos[0]+'c'+(pos[1]+1)).removeClass("caution");
				$('#r'+pos[0]+'c'+(pos[1]+1)).addClass("danger");
			}
			$('#console').prepend("Potential Pit At: " + "[" + pos[0] + "," + (pos[1]+1) + "]<br/>");
		}
	}
	if (moves[moves.length-1].join() != pos.join())
		moves.push(pos);
	if (!checkArray(visited,pos))
		visited.push(pos);
		
	$('#r'+pos[0]+'c'+pos[1]).removeClass("hidden");
	$('#r'+pos[0]+'c'+pos[1]).removeClass("caution");
	$('#r'+pos[0]+'c'+pos[1]).removeClass("danger");
	$('#r'+pos[0]+'c'+pos[1]).append("HERO");
	} 
}
function moveLeft() {
	pos = [pos[0],pos[1]-1];
}
function moveRight() {
	pos = [pos[0],pos[1]+1];
}
function moveUp() {
	pos = [pos[0]-1,pos[1]];
}
function moveDown() {
	pos = [pos[0]+1,pos[1]];
}
function checkArray(array,value) {
	for (i=0; i < array.length; i++) {
		if (array[i].join() == value.join()) {
			return true;
			break;
		} 
	}
	return false;
}
function getAll(array) {
	a="";
	for (i=0; i < array.length; i++) {
		a+=array[i]+"\n";
	}
	return a;
}
function checkLast() {
	try {
	$('#console').prepend("checkLast() run!<br/>");
	prevIndex = 1;
	pathingReset();
	while (desPos.length < 1) {
		lpos = moves[moves.length - prevIndex];
		if (!checkArray(danger,[(lpos[0]-1),lpos[1]]) && lpos[0] > 0 && !checkArray(visited, [(lpos[0]-1),lpos[1]])) {
			desPos = lpos;//[lpos[0]-1,lpos[1]];
			$('#console').prepend("desPos set! desPos = [" + desPos[0] + "," + desPos[1] + "]<br/>");
		} else if (!checkArray(danger,[lpos[0],(lpos[1]+1)]) && lpos[1] < 6 && !checkArray(visited, [lpos[0],(lpos[1]+1)])) {
			desPos = lpos;//[lpos[0],lpos[1]+1];
			$('#console').prepend("desPos set! desPos = [" + desPos[0] + "," + desPos[1] + "]<br/>");
		} else if (!checkArray(danger,[(lpos[0]+1),lpos[1]]) && lpos[0] < 6 && !checkArray(visited, [(lpos[0]+1),lpos[1]])) {
			desPos = lpos;//[lpos[0]+1,lpos[1]];
			$('#console').prepend("desPos set! desPos = [" + desPos[0] + "," + desPos[1] + "]<br/>");
		} else if (!checkArray(danger,[lpos[0],(lpos[1]-1)]) && lpos[1] > 0 && !checkArray(visited, [lpos[0],(lpos[1]-1)])) {
			desPos = lpos;//[lpos[0],lpos[1]-1];
			$('#console').prepend("desPos set! desPos = [" + desPos[0] + "," + desPos[1] + "]<br/>");
		} else if (prevIndex == moves.length) {
			$('#console').prepend("Trying a random danger zone!<br/>");
			//if (danger2.length >= danger.length) 
				//pickRandomRed();
			//else
				pickRandom();
			break;
		} else {
			prevIndex++;
			$('#console').prepend("Checking [" + lpos[0] + "," + lpos[1] + "]<br/>");
			
		}
	}
	}
	catch (e) {
		console.log("ERROR: " + e);
	}
	
}
function pickRandom() {
	try {
	i=0;
	randSpace = danger[Math.round(Math.random() * (danger.length-1))];
	while (checkArray(danger2,randSpace) || checkArray(visited, randSpace)) {
		randSpace = danger[Math.round(Math.random() * (danger.length-1))];
		i++;
	}
	$('#console').prepend("Random danger zone at: [" + randSpace[0] + "," + randSpace[1] + "]<br/>");
	pathingReset();
	desPos = randSpace;
	} catch (e) {
		console.log("ERROR: " + e);
	}
}
function pickRandomRed() {
	$('#console').prepend("Will this run?");
	randSpace = danger2[Math.round(Math.random() * (danger2.length-1))];
	/*while(checkArray(visited,randSpace)) {
		randSpace = danger2[Math.round(Math.random() * (danger2.length-1))];
	}*/
	$('#console').prepend("Random RED danger zone at: [" + randSpace[0] + "," + randSpace[1] + "]<br/>");
	pathingReset();
	desPos = randSpace;
}
function resetPage() {
	window.location.reload();
}
function pathingReset() {
	try {
	if (prevPathing.join() == pathing.join() && pathing.length > 1) {
		$('#console').prepend("STUCK IN A LOOP!<br/>");  
	}
	$('#console').prepend("RESETTING PATHING!<br/>");
	prevPathing = pathing;
	pathing = [];
	pathing.push(pos);
	} catch (e) {
		console.log("ERROR: " + e);
	}
}
function removeFrom(array, value) {
	for(var i = 0; i < array.length; i++) {
		if (array[i].join() == value.join()) {
			array.splice(i,1);
			break;
		}
	}
}
function autoRun() {
	auto=true;
}
</script>
</table>
<br/>
<button onclick="move();" id="movebutton">Next Move</button>
<button onclick="autoRun();" id="movebutton">Auto Run</button>
</div>
</body>
</html>