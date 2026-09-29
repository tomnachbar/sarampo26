<p align="center"> <img src="https://user-images.githubusercontent.com/50468352/141820811-412e9364-7f5c-4889-826a-fcba23b92e23.png" width="350" alt="Logo do Projeto" /> </p> <h3 align="center">📌 Análise de Dados com Machine Learning — Indicador de Sarampo (RIPSA)</h3> <p align="center"><strong>Autor:</strong> Eliton Mauro Nachbar</p> <p align="center"><strong>Curso:</strong> Data Science — Univesp</p>
💡 Projeto: Predição de Casos de Sarampo por Município

Pipeline de Machine Learning para prever a ocorrência de casos de sarampo em municípios brasileiros, a partir de dados públicos do RIPSA, com exportação de resultados para o Power BI.

<details> <summary>🟡 <strong>Sobre o problema encontrado</strong></summary> <br/>

🔍 A base de dados do RIPSA (Rede Interagencial de Informação para a Saúde) registra, mês a mês, indicadores de vigilância epidemiológica por município, desagregados por sexo, faixa etária, situação vacinal e tipo de caso.

A grande maioria dos registros (~97%) tem valor zero, ou seja, a ocorrência de casos é um evento raro — o que torna a identificação de padrões e a antecipação de focos um desafio tanto estatístico quanto de saúde pública.

</details>
<details> <summary>🟡 <strong>Solução implementada</strong></summary> <br/>

✅ Construímos um pipeline completo de análise preditiva com scikit-learn, cobrindo:

🧹 Tratamento de dados e remoção de vazamento de informação (data leakage)
🏗️ Engenharia de atributos (temporais, geográficos e de categoria)
⚖️ Classificação binária com RandomForestClassifier (class_weight='balanced') para lidar com o forte desbalanceamento entre as classes
📈 Avaliação com ROC-AUC, recall, precisão e matriz de confusão
📊 Exportação dos resultados para o Power BI, permitindo segmentação por UF, região e categoria
</details>
<details> <summary>🟡 <strong>Estrutura do projeto</strong></summary> <br/>

📓 Todo o pipeline está documentado passo a passo no notebook analise_ml_ripsa.ipynb, da carga dos dados até a exportação final. Os arquivos gerados para consumo no Power BI são:

Arquivo	Conteúdo
predicoes_powerbi.csv	Predições do modelo por município, com probabilidade e acerto
importancia_atributos.csv	Importância de cada atributo no modelo
curva_roc.csv	Pontos da curva ROC (FPR x TPR)
metricas.csv	Resumo das métricas do modelo
</details>
<details> <summary>🛠️ <strong>Como rodar o projeto localmente</strong></summary> <br/>

✅ Clonar o projeto para a máquina local: <code>git clone https://github.com/tomnachbar/SEU-REPOSITORIO.git</code>

</br>

✅ Acesse o diretório do projeto: Navegue para o diretório do projeto clonado usando o comando: <code>cd SEU-REPOSITORIO</code>

</br>

✅ Instale as dependências: <code>pip install pandas numpy scikit-learn joblib jupyter</code>

</br>

✅ Rodando o notebook: O arquivo de dados original (ripsa008mb.csv) está compactado como ripsa008mb.zip neste repositório para respeitar o limite de tamanho do GitHub. O pandas lê o .zip diretamente, sem necessidade de extração:

<code>CAMINHO_CSV = 'ripsa008mb.zip'</code>

Abra analise_ml_ripsa.ipynb no Jupyter, no VS Code ou em um GitHub Codespace e execute as células em ordem (Executar Tudo).

</details>
🧰 Tecnologias e ferramentas utilizadas
<p> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Badge"/> <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas Badge"/> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn Badge"/> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Badge"/> <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/> <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI Badge"/> </p>
📚 Fonte dos dados

Dados públicos do RIPSA — Rede Interagencial de Informação para a Saúde.
