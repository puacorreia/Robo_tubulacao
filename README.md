<h1 align="center">
  Robô Limpador de tubulações 🤖
</h1>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/puacorreia/Robo_tubulacao">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/puacorreia/Robo_tubulacao">
  
  <a href="https://github.com/puacorreia/Robo_tubulacao/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/puacorreia/Robo_tubulacao">
  </a>

   <a href="https://github.com/puacorreia/Robo_tubulacao/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/puacorreia/Robo_tubulacao?style=social">
  </a>
</p>

<div align="center">
  <img src="https://github.com/puacorreia/Robo_tubulacao/assets/86266893/36e703c9-07b0-4045-b72d-4f5bee6d4fa1" alt"Mapa">
</div>

<br>

<p align="center">
 <a href="#-sobre">Sobre</a> | 
 <a href="#-como-funciona">Como funciona</a> | 
 <a href="-preview">Preview</a> |
 <a href="#-autores">Autores</a>
</p>


## 💻 Sobre

Deseja-se construir o controlador de um `robô` capaz de `remover detritos não metálicos de uma tubulação metálica`. A figura acima ilustra o problema.

---

## ❓ Como funciona 

A tubulação a ser percorrida corresponde aos componentes de uma matriz de células, indicados pela cor cinza. O robô, mostrado como uma seta, é colocado em uma célula da cor preta, a qual representa um ponto de acesso do sistema de tubulação, com sua frente voltada para qualquer um dos 4 sentidos possíveis (Norte, Sul, Leste ou Oeste).
O robô possui 4 sensores binários:
- head (H): detector de metal de curto alcance, situado na frente do robô (ponta da seta), que
retorna 0 quando a célula situada à frente do robô está livre para prosseguir (célula cinza ou
preta) – caso contrário, retorna 1;

- left (L): detector de metal de curto alcance, situado na lateral esquerda do robô, que retorna 0
quando a célula do lado esquerdo do robô está livre (ou seja, há uma abertura à esquerda na
tubulação) – caso contrário, retorna 1;

- under (U): sensor situado na parte inferior do robô, que retorna 1 quando a célula na qual o robô
está situado é preta – caso contrário, retorna 0;

- barrier (B): sensor situado na frente do robô, que retorna 1 quando a célula situada à frente do
robô está bloqueada por algum entulho que o robô é capaz de remover (células com losango) –
caso contrário, retorna 0.

Em relação à movimentação, o robô é capaz de fazer apenas 2 tipos de movimento: avançar para uma célula livre à sua frente **(saída F)** ou rotacionar 90o para a esquerda, mantendo-se na mesma célula em que se encontra **(saída T)**. Cada movimento consome 1 pulso de clock. Ao passar de uma célula livre para uma célula preta ou, ainda, em casos anômalos, o robô deverá ficar suspenso **(em stand-by)**, até que um novo reset seja dado. Ao deparar-se com algum entulho à sua frente, o robô consumirá ao menos 3 pulsos de clock para removê-lo **(saída R)**, após o que poderão ocorrer duas situações: i) caso reste algum entulho, o robô fará novo ciclo de remoção (3 pulsos) e testará a condição de caminho livre novamente; ii) caso o caminho esteja livre (não há mais entulho na célula considerada), o robô entrará em movimento novamente, avançando sobre o setor antes ocupado pelo entulho. O robô deverá ser capaz de percorrer toda a tubulação de forma otimizada, adotando sempre o mesmo critério em todas as bifurcações, qual seja, adotar o lado esquerdo como preferencial.

---

## Preview 📸

### Finite Machine State (FSM)
  ![image](https://github.com/puacorreia/Robo_tubulacao/assets/86266893/dc124425-40c0-4308-a08b-023dcd0be6f0)

### Tabela
  <div align="center">
    <img src="https://github.com/puacorreia/Robo_tubulacao/assets/86266893/bac5fe19-9527-447a-9b76-f2266f0a7225" />
  </div>

---

## ✍ Autores 
<div>
  <img alt="Perfil Github" title="Perfil Github" src="https://github.com/RuanCxrdoso.png" width="100px" />
</div>
<br>
<div>
  <img alt="Perfil Github" title="Perfil Github" src="https://github.com/MiCorreia.png" width="100px" />
</div>
<br>
<div>
  <img alt="Perfil Github" title="Perfil Github" src="https://github.com/Edilton-Damasceno.png" width="100px" />
</div>

<br>
