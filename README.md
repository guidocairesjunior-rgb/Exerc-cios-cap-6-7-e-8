# Exercícios JavaScript Resolvidos (6, 7 e 8)

Este repositório contém as soluções corrigidas e otimizadas para a lista de exercícios de JavaScript.

---

## 📋 Lista de Exercícios

### Exercício 1 - Comprinhas Online
Calcula o valor total dos produtos somado ao frete de acordo com a cidade de destino.

```javascript
function calculaValorTotalDaCompra(produtos, cidade, caixa, fretes) {
  let total = 0;
  produtos.forEach(function(produto) {
    total += caixa[produto] || 0;
  });
  total += fretes[cidade] || fretes["Outros"];
  return total;
}

const caixa = {
  "Arroz": 7.10,
  "Feijão": 2.30,
  "Macarrão": 4.70,
  "Refrigerante": 3.00
};

const fretes = {
  "São Paulo": 10.10,
  "Rio de Janeiro": 12.30,
  "Brasília": 14.70,
  "Outros": 13.00
};

console.log(
  calculaValorTotalDaCompra(["Arroz"], "São Paulo", caixa, fretes)
);
// Saída esperada: 17.20