# Análise da Variação do Período Orbital de Kepler-451
 
Este código busca investigar a variação do período orbital da binária pós-envelope comum *sdB+dM* eclipsante destacada, Kepler-451, através do método Monte Carlo via Cadeia de Markov [(*MCMC*; [Gilks et al., 1995](https://books.google.com.br/books?hl=pt-BR&lr=&id=TRXrMWY_i2IC&oi=fnd&pg=PA1&dq=gilks+1995+MCMC&ots=7kTqqsKwkt&sig=QVxAhVMecFyRYTv1ThifNN02NeU#v=onepage&q=gilks%201995%20MCMC&f=false)) adaptado para o algoritmo genético Evolução Diferencial (*DE*; [Storn and Price, 1997](https://link.springer.com/article/10.1023/a:1008202821328)).

## Cadeia de Markov de Evolução Diferencial

Usamos o algoritmo [*DE-MC*](https://link.springer.com/article/10.1007/s11222-006-8769-1#preview) neste trabalho para propor novos valores de parâmetros por evolução diferencial. Entretanto, a aceitação ou rejeição dessas propostas segue a probabilidade de aceitação MH, governada pela probabilidade a posteriori, preservando as propriedades fundamentais do *MCMC*.

As vantagens do *DE-MC* sobre o *MCMC* convencional são a simplicidade, a velocidade de cálculo e a convergência para a distribuição posterior correta, mesmo para parâmetros quase colineares e densidades multimodais. Sendo assim, recomendado para análises de dados realistas, incluindo sistemas com mútuas interações planetárias observáveis fortes ([Nelson et al., 2013](https://iopscience.iop.org/article/10.1088/0067-0049/210/1/11/meta)).

Implementamos este método visando ajustar a efeméride linear dos instantes dos meios dos eclipses, ajustados pelo modelo WD+PIKAIA e convertidos para *BJD*, somatizada à contribuição do ETL (equação não linear), atribuída por corpos extras ligados gravitacionalmente ao sistema estudado. Essa abordagem visa investigar possíveis variações no seu período orbital.
