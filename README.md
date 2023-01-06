# notaatletas
classificação atletas e nome
// DeverÃ¡ apresentar ao usuÃ¡rio o nome de cada atleta, seguido das notas e da mÃ©dia calculada.
//Utilize a seguinte entrada:


let atletas = [
 {
   nome: "Cesar Abascal",
   notas: [10, 9.34, 8.42, 10, 7.88]
 },
 {
   nome: "Fernando Puntel",
   notas:  [8, 10, 10, 7, 9.33]
 },
 {
   nome: "Daiane Jelinsky",
   notas: [7, 10, 9.5, 9.5, 8]
 },
 {
   nome: "Bruno Castro",
   notas: [10, 10, 10, 9, 9.5]
 }
];
// Permite comparar os valores da matriz, ordenar do maior para o menor
function compare(a,b) {return a - b;};
// LaÃ§o for para percorrer todos os itens da matriz de objetos
for (let i = 0; i < atletas.length; i++) {
// variável valor zero
  let valor = 0;   
  let soma = 0;
  atletas[i].notasComputadas = atletas[i].notas;
// Utilizar o mÃ©todo .slice(x, y) para ajudar na seleÃ§Ã£o dos valores e o mÃ©todo .sort() para ordenar as matrizes:
  atletas[i].notasComputadas = atletas[i].notasComputadas.sort(compare).slice(1,4);
//Classificando a matriz em ordem crescente.
 atletas[i].notasComputadas.map(function(notas) {
   soma = soma + notas;
 });
 // O valor da variÃ¡vel Ã© usado para calcular a mÃ©dia.
    valor = (soma / atletas[i].notasComputadas.length)
// Para imprimir os resultados.
console.log("\nAtleta: " + atletas[i].nome + "\nNotas: " + atletas[i].notas + "\nMÃ©dia Calculada: " + valor);
};
