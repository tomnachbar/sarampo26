<p align="center"> <img src="https://user-images.githubusercontent.com/50468352/141820811-412e9364-7f5c-4889-826a-fcba23b92e23.png" width="350" alt="Logo do Projeto" /> </p> <h3 align="center">📌 Análise de Dados com Machine Learning — Indicador de Sarampo (RIPSA)</h3> <p align="center">

<p align="center"><strong>Orientadora do PI:</strong> Camila Ciasca Prodocimi </p>

---

## 👥 Integrantes do grupo

| Nome                              |
|-----------------------------------|
| Daniel Guilherme Vieira Ferreira| 
| Eliton Mauro Nachbar| 
| Fernando de Barros Lellis| 
| Flavio Jorge de Medeiros|
| João Ramos de Kinal| 
| Ricardo Gabriel da Barros Carnecini|
---

💡 Projeto: SARAMPO EM DADOS – Plataforma para análise epidemiológica de casos no 
Brasil

Pipeline de Machine Learning para prever a ocorrência de casos de sarampo em municípios brasileiros, a partir de dados públicos do RIPSA, com exportação de resultados para o Power BI.

<details> <summary>🟡 <strong>Sobre o problema encontrado</strong></summary> <br/>

🔍 A base de dados do RIPSA (Rede Interagencial de Informação para a Saúde) registra, mês a mês, indicadores de vigilância epidemiológica por município, desagregados por sexo, faixa etária, situação vacinal e tipo de caso. <br/><br/> A grande maioria dos registros (~97%) tem valor zero, ou seja, a ocorrência de casos é um evento raro — o que torna a identificação de padrões e a antecipação de focos um desafio tanto estatístico quanto de saúde pública.

</details>
<details> <summary>🟡 <strong>Solução implementada</strong></summary> <br/>

✅ Construímos um pipeline completo de análise preditiva com <strong>scikit-learn</strong>, cobrindo:

<ul> <li>🧹 Tratamento de dados e remoção de vazamento de informação (<em>data leakage</em>)</li> <li>🏗️ Engenharia de atributos (temporais, geográficos e de categoria)</li> <li>⚖️ Classificação binária com <code>RandomForestClassifier</code> (<code>class_weight='balanced'</code>) para lidar com o forte desbalanceamento entre as classes</li> <li>📈 Avaliação com <code>ROC-AUC</code>, <code>recall</code>, <code>precisão</code> e matriz de confusão</li> <li>📊 Exportação dos resultados para o <strong>Power BI</strong>, permitindo segmentação por UF, região e categoria</li> </ul> </details>
<details> <summary>🟡 <strong>Estrutura do projeto</strong></summary> <br/>

📓 Todo o pipeline está documentado passo a passo no notebook <code>analise_ml_ripsa.ipynb</code>, da carga dos dados até a exportação final. Os arquivos gerados para consumo no Power BI são:

<br/><br/>

<table> <thead> <tr> <th align="left">Arquivo</th> <th align="left">Conteúdo</th> </tr> </thead> <tbody> <tr> <td><code>predicoes_powerbi.csv</code></td> <td>Predições do modelo por município, com probabilidade e acerto</td> </tr> <tr> <td><code>importancia_atributos.csv</code></td> <td>Importância de cada atributo no modelo</td> </tr> <tr> <td><code>curva_roc.csv</code></td> <td>Pontos da curva ROC (FPR x TPR)</td> </tr> <tr> <td><code>metricas.csv</code></td> <td>Resumo das métricas do modelo</td> </tr> </tbody> </table> </details>
<details> <summary>🛠️ <strong>Como rodar o projeto localmente</strong></summary> <br/>

✅ <strong>Clonar o projeto para a máquina local:</strong> <br/> <code>git clone https://github.com/tomnachbar/sarampo26.git</code>

<br/><br/>

✅ <strong>Acesse o diretório do projeto:</strong> <br/> Navegue para o diretório do projeto clonado usando o comando: <br/> <code>cd SEU-REPOSITORIO</code>

<br/><br/>

✅ <strong>Instale as dependências:</strong> <br/> <code>pip install pandas numpy scikit-learn joblib jupyter</code>

<br/><br/>

✅ <strong>Rodando o notebook:</strong> <br/> O arquivo de dados original (<code>ripsa008mb.csv</code>) está compactado como <code>ripsa008mb.zip</code> neste repositório para respeitar o limite de tamanho do GitHub. O <code>pandas</code> lê o <code>.zip</code> diretamente, sem necessidade de extração:

<br/><br/>

<code>'ripsa008mb.zip'</code>

<br/><br/>

Abra <code>analise_ml_ripsa.ipynb</code> no Jupyter, no VS Code ou em um GitHub Codespace e execute as células em ordem (Executar Tudo).

</details>
🧰 Tecnologias e ferramentas utilizadas
<p> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Badge"/> <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas Badge"/> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn Badge"/> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Badge"/> <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/> <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI Badge"/> </p>
📚 Fonte dos dados

Dados públicos do RIPSA — Rede Interagencial de Informação para a Saúde.
