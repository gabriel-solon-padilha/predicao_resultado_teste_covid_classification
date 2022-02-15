# projeto_9_predicao_resultado_teste_covid
 Meu 9 projeto de machilearning em que o objetivo era tentar predizer o resultado de um teste de covid.

Nesse projeto temos as seguintes features:

<br>
 - **id**: Identificação do paciente<br>
 - **sex**: Sexo do Paciente (0 - Homem / 1 - Mulher) <br>
 - **patient_type**: Se o paciente foi dispensado para casa (1) ou se foi internado (0) <br>
 - **intubed**: Seo paciente foi intubado ou não<br>
 - **pneumonia**: Se o paciente apresentou pneumonia ou não<br>
 - **age**: Idade do Paciente<br>
 - **pregnancy**: Se a paciente estava grávida ou não (para pacientes mulheres)<br>
 - **diabetes**: Se o paciente tem diabetes ou não<br>
 - **copd**: Se opaciente tem COPD ou não<br>
 - **asthma**: Se o paciente tem Asma ou não<br>
 - **inmsupr**: Se o paciente apresentou Imunosupressão ou não<br>
 - **hypertension**: Se o paciente tem hipertensão ou não<br>
 - **ohter_disease**: Se o paciente tem outras doenças ou não<br>
 - **cardiovascular**: Se o paciente tem doenças cardiácas ou não<br>
 - **obesity**: Se o paciente tem obesidade ou não<br>
 - **renal_chronic**: Se o paciente tem problemas renais ou não<br>
 - **tobacco**: Se o paciente é fumante ou não<br>
 - **contact_other_covid**: Se o paciente teve contato com outras pessoas diagnosticadas com covid<br>
 - **icu**: Se o paciente precisou ser internado na UTI<br>
 - **covid_res**: Se o resultado do teste foi Positivo ou Negativo<br>

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
- Passo 4: Treinamento com a base completa e conclusão
    - Treinamento com a base completa
    - Conclusão