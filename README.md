## Dígito Verificador CPF

#### Objetivo: 

Com base nos 9 primeiros dígitos inseridos pelo usuário realizar a verificação se esses dígitos são válidos e após isso mostrar os dos últimos dígitos do CPF de qualquer pessoa.

Dessa forma o usuário deverá conseguir:

* Navegar pelo MENU do algoritmo e selecionar três opções: Validar o CPF, Informações do Desenvolvedor e Sair do Algoritmo.
* Ao selecionar a opção de validar o CPF o usuário deverá conseguir inserir os 9 primeiros dígitos do seu CPF e após isso receber a informação se esse CPF é válido e caso seja válido deverá retornar os 9 primeiros dígitos do CPF mais os 2 últimos dígitos, também conhecido como "Dígitos Verificadores".
* Ao selecionar a opção de "Informações do Desenvolvedor", o usuário deverá receber o nome completo e a matrícula.
* Ao selecionar a opção "Sair do Algoritmo", o algoritmo deverá parar de funcionar.



#### Solução:

O algoritmo foi desenvolvido em Java com a seguinte lógica:

```
Etapa 1: cálculo de DV1
Soma 1: soma dos produtos de cada dígito por um peso de 2 a 10, na ordem inversa (do nono
para o primeiro). Multiplique a “Soma 1” por 10 e calcule o resto da divisão do resultado por 11.
Se der 10, DV1 é zero, caso contrário o DV1 é o próprio resto.
Etapa 2: cálculo de DV2
Soma 2: soma dos produtos de cada dígito por um peso de 3 a 11, também na ordem inversa.
Adicione a “Soma 2” ao dobro do DV1, multiplique por 10 e calcule o resto da divisão do resultado
por 11. Se der 10, DV2 é zero, caso contrário o DV2 é o próprio resto.
Etapa 3: Multiplique DV1 por 10, some com DV2 e você tem o número de controle do CPF.
```