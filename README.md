# **Poke-Projeto-COCADA**
Projeto final individual da disciplina de Computação Científica e Análise de Dados de Vinícius Leoni


### **AUTOR**
- Vinícius Leoni Gonçalves - DRE: _*121083446*_
- _*Menção honrosa para Ian Mascaro, que fez dupla com o autor deste, no [__projeto final da disciplina de Algebra Linear Algorítmica__](___https://github.com/ViniciusLeoniGoncalves/Poke-Projeto-ALA___), a base temática utilizada para a construção deste trabalho.*_


## **BEM-VINDO, TREINADOR!**
***
Aqui faremos uma análise de todos os pokémons até a 4° geração com foco em montar um time de 6 que seja capaz de enfrentar a grande campeã da região de Sinnoh, a temida Cynthia!

O objetivo desta ferramenta é ajudar treinadores a identificar os Pokémon cujos status base são mais semelhantes ao estilo que se quer impor contra a campeã. O cálculo leva em conta ****os status base de todos os pokemons**** e também ****suas tipagens****, possibilitando assim, o treinador montar um time capaz de enfrentar a Cynthia imprimindo um  _*estilo de jogo*_ e uma _*vantagem de tipo*_ ao mesmo tempo.

## **Resumo do que será feito**
***
- Vamos analisar o time da cynthia, olhando monstro a monstro e vendo seus status e tipagens, mostrando ao usuário.
    - Usarei o time da Cynthia de Pokemon Diamond/Pearl nessa análise, ele consiste em:
        Roserade lvl 60
        Gastrodon lvl 60
        Spiritomb lvl 61
        Milotic lvl 63
        Lucario lvl 63
        Garchomp lvl 66
- Depois, escolher um estilo de luta, vou escolher o estilo "Blitzkrieg" que consiste em ganhar dos monstros da cynthia na velocidade, e acertar duros golpes (Ataque basico ou especial, vai depender do que é mais efetivo no monstro dela) ****COM VANTAGEM DE TIPO****, para que ela quase não tenha chances de revidar.
***
- Posto isso, a parte de COCADA consiste em extrair todos os pokemons até a gen4 via pokeapi, guardar os dados de: $\begin{bmatrix} nome && sprite && tipo 1 && tipo 2 && HP (base) && Attack (base) && Defense (base) && SpAtk (base) && SpDef (base) && Speed (base) \end{bmatrix}$ nas colunas de uma matriz.

Essa estrutura será nossa base de dados principal, uma matriz onde cada linha representa um Pokémon e cada coluna representa uma característica relevante do ponto de vista de combate

_*técnicas de análise:*_
- Primeiro fazer um PCA e reduzir os vetores Status de pokemons para 2 dimensões.

- Visualização e interpretação do resultado dos PCAs

- Com base na observação dos PCAs, realizar uma clusterização de pokemons focando no grupo blitzkrieg


## **O que faremos aqui em termos técnicos é:**

- extrair a matriz com os vetores de status do pokeAPI
- Fazer PCA1 e PCA2 nela para procurar visualizar um grupo Blitzkrieg
- clusterizar pensando em achar um grupo blitzkrieg
- olhar os monstros da cynthia 1 a 1 e escolher, dentro do cluster blitzkrieg, o que tem mais vantagem de tipo contra ele