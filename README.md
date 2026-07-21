## o que esse projeto resolve?
imagina uma fabrica de transformadores parando do nada porque uma maquina quebrou. isso atrasa toda a linha de producao e quebra o planejamento de compras . esse projeto de machine learning preve se uma maquina vai dar pau ou nao com base nos dados dos sensores (temperatura, rpm, torque e desgaste), avisando antes da falha acontecer. a arvore de decisao final acertou mais de 95% dos casos no teste!

## tecnologias e tecnicas utilizadas
- **python**: a linguagem principal.
- **pandas, matplotlib & seaborn**: pra tratar os dados, tirar nulos/duplicados e plotar os graficos.
- **scikit-learn**: pra padronizar os dados e criar os modelos preditivos (arvore de decisao e knn).
- **imbalanced-learn (smote)**: pra criar dados sinteticos no treino, ja que quebra de maquina e um evento raro e a base tava super desbalanceada.
- **feature engineering**: criacao da variavel 'potencia' multiplicando rpm por torque pra medir o esforco real do equipamento.

## como executar o sistema
1. faça o clone desse repositorio na sua maquina.
2. instale as bibliotecas necessarias rodando no terminal: `pip install -r requirements.txt`
3. abra o arquivo `.ipynb` no jupyter notebook, google colab ou vs code.
4. rode todas as celulas em sequencia. o sistema vai carregar os dados, limpar, treinar as IAs e cuspir a acuracia final.

## o que da pra melhorar no futuro
- testar algoritmos mais parrudos, tipo random forest ou xgboost.
- fazer um deploy do modelo em uma api simples (com flask ou fastapi) pra maquina avisar o celular do operador em tempo real.
- puxar e cruzar esses dados direto com o modulo de manutencao do sap.
