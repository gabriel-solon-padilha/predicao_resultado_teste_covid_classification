# Predição de resultado teste de covid

## Introdução
Meu quinto projeto de machine learning em que o objetivo era tentar predizer o resultado de um teste de covid.

Nesse projeto temos as seguintes features:
 - id: Identificação do paciente
 - sex: Sexo do Paciente (0 - Homem / 1 - Mulher) 
 - patient_type: Se o paciente foi dispensado para casa (1) ou se foi internado (0) 
 - intubed: Seo paciente foi intubado ou não
 - pneumonia: Se o paciente apresentou pneumonia ou não
 - age: Idade do Paciente
 - pregnancy: Se a paciente estava grávida ou não (para pacientes mulheres)
 - diabetes: Se o paciente tem diabetes ou não
 - copd: Se opaciente tem COPD ou não
 - asthma: Se o paciente tem Asma ou não
 - inmsupr: Se o paciente apresentou Imunosupressão ou não
 - hypertension: Se o paciente tem hipertensão ou não
 - ohter_disease: Se o paciente tem outras doenças ou não
 - cardiovascular: Se o paciente tem doenças cardiácas ou não
 - obesity: Se o paciente tem obesidade ou não
 - renal_chronic: Se o paciente tem problemas renais ou não
 - tobacco: Se o paciente é fumante ou não
 - contact_other_covid: Se o paciente teve contato com outras pessoas diagnosticadas com covid
 - icu: Se o paciente precisou ser internado na UTI
 - covid_res: Se o resultado do teste foi Positivo ou Negativo

## Desenvolvimento
As etapas do projeto consistiram em:
- Passo 1: Pré processamento e EDA
    - Importação das bibliotecas
    - Analisando a consistência dos dados
    - EDA
- Passo 2: Feature Engeneering e Modelagem
    - Feature engeneering
    - Modelagem
- Passo 3: Tunning dos melhores modelos
    - Adaboost
    - Regressão Logística
    - XGBoost
    - Alteração de threshold
- Passo 4: Treinamento com a base completa e conclusão
    - Treinamento com a base completa
    - Conclusão

## Conclusão e resultados encontrados

   Model     |    f1  	|precision|	recall  |	accuracy|	auc
-------------|---------|---------|---------|---------|-------
reg_logistic	 |0.468673	|0.648371	|0.366967	|0.632576	|0.604793
ada_boost	    |0.467286	|0.655936	|0.362911	|0.634607	|0.606187
xgb	          |0.466619	|0.665477	|0.359263	|0.637309	|0.608225


Mesmo após otimizar os modelos, o recall não ficou satisfatório. Com a alteração do treshold, conseguimos aumentar nosso recall a custo de uma redução muito expressiva na precision, o que também não seria um cenário ideial, já que aumentarmos demais o erro tipo 1, podendo ocasionar uma falta de confiança por parte da população nos testes de covid.

A nossa variável target, o resultado do teste conseguiu ter os resultados negativos previstos bem em volume mas os positivos não (recall). Além disso, de todos os resultados que prevíamos, acertávmos próximo a 70% para testes positivos e para testes negativos (precision). Considerando que aqui o erro tipo 2 (falso negativo) é o mais fatal e prejudicial a população, não consigo considerar que noss modelo poderia ser colocado em produção. Algumas conclusões dos motivos desses resultados.

- A escolha dos dados (features) para prever o resultado do teste não foi adequada. Haviam features que ocorriam após o resultado do teste como internação, intubação e internação na UTI
- Uma abordagem mais lógica para o problema e que poderia gerar mais benefícios econômicos seria tentar prever a necessidade de internação, intubação ou internação na UTI a partir das features e usar o resultado do teste como uma feature também. Com essa predição poderia ser tomadas medidas pelos orgãos de saúde como forma de tratar a epidemia.
- Para prever o resultado do teste, usar features mais focadas em expressões de genes ou indicadores biológicos, como a saturação de oxigênio no sangue faria mais sentido e provavelmente levaria a um resultado mais satisfatório

Essas foram minhas conclusões e estou aberto a qualquer tipo de feedback.

IDEIAS futuras para o projeto
 - Tentar usar a metodologia de inferência causal
