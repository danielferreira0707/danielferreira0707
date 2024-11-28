let campoIdade;
let campoterror;
let campocomedia;

function setup() {
  createCanvas(800, 400);
  createElement("h2", "Recomendador de filmes");
  createSpan("Sua idade:");
  campoIdade = createInput("5");
  campoterror = createCheckbox("Gosta de Terror?");
  campocomedia = createCheckbox("Gosta de Comedia?");
}

function draw() {
  background("black");
  let idade = campoIdade.value();
  let gostaDeTerror = campoTerror.checked();
  let gostaDeComedia = campoAventura.checked();
  let recomendacao = geraRecomendacao(idade, gostaDeTerror, gostaDeComedia);

  fill(color(76, 0, 115));
  textAlign(CENTER, CENTER);
  textSize(38);
  text(recomendacao, width / 2, height / 2);
}

function geraRecomendacao(idade, gostaDeTerror, gostaDeComedia) {
  if (idade >= 16) {
    if (idade >= 14) {
      return "O vazio";
    } else {
      if (idade >= 16) {
        if(gostaDeTerror || gostaDeComedia) {
          return "o poço";          
        } else{
         return "se beber não case";
        }
      } else {
        if (gostaDTerror) {
          return "O Chamado";
        } else {
          return "Lupin";
        }
      }
    }
  } else {
    if (gostaDeterror) {
      return "Ponico";
    } else {
      return "Ronaldo";
    }
  }
}
