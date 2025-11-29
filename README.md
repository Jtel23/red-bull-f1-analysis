# 🚀 **README COMPLETO — Red Bull Racing F1 Analysis**

```markdown
# 🏎️ Red Bull Racing — F1 Data Analysis Project

Este projeto apresenta uma análise detalhada do desempenho da equipe **Red Bull Racing** na Fórmula 1, utilizando dados públicos do Kaggle, transformação via SQL no **Data.World**, pré-processamento no **Excel** e visualização final no **Power BI**.

O objetivo foi entender padrões de performance, impacto dos pilotos, comportamento em diferentes circuitos e tendências históricas da equipe.

---

## 📊 Dashboard (Power BI)

O dashboard completo está disponível no arquivo:

> **Nota importante:**  
> O arquivo PBIX está conectado diretamente a um **dataset externo no Data.World**, portanto o Power BI pode exibir erros de conexão ao abrir.  
> Isso é esperado.  
> Para fins de portfólio, o `.pbix` serve para demonstrar:
> - O **modelo de dados**
> - Medidas **DAX**
> - Transformações realizadas no **Power Query**
> - O layout e estrutura das visualizações


---

## 📚 Fonte dos Dados

Os dados originais são públicos e podem ser acessados aqui:

🔗 Kaggle — F1 Race Traces  
https://www.kaggle.com/code/jtrotman/f1-race-traces-2021

Este dataset contém informações sobre:

- Corridas  
- Pilotos  
- Circuitos  
- Pontuações  
- Velocidade média  
- Estatísticas de performance  

---

## 🔧 Tecnologias Utilizadas
- **SQL (Data.World)** — criação das tabelas analíticas  
- **Power BI** — visualização, storytelling e modelagem  
- **Power Query** — transformações finais  
- **Kaggle** — fonte dos dados brutos  

---

## 🔍 Processo do Projeto (ETL + Análise)

### **1. Coleta de Dados**
O dataset original foi baixado do Kaggle, contendo múltiplas temporadas da Fórmula 1 com métricas de velocidade, pontuação, pilotos e pistas.

### **2. SQL no Data.World**
As queries foram rodadas diretamente no servidor SQL da plataforma.

> As queries originais não foram exportadas, mas abaixo está uma representação fiel da lógica utilizada.

**🔸 Pontos totais por piloto**
```sql
SELECT driver, SUM(points) AS total_points
FROM races
GROUP BY driver
ORDER BY total_points DESC;
````

**🔸 Velocidade média por circuito**

```sql
SELECT circuit, AVG(average_speed) AS avg_speed
FROM races
GROUP BY circuit;
```

**🔸 Performance da Red Bull por ano**

```sql
SELECT season, SUM(points) AS total_points
FROM races
WHERE team = 'Red Bull Racing'
GROUP BY season;
```

---

## 📈 Insights Principais

* A Red Bull mostra **crescimento consistente** em temporadas específicas, alinhado com atualizações de regulamento.
* A diferença entre pilotos da equipe é evidente: um deles concentra grande parte da pontuação.
* Circuitos de alta velocidade aumentam significativamente o desempenho da equipe.
* Pistas de rua tendem a reduzir a vantagem da Red Bull, equalizando o grid.
* A velocidade média da equipe cresce continuamente ao longo das temporadas analisadas.

---


## 👤 Autor

**Julio — Data Analyst**
🔗 LinkedIn: *[(adicione aqui)](https://www.linkedin.com/in/j%C3%BAlio-teleschi-ba173420b/)*

---

Se quiser visualizar ou melhorar o projeto, fique à vontade para abrir issues ou sugestões.

```

