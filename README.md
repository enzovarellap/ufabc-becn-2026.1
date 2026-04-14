# 🧊 Conservação Térmica de Garrafas — BECN UFABC 2026.1

Análise experimental e modelagem matemática da eficiência térmica de garrafas comerciais, desenvolvida para o **XXVIII Simpósio de Base Experimental das Ciências Naturais** da Universidade Federal do ABC (UFABC), campus Santo André — Abril de 2026.

## 🔗 Acesso

**[→ Acessar o projeto online](https://enzovarellap.github.io/ufabc-becn-2026.1/)**

## 📋 Sobre o Projeto

O experimento compara a eficiência térmica de seis garrafas (Gocase, Tuyo, Stanley, Pacco, Le Postiche e uma descartável de plástico) utilizando uma mistura de água gelada a 5 °C com gelo. As medições de temperatura foram realizadas ao longo de 90 minutos, e o volume de água derretida ao final do experimento foi utilizado como indicador energético.

### Dados do Experimento

| Parâmetro | Valor |
|---|---|
| Massa de gelo | 53,42 g |
| Derretimento total | 56,2 ml |
| Volume total (gelo + água) | 300 ml |
| Temperatura ambiente | 23 °C |
| Temperatura inicial | 5 °C |
| Duração | 90 min |

### Garrafas Testadas

| Garrafa | Água Derretida | Status aos 90 min |
|---|---|---|
| Plástico (controle) | 56,2 ml | Todo gelo derreteu |
| Le Postiche | 56,2 ml | Todo gelo derreteu |
| Pacco | 56,2 ml | Todo gelo derreteu |
| Gocase | 54,1 ml | Gelo residual |
| Tuyo | 51 ml | Gelo residual |
| Stanley | 35 ml | Gelo residual |

## 📊 Páginas de Análise

### [Curvas de Aquecimento](https://enzovarellap.github.io/ufabc-becn-2026.1/curvas.html)
Modelo de duas fases (Fase 1: gelo presente → Fase 2: aquecimento exponencial) com cálculo da condutância térmica UA, constante k, tempo de derretimento e projeção das curvas até a temperatura ambiente.

### [Linearização Logarítmica](https://enzovarellap.github.io/ufabc-becn-2026.1/linearizacao.html)
Transformação ln(T_amb − T) vs. t para validação do modelo exponencial via regressão linear, com gráfico, tabela de parâmetros (m, b, k, R²) e cálculo detalhado da transformação.

## 🔬 Fundamentação Teórica

O modelo utiliza a **Lei de Resfriamento de Newton** aplicada em duas fases:

**Fase 1** — Enquanto há gelo, a energia térmica é absorvida pelo calor latente de fusão (L_f = 334 kJ/kg), mantendo T ≈ 0 °C.

**Fase 2** — Após derretimento total, a temperatura segue:

```
T(t) = T_amb × [1 − e^(−k · (t − t_melt))]
```

A condutância térmica UA (W/K) é calculada pelo volume de água derretida:

```
UA = m_derretida × L_f / (t × T_amb)
```

A linearização logarítmica valida o modelo:

```
ln(T_amb − T) = ln(C) − k · t
```

## 🏆 Resultado Principal

| # | Garrafa | UA (W/K) | t_melt | Ranking |
|---|---|---|---|---|
| 🏆 | Stanley | 0,0941 | 2,6 h | Melhor isolamento |
| 2 | Tuyo | 0,1371 | 1,8 h | — |
| 3 | Gocase | 0,1455 | 1,7 h | — |
| 4 | Pacco | 0,1478 | 1,3 h | — |
| 5 | Le Postiche | 0,1503 | 0,8 h | — |
| 6 | Plástico | 0,1560 | 0,4 h | Controle |

## 👥 Autores

- Ana Beatriz Souza Freeman
- Beatriz Santos Franco
- Clarice Maria de Faria Lima
- Enzo Varella Pastore
- Manuela Varela Medeiros
- Talita Santos da Silva

**Orientador:** Prof. Reginaldo Kisho Fukuchi

## 📚 Referências

1. DIEFENTHÄLE, A. T.; AVI, P. C. Determinação da curva de resfriamento da água em ampolas de garrafas térmicas. **Revista Mundi ETG**, v. 1, n. 2, 2016.

2. INMETRO. Garrafa térmica com ampola de vidro. Disponível em: https://www.inmetro.gov.br/consumidor/produtos/garrafaTermica.asp

3. FAGUNDES, A. W. R. *et al.* Modelagem matemática na lei de resfriamento de Newton: experiência com garrafas térmicas. **SAJEBTT**, v. 6, n. 2, p. 21–39, 2019.

## 🛠️ Tecnologias

- HTML/CSS/JS puro (sem frameworks)
- [Chart.js](https://www.chartjs.org/) para gráficos interativos
- GitHub Pages para hospedagem

---

UFABC — Base Experimental das Ciências Naturais — 2026.1
