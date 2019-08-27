# autoGoodPigg
its a Bookmarklet.  
Go to <https://s.pigg.ameba.jp/area/good>  
And run this.
```javascript
javascript:if (location.href != "https://s.pigg.ameba.jp/area/good") {
	location.href = "https://s.pigg.ameba.jp/area/good"
} else {
	document.body.innerHTML =
		" <style>html,body { width: 100%; height: 100%; background-color : #393939; }</style> <style>body { position:absolute !important; left:10% !important; width: 80%; height: 100%; background-color : #393939; }</style> <div style= ' position:absolute !important; top:10% !important; left:10% !important; width: 80%; height: 80%; text-align:center; background: rgba(0, 0, 0, 0.5); -webkit-border-radius: 10px; -moz-border-radius: 10px; border: 1px solid #000; '> <div style= ' margin: 20px auto; color:White; font-size:20px; '>Auto Good Pigg</div> <iframe name= 'f' src = 'https://s.pigg.ameba.jp/area/good' onload = 'run()' style = ' position:relative; top:50%; width: 80%; height: 80%; border: 1px solid #000; '></iframe></div>";
	c = 0;

	function run() {
		if (f.document.getElementsByClassName("goodpigg").length < 102) {
			f.document.getElementById("goodpigg-area-more-button").click();
			setTimeout("run()", 100)
		} else if (f.document.getElementsByClassName("goodpigg").length - f.document.getElementsByClassName(
				"done").length != 0) {
			f.document.getElementsByClassName("goodpigg")[c].click();
			c++;
			setTimeout("run()", 100)
		} else {
			c = 0;
			f.location.reload()
		}
	}
}
```
# Demo
<img src="https://user-images.githubusercontent.com/8677536/63814761-eeb4fb80-c96c-11e9-982c-dc3122079a6b.gif">
