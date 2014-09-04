
<html>
<head>
<meta charset="utf-8">
<title>Untitled Document</title>
<style> 

span {
  display: inline-block;
  opacity: 0;
  transition: 2s;
}

body {
  padding: 50px;
  font-family: 'Bubblegum Sans', cursive;
  font-size: 32px;
}

</style>
<script type="text/javascript" src="jquery-1.7.2.min.js" > </script>
<script type="text/javascript"> 

$(document).ready(function(e) {
    function getRandomInt(min, max) {
	  return Math.floor(Math.random() * (max - min + 1)) + min;
	}
	var arr = [];
	$(".pg").each(function(e) {
	
	  var text = $(this).html();
	  arr.push(text);
	  var words = text.split(" ");
	  var spanSentence = "";
	  for (var i = 0; i < words.length; i++) {
		  $(words[i]).css('color','#F8060A');
		spanSentence += "<span>" + words[i] + "</span> ";
	  }
	  $(this).html(spanSentence);
	})
	
	$(".pg span").each(function() {
	  $(this)
		.css({
		  "transform": "translate(" + getRandomInt(-100, 100) + "px, " + getRandomInt(-100, 100) + "px)"
		})
	});
	
	setTimeout(function() {
	  $(".pg:nth-child(1) span").css({
		"transform": "translate(0, 0)",
		"opacity": 1
	  });
	}, 50);
	
	setTimeout(function() {
	  $(".pg:nth-child(2) span").css({
		"transform": "translate(0, 0)",
		"opacity": 1
	  });
	}, 3050);
	
	setTimeout(function() {
	  $(".pg:nth-child(3) span").css({
		"transform": "translate(0, 0)",
		"opacity": 1
	  });
	}, 6050);
	
	
	setTimeout(function(){
		
		for(var i=0;i<arr.length;i++){
			document.getElementsByClassName('pg')[i].innerHTML	= arr[i];
		}
		
		/*var b = document.getElementsByTagName('span');
		while(b.length) {
			var parent = b[ 0 ].parentNode;
			while( b[ 0 ].firstChild ) {
				parent.insertBefore(  b[ 0 ].firstChild, b[ 0 ] );
			}
			parent.removeChild( b[ 0 ] );
		}
		
		var temp = document.getElementsByClassName('pg').innerHTML;
		var str2 = temp.replaces(/(\r\n|\n|\r)/gm," ");
		alert(str2)
		document.getElementsByClassName('pg').innerHTML = str2;*/
		
	}, 10000);
});
</script>



</head>

<body>

<p class="pg">I'll sing you a poem of a silly young king
Who played with the world at the end of a string,
But he only loved one single thing—
  And that was just a peanut-butter sandwich.</p>

<p class="pg">His scepter and his royal gowns,
His regal throne and golden crowns
Were brown and sticky from the mounds
And drippings from each peanut-butter sandwich.</p>

<p class="pg">His subjects all were silly fools
For he had passed a royal rule
That all that they could learn in school
Was how to make a peanut-butter sandwich.</p>

</body>
</html>
