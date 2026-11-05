The code for the game is here
Please use the code tab instead


HTML

<div style="text-align: center; padding-top: 100px; position: relative; width: 400px; margin: 0 auto; height: 400px;">
  
  <img id="player-1down" src="https://github.com/neelanshsha-wq/tag-assets/blob/main/Untitled%20design%20(2).png?raw=true" alt="My Image" width="400" style="position: absolute; top: 0; left: 0;">
  
  <img id="player-2down" src="https://github.com/neelanshsha-wq/tag-assets/blob/main/Untitled%20design%20(4).png?raw=true" alt="My Image" width="400" style="position: absolute; top: 0; left: 0; display: none;">
  
  <img id="player-3down" src="https://raw.githubusercontent.com/neelanshsha-wq/tag-assets/refs/heads/main/Untitled%20design%20(5).png" alt="My Image" width="400" style="position: absolute; top: 0; left: 0; display: none;">
  
</div>

CSS

img {
  display: inline-block;
  margin: 0 auto;
  
}


JavaScript


document.getElementById("player-1down").style.display="none";
document.getElementById("player-2down").style.display="block";
document.getElementById("player-3down").style.display="none";
let isWalking = 1

window.addEventListener('keydown', function(){
// starting checking code
if (isWalking === 1) {
document.getElementById("player-2down").style.display="none";
isWalking = 0
document.getElementById("player-1down").style.display="block";
setTimeout(function() {
document.getElementById("player-1down").style.display="none";
document.getElementById("player-3down").style.display="block";
setTimeout(function() {
document.getElementById("player-3down").style.display="none";
isWalking = 1;
}, 200);
}, 200);
}
});
window.addEventListener('keyup', function(){
document.getElementById("player-1down").style.display="none";
document.getElementById("player-2down").style.display="block";
document.getElementById("player-3down").style.display="none";
});
