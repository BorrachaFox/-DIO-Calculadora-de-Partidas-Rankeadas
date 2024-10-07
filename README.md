# DIO CALCULADORE DE PARTIDAS RANKEADAS

Este projeto é uma calculadora de partidas ranqueadas, que calcula o saldo de vitórias e derrotas de um herói e determina seu nível ranqueado com base nesse saldo.

1. **Cálculo do saldo de vitórias**: 
   - A função `calculaSaldoVitorias` recebe o número de vitórias e derrotas e calcula o saldo:
     ```javascript
     const calculaSaldoVitorias = (vitorias, derrotas) => {
        return vitorias - derrotas;
     };
     ```
   
2. **Classificação do herói por saldo**:
   - A função `rankDoHeroi` recebe o saldo de vitórias e retorna o nível ranqueado do herói, de acordo com as faixas estabelecidas. Os níveis incluem:
     - **Ferro**: saldo menor que 10
     - **Bronze**: saldo entre 11 e 20
     - **Prata**: saldo entre 21 e 50
     - **Ouro**: saldo entre 51 e 80
     - **Diamante**: saldo entre 81 e 90
     - **Lendário**: saldo entre 91 e 100
     - **Imortal**: saldo acima de 101
    
## Exemplo de Uso

Aqui está um exemplo de como calcular o saldo e determinar o nível do herói:

```javascript
let saldoVitorias = calculaSaldoVitorias(157, 58);
let nivel = rankDoHeroi(saldoVitorias);

console.log(`O Herói tem de saldo de ${saldoVitorias} e está no nível de ${nivel}`);
