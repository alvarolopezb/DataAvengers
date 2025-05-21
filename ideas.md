# NLP y Grafos:

### Datasets con descripciones de trabajos para NER:

La idea es usar a Gepeto para traducirlos a español y etiquetarlos tocandonos las narices
https://www.kaggle.com/datasets/yuanmozhu/job-boards-listings-for-it-jobs
https://www.kaggle.com/datasets/andrewmvd/data-analyst-jobs

## NLP:

  - Fine tuning ROBERTA (LADY GAGA) con etiquetado de NER especializado en HR.
  - Preprocesado de Stopwords
  - Etiquetado por cortesía de Gepeto:
      - Habilidades técnicas o blandas (SKILL)
      - Idiomas (LANGUAGE)
      - Nivel de experiencia (EXPERIENCE_LEVEL)
      - Certificaciones (CERTIFICATION)
      - Títulos de puesto (JOB_TITLE)
      - Formación requerida (DEGREE)
      - Herramientas o tecnologías (TECH_TOOL)
      - Tipo o duración del contrato (CONTRACT_TYPE, CONTRACT_DURATION)
      - Jornada o horario (WORK_HOURS)
      - Beneficios o ventajas (BENEFIT)
      - Localización (LOCATION)
      - Rango salarial (SALARY)
      - Requisitos legales (LEGAL_REQ)
  - Extracción de la etiquetas
      - Con nuestro RecruBERT en español sacamos y estructuramos la información de las descripciones de trabajos y cv.
      - Hasta aquí preparación de datos.
        
  ## Grafos 
  
  - Ahora vamos con la chicha. Como conectamos a personas con trabajos?
  - Usamos networkx, hay que buscar una forma adecuada para poder generar el grafo y las recomendaciones
  - Pesos para las conexiones por cada tipo de NER. Tambien para las recomendaciones, hay que tener en cuenta la antiguedad de la persona que recomienda.
  - Estos pesos es para skills y demas tipos de etiquetas. Cada tipo va a tener su peso. Los pesos de skills se pueden hacer dependiendo de la demanda del tipo de puesto ofertado y otros similares.
  - kmeans de trabajos y sus pesos pre calculados. 
  - Sacar la frecuencia de skills por tipo de trabajo, y manualmente poner los pesos (con un algo seguro, a manini no se hace nada)

## Interfaz

  - Streamlit, Filippino Assassino se encarga. Jorgino Capuchino seguro que se quiere meter a optimizar, Nuestro FRONTEND DEV.


