function setup() {
  createCanvas(400, 400);
}
let xJogador1 = 0;
let xJogador2 = 0;

function draw() {
  ativaJogo();
  desenhaJogadores();
  desenhaLinhaDeChegada();
  verificarJogador();
}
  
 function ativaJogo() {
  if(focused== true)  {
 background(220);
 } else { background(" rgb(238,178,178)" )
        }
 } 
   
function desenhaJogador(){
    textSize(40);
  text("🥱", xJogador1, 100);
  text("🥸", xJogador2, 150);
}
  rect(350, 0, 10, 400);
  xJogador1 = xJogador1 + random(5);
  xJogador2 = xJogador2 + random(5);

  if (xJogador1 > 350) {
    text("Jogador 1 VENCEU!", 20, 200);
    noLoop();
  }

  if (xJogador2 > 350) {
    text("Jogador 2 VENCEU!", 20, 200);
    noLoop();
   
  }