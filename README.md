# Projeto de Condução Elétrica com Método dos Elementos Finitos (MEF)

Este projeto faz parte do exercício optativo da disciplina de PMR 3401 - Mecânica Computacional, e envolve a análise de condução elétrica em um meio contínuo utilizando o Método dos Elementos Finitos (MEF). O objetivo é resolver a equação de Laplace em um domínio bidimensional.

## Estrutura do Projeto

### Arquivos Principais

- `main.m`: Script principal que realiza a simulação e gera as visualizações dos resultados.

## Descrição do Problema

Em regime estacionário, o fenômeno de condução elétrica em duas dimensões e em meios contínuos é regido pela equação de Laplace:

$$
-\sigma \left( \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} \right) = 0
$$


### Condições do Problema

- **Condutividade elétrica**:

  - Material A: $\(\sigma_A = 4 \times 10^6 \, S/m\)$
  - Material B: $\(\sigma_B = 9 \times 10^7 \, S/m\)$

- **Potencial elétrico**:
  - $\(V = 200 \, V\)$ nos pontos $\(x = 0 \, m\)$ e $\(y = 0,22 \, m\)$
  - $\(V = 0 \, V\)$ nos pontos $\(x = 0,24 \, m\)$

### Implementação

O código MATLAB utiliza o Método dos Elementos Finitos (MEF) com uma malha triangular para resolver a equação de Laplace. As condições de contorno são aplicadas conforme descrito no enunciado.

#### Estrutura do Código

1. **Inicialização**:
   - Definição das variáveis globais e condições iniciais.
   - Criação da malha triangular utilizando coordenadas dos nós e elementos.

2. **Resolução**:
   - Montagem da matriz de rigidez e do vetor de força.
   - Aplicação das condições de contorno.
   - Solução do sistema linear resultante para obter o potencial elétrico $\(V(x, y)\)$.

3. **Visualização**:
   - Geração de gráficos para visualizar a distribuição de \(V(x, y)\) e o vetor densidade de corrente elétrica $\(\mathbf{J}(x, y)\)$.

4. **Cálculo da Resistência Elétrica**:
   - Cálculo da corrente elétrica média $\(I_m\)$ utilizando integração numérica.
   - Cálculo da resistência elétrica $\(R\)$ do bloco.

#### Como Executar

1. Abra o MATLAB e navegue até o diretório contendo o script `main.m`.
2. Execute o script digitando `main` no console do MATLAB.
3. A simulação será iniciada e os resultados serão salvos na pasta atual.

### Resultados

Os resultados incluem:
- Gráficos da distribuição de $\(V(x, y)\)$ no domínio.
- Vetores da densidade de corrente elétrica $\(\mathbf{J}(x, y)\)$.
- Cálculo da resistência elétrica $\(R\)$ do bloco.

### Distribuição de Potencial Elétrico

![Distribuição de Potencial Elétrico](https://github.com/DouglasOliveiraC/MATLAB---Problema-de-Condutividade/blob/main/potencial%20eletrico.png)

### Vetores da Densidade de Corrente Elétrica

![Densidade de Corrente Elétrica](https://github.com/DouglasOliveiraC/MATLAB---Problema-de-Condutividade/blob/main/densidade_corrente.png)


## Dependências

- MATLAB R2021a ou superior.

## Contato

Douglas Oliveira  
Email: douoliver@gmail.com
