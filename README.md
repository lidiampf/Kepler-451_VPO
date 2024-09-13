# Análise da Variação do Período Orbital de Kepler-451: Candidato a sistema multiplanetário em uma configuração circumbinária

Lídia Maria Peregrino de Faria $^{1,*}$, João Victor Ferreira Lacerda Aires $^{1,\dagger}$, and Leonardo Andrade de Almeida $^{2,\ddagger}$.

$^{1}$ Departamento de Física, Universidade Federal do Rio Grande do Norte. \
$^{2}$ Escola de Ciência & Tecnologia, Universidade Federal do Rio Grande do Norte.

\* [lidiampf@hotmail.com](mailto:lidiampf@hotmail.com) \
$\dagger$ [joaovictor.jvic@gmail.com](mailto:joaovictor.jvic@gmail.com) \
$\ddagger$ [leonardo.almeida@ufrn.br](mailto:leonardo.almeida@ufrn.br)

## Resumo

Este repositório foi criado a fim de demonstrar a metodolodia usada na dissertação apresentada por Lídia Peregrino ao Programa de Pós-Graduação em Física, da Universidade Federal do Rio Grande do Norte, como requisito parcial à obtenção do título de Mestre em Física, intitulada ``Análise da Variação do Período Orbital de Kepler-451: Candidato a sistema multiplanetário em uma configuração circumbinária''.

Este código busca investigar a variação do período orbital da binária pós-envelope comum *sdB+dM* eclipsante destacada, Kepler-451, através do método Monte Carlo via Cadeia de Markov (*MCMC*) adaptado para o *Stretch Move* ([Goodman & Weare, 2010](https://msp.org/camcos/2010/5-1/camcos-v5-n1-p04-s.pdf)).

### Algoritmo Stretch Move

Usamos o algoritmo *Stretch Move* neste trabalho para propor novos valores de parâmetros por cadeias de Markov paralelas simultâneas (*walkers*). Nessa variação de *MCMC*, os *walkers* evoluem de forma que a direção da distribuição proposta para um determinado *walker* depende apenas da posição do conjunto de parâmetros atual e não dos anteriores. A aceitação (ou rejeição) dessas propostas é governada pela probabilidade a posteriori, preservando as propriedades fundamentais do *MCMC*.

As vantagens do *Stretch Move* são a simplicidade,  a eficiência computacional e a rápida convergência para a distribuição posterior correta, mesmo em situações com parâmetros quase colineares ou distribuições multimodais. Sendo assim, recomendado para análises de dados complexos, como sistemas planetários com interações gravitacionais observáveis.

Implementamos este método visando ajustar a efeméride linear dos instantes dos meios dos eclipses, ajustados pelo modelo WD+PIKAIA e convertidos para *BJD*, somatizada à contribuição do ETL (equação não linear), atribuída por corpos extras ligados gravitacionalmente ao sistema estudado. Essa abordagem visa investigar possíveis variações no seu período orbital.
