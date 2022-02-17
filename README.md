# projeto_9_predicao_resultado_teste_covid
 Meu 9 projeto de machine learning em que o objetivo era tentar predizer o resultado de um teste de covid.

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

As etapas do projeto consistiram em:

- Passo 1: Pré processamento e EDA
    - Importação das bibliotecas
    - Analisando a consistência dos dados
    - EDA
- Passo 2: Feature Engeneering e Modelagem
    - Feature engeneering
    - Modelagem
- Passo 3: Tunning dos modelos
    - Adaboost
    - Regressão Logística
    - XGBoost
    - Alterando os threshold
- Passo 4: Treinamento com a base completa e conclusão
    - Treinamento com a base completa
    - Conclusão
