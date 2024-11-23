**Aluno: Albert França**

**Turma: 109**

---
## 1. Função ```verificarIdade```

```javascript
function verificarIdade(idade) {
    if (idade < 18) {
        return "Menor de idade";
    } else {
        return "Maior de idade";
    }
}

console.log(verificarIdade(15));
console.log(verificarIdade(18)); 
console.log(verificarIdade(21));
```

 - A função ```verificarIdade``` recebe um parâmetro idade.
 - Utiliza uma estrutura condicional ```(if-else)``` para verificar se a idade é menor que 18:
    - Retorna `"Menor de idade"` se for menor que `18`.
    - Caso contrário, retorna `"Maior de idade"`.
 - Testamos a função com os valores `15`, `18` e `21`.

---

## 2. Função ```definirDiaDaSemana```

```javascript
function definirDiaDaSemana(numero) {
    switch (numero) {
        case 1:
            return "Domingo";
        case 2:
            return "Segunda-feira";
        case 3:
            return "Terça-feira";
        case 4:
            return "Quarta-feira";
        case 5:
            return "Quinta-feira";
        case 6:
            return "Sexta-feira";
        case 7:
            return "Sábado";
        default:
            return "Número inválido";
    }
}

console.log(definirDiaDaSemana(3));
console.log(definirDiaDaSemana(7));
console.log(definirDiaDaSemana(8));
```

 - A função `definirDiaDaSemana` recebe um número como parâmetro.
 - Utiliza a estrutura ```switch-case``` para mapear números de `1` a `7` para os dias da semana:
   - Retorna o dia correspondente (ex.: `1` para `"Domingo"`).
   - Para números fora do intervalo, o `default` retorna `"Número inválido"`.
 - Testamos com os valores `3`, `7` e `8`.

---

## 3. Função ```parOuImpar```

```javascript
function parOuImpar(numero) {
    return numero % 2 === 0 ? "Par" : "Ímpar";
}

console.log(parOuImpar(10));
console.log(parOuImpar(15));
console.log(parOuImpar(22));
```

 - A função `parOuImpar` utiliza o operador ternário para verificar se o número é par:
    - `numero % 2 === 0` verifica se o número é divisível por 2.
    - Retorna `"Par"` se a condição for verdadeira, e `"Ímpar"` caso contrário.
 - Testamos com os valores `10`, `15` e `22`.

---

## 4. Função `podeAcessar`

```javascript
function podeAcessar(usuario) {
    return ((usuario.idade > 18 || usuario.isAdmin) && !usuario.isBlocked);
}

console.log(podeAcessar({ idade: 20, isAdmin: false, isBlocked: false }));
console.log(podeAcessar({ idade: 16, isAdmin: true, isBlocked: true }));
```

 - A função podeAcessar verifica duas condições:
    - O usuário deve ser maior de 18 anos (`usuario.idade > 18`) OU ser administrador (`usuario.isAdmin`).
    - A conta do usuário não pode estar bloqueada (`!usuario.isBlocked`).
 - A lógica é implementada com operadores lógicos:
    - `||` verifica se o usuário atende a pelo menos uma das condições de acesso.
    - `&&` garante que a conta não esteja bloqueada.
 - Testamos com:
    - `{ idade: 20, isAdmin: false, isBlocked: false }:` Acesso permitido (true).
    - `{ idade: 16, isAdmin: true, isBlocked: true }:` Acesso negado (false).

---

## 5. Função `calcularDesconto`

```javascript
const calcularDesconto = (precoOriginal, porcentagemDesconto) =>
    precoOriginal - (precoOriginal * (porcentagemDesconto / 100));

console.log(calcularDesconto(100, 10));
console.log(calcularDesconto(250, 20));
```

 - A função `calcularDesconto` calcula o preço final após aplicar um desconto:
    - O desconto é obtido com a fórmula: `precoOriginal * (porcentagemDesconto / 100)`.
    - O preço final é: `precoOriginal - desconto`.
 - A função é uma arrow function para ser mais concisa.
 - Testamos com:
    - Preço `100` e desconto `10%`: Retorna `90`.
    - Preço `250` e desconto `20%`: Retorna `200`.

