# 📊 Fundamentos de Ciência de Dados

Repositório destinado às práticas e implementações desenvolvidas na disciplina de **Fundamentos de Ciência de Dados** (ULBRA). O objetivo deste repositório é aplicar conceitos estatísticos e matemáticos fundamentais utilizando **Python** e **Jupyter Notebooks**.

---

## 📌 Conteúdo do Projeto

O arquivo principal [`Calculos.ipynb`](Calculos.ipynb) possui implementações manuais em Python (sem bibliotecas externas) para diversas operações e medidas estatísticas de tendência central e somatórios:

1. **Somatório ao Quadrado (`somantorio_ao_quadrado(n)`)**:
   - Calcula a soma dos quadrados dos números inteiros de $0$ até $n$:
     $$\sum_{i=0}^{n} i^2$$

2. **Soma de Dados (`soma_dados(conjunto)`)**:
   - Realiza o somatório simples dos elementos de um determinado conjunto numérico:
     $$\sum x_i$$

3. **Média Aritmética (`media_aritmetica(conjunto)`)**:
   - Calcula a média simples de uma amostra/conjunto de dados:
     $$\bar{x} = \frac{\sum x_i}{n}$$

4. **Soma dos Quadrados dos Dados (`soma_dados_ao_quadradro(conjunto)`)**:
   - Calcula o somatório dos elementos elevados ao quadrado em um conjunto:
     $$\sum x_i^2$$

5. **Média Harmônica (`media_harmonica(conjunto)`)**:
   - Média útil em situações que envolvem taxas e proporções (como velocidades médias):
     $$H = \frac{n}{\sum \frac{1}{x_i}}$$

6. **Média Geométrica (`media_geometrica(conjunto)`)**:
   - Média aplicável no cálculo de taxas de crescimento e percentuais acumulados:
     $$G = \sqrt[n]{\prod_{i=1}^{n} x_i} = \left(\prod_{i=1}^{n} x_i\right)^{\frac{1}{n}}$$

7. **Média Quadrática (`media_quadratica(conjunto)`)**:
   - Conhecida também como *Root Mean Square* (RMS), muito empregada em análises estatísticas e físicas:
     $$RMS = \sqrt{\frac{\sum x_i^2}{n}}$$

8. **Média Ponderada (`media_ponderada(valores, pesos)`)**:
   - Calcula a média atribuindo diferentes pesos a cada valor:
     $$\bar{x}_w = \frac{\sum (x_i \cdot w_i)}{\sum w_i}$$

9. **Mediana (`mediana(conjunto)`)**:
   - Elemento central de um conjunto numérico ordenado. Se a quantidade $n$ de elementos for ímpar, retorna o valor central; se $n$ for par, resulta na média dos dois valores centrais:
     $$Md = \begin{cases} x_{\left(\frac{n+1}{2}\right)}, & \text{se } n \text{ for ímpar} \\[6pt] \frac{x_{\left(\frac{n}{2}\right)} + x_{\left(\frac{n}{2} + 1\right)}}{2}, & \text{se } n \text{ for par} \end{cases}$$

10. **Moda (`moda(conjunto)`)**:
    - Identifica o elemento (ou elementos) de maior frequência no conjunto. Suporta distribuições **unimodais**, **multimodais** e identifica casos **amodais**:
      $$Mo = \text{valor(es) com maior frequência de ocorrência em } X$$

11. **Ponto Médio (`ponto_medio(conjunto_ou_a, b=None)`)**:
    - Calcula o ponto médio tanto de um conjunto de dados (*Midrange*) quanto de um intervalo de classe $[a, b]$:
      $$PM = \frac{\min(X) + \max(X)}{2} \quad \text{ou} \quad PM = \frac{a + b}{2}$$

---

## 💡 Casos de Uso Práticos no Dia a Dia

| Medida Estatística | Exemplo Prático do Mundo Real | Por que usar essa medida? |
| :--- | :--- | :--- |
| **Média Aritmética** | Média de notas escolares sem pesos (ex: `7.5, 8.0, 6.5, 9.0`) | Avaliação simples quando todas as observações têm a mesma importância. |
| **Média Ponderada** | Nota final da faculdade onde provas têm peso maior que trabalhos | Quando determinados dados têm importância/peso diferente na média. |
| **Média Harmônica** | Velocidade média em percursos de mesma distância (ex: ida a 60 km/h e volta a 40 km/h) | Correta para taxas e velocidades. A média simples daria 50 km/h (incorreto), enquanto a harmônica dá 48 km/h (correto). |
| **Média Geométrica** | Rentabilidade acumulada de investimentos ao longo dos anos (+10%, +20%, -5%) | Ideal para valores multiplicativos, percentuais acumulados e taxas de crescimento populacional/financeiro. |
| **Média Quadrática (RMS)** | Medição de tensão elétrica alternada em Volts (ex: `115V, -110V, 108V, -112V`) | Muito usada na engenharia elétrica e acústica para calcular a amplitude/energia de sinais que oscilam entre positivo e negativo. |
| **Mediana** | Renda salarial de um bairro ou empresa com grande discrepância (ex: 5 estagiários e 1 CEO) | A média daria um salário irreal de R$ 18.500; a mediana entrega o valor realista do cidadão comum (R$ 2.350). |
| **Moda** | Controle de estoque de loja (tamanho de vestuário mais vendido: `"P"`, `"M"`, `"G"`) | Descobre qual item tem a maior demanda para guiar decisões de compra e reabastecimento. |
| **Ponto Médio** | Estimativa rápida da temperatura média diária (Mínima de 14°C e Máxima de 28°C) | Determina a posição central entre os dois limites extremos de uma amostragem. |

---

## 📁 Estrutura do Repositório

```text
data-science-fundamentals/
│
├── Calculos.ipynb     # Notebook com a implementação e casos práticos do dia a dia
├── requirements.txt   # Dependências do projeto (Jupyter, IPykernel, etc.)
├── .gitignore         # Arquivos ignorados pelo controle de versão
└── README.md          # Documentação do projeto
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

- **Python 3.8+** instalado na sua máquina.
- Git instalado.

### Passo a Passo

1. **Clonar o repositório** (caso tenha baixado via git):
   ```bash
   git clone <URL_DO_SEU_REPOSITORIO>
   cd data-science-fundamentals
   ```

2. **Criar e ativar um ambiente virtual** *(opcional, mas recomendado)*:
   - **Linux / macOS:**
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```
   - **Windows:**
     ```cmd
     python -m venv venv
     venv\Scripts\activate
     ```

3. **Instalar as dependências**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Abrir o Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   ou abra a pasta diretamente no **VS Code** com a extensão do Jupyter instalada e selecione o arquivo [`Calculos.ipynb`](Calculos.ipynb).

---

## 📤 Como Subir o Projeto para o GitHub

Seu repositório local já foi inicializado e comitado na branch `main`. Para enviar para o GitHub, siga apenas os passos 5 e 6 abaixo no terminal:

1. **Criar um novo repositório no GitHub** (no site github.com) sem inicializar com README ou gitignore.

2. **Conectar e Enviar para o Repositório Remoto**:
   ```bash
   git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
   git push -u origin main
   ```

---

## 📝 Licença e Autoria

Desenvolvido para fins acadêmicos na Universidade Luterana do Brasil (ULBRA).  
Sinta-se à vontade para utilizar o código para estudos!
