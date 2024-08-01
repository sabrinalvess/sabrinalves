let palavra;

function setup() {
  createCanvas(400, 400);

  palavra = palavraAleatoria();

}

function palavraAleatoria() {
  
  let palavras = ["hello kitty", "moranguinho", "coquette"];
  
  return random(palavras);
}

function inicializaCores() {
  background("rgb(255,255,255)");
  fill("#F5BED0");
  textSize(64);
  textAlign(CENTER, CENTER);
}

function palavraParcial(minimo, maximo) {
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);
  let parcial = palavra.substring(0, quantidade);
  return parcial;
}

function draw() {
  
  inicializaCores();

  let parcial = palavraParcial(0, width);
    
  text(parcial, 200, 200);
  
}
