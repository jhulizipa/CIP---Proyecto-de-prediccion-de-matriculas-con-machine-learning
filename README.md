# CIP---Proyecto-de-prediccion-de-matriculas-con-machine-learning
Proyecot final de sustentación del curso de investigacion pregradual DataScience

# Resumen
Contexto. El proyecto busca analizar las tendencias de matrícula en instituciones de educación superior en Colombia mediante aprendizaje automático, identificando patrones y realizando predicciones para apoyar decisiones en el sector educativo, se enfoca en estudiar datos históricos relacionados con género, región y tipo de institución, para anticipar necesidades, asignar recursos eficientemente y poder diseñar políticas inclusivas. Además, proyectará escenarios futuros para reducir desigualdades y mejorar el acceso a la educación superior, promoviendo la equidad y el desarrollo social y económico del país.

# 1.Introducción
La educación superior desempeña un papel clave en el desarrollo social y económico de Colombia, ya que impacta directamente en la formación de profesionales y en la competitividad del país, sin embargo, la planificación efectiva de la oferta académica y la gestión de recursos requieren herramientas avanzadas que permitan prever tendencias y optimizar la toma de decisiones.
En este estudio, se implementó un modelo de Machine Learning para proyectar la matrícula en educación superior en Colombia, utilizando datos del Sistema Nacional de Información de la Educación Superior (SNIES). Este enfoque permite identificar patrones históricos y generar predicciones más precisas sobre la cantidad de estudiantes que ingresarán a las universidades en los próximos años.
El uso de técnicas de aprendizaje automático en este contexto no solo mejora la precisión de las estimaciones, sino que también brinda información valiosa para el diseño de políticas educativas, la asignación de recursos y la planificación institucional. A lo largo de este trabajo, se detalla el proceso de recopilación y análisis de datos, el desarrollo del modelo predictivo y sus implicaciones para el futuro de la educación superior en Colombia.

# 2. Métodos y materiales
La base de datos se obtiene de los datos históricos de matrícula en primer curso en instituciones de educación superior en Colombia entre los años 2000 y 2013. Esto incluye registros detallados por   semestre, género, institución, región, y tipo de institución. 

# 2.1. Datos
Los datos utilizados provienen del Sistema Nacional de Información de la Educación Superior (SNIES) e incluyen registros de matrícula, información sociodemográfica, indicadores académicos y características de las instituciones de educación superior.  

El dataset contiene 23,891 registros y 110 columnas. Algunas de las columnas más relevantes incluyen:

Institución de Educación Superior (IES): Nombre de la universidad o institución educativa.
Sector IES: Si la institución es oficial (pública) o privada.
Carácter IES: Tipo de institución (universidad, instituto, etc.).
Departamento de domicilio de la IES: Ubicación de la institución en Colombia.
Programa Académico: Nombre de la carrera o programa.
Nivel de Formación: Nivel de estudios (universitario, técnico, etc.).
Metodología del programa: Modalidad de estudio (presencial, virtual, etc.).
Área de Conocimiento: Clasificación del programa en áreas como ingeniería, salud, bellas artes, etc.
Año y semestre de matrícula: Datos desglosados por año y semestre, diferenciando matrícula de hombres y mujeres.




También se identificaron valores ausentes en variables críticas como el código del departamento y código del municipio del programa, lo que podría impactar análisis regionales y requerir un proceso de limpieza y normalización de datos.

# 2.2. Exploración de datos
El análisis de los datos de matrículas universitarias permite identificar tendencias clave en la evolución del número de estudiantes según la metodología del programa, el nivel de formación y su distribución geográfica.

Aquí se puede ver que la cantidad de estudiantes ha crecido significativamente en la modalidad presencial, mientras que las metodologías a distancia (tradicional y virtual) muestran un crecimiento más moderado, se evidencia un comportamiento cíclico en la modalidad presencial con picos en los segundos semestres de cada año.

Se observa una alta concentración de estudiantes en la modalidad presencial, mientras que las modalidades a distancia presentan una distribución menos dispersa con valores más homogéneos.

Los departamentos con mayor oferta de programas académicos son Bogotá D.C., Antioquia, Valle del Cauca y Atlántico, mientras que departamentos como Vaupés, Vichada y Guainía presentan una oferta significativamente menor.

La mayoría de los estudiantes se concentran en programas universitarios, seguidos por niveles tecnológicos y técnicos profesionales, la matrícula en maestrías, especializaciones y doctorados es considerablemente menor, aunque muestra una tendencia creciente.

# 2.3. Modificación de datos.
Se aplicaron técnicas de limpieza de datos, eliminación de valores nulos, imputación de datos faltantes y normalización de variables para optimizar el rendimiento del modelo predictivo.

# 2.4. Modelo.
Para la predicción de la matrícula en educación superior en Colombia, se implementaron y compararon diferentes modelos de Machine Learning con el objetivo de determinar el más preciso y eficiente se probaron la Regresión Lineal y el Random Forest Regressor, utilizando métricas de evaluación como el Error Absoluto Medio (MAE), el Error Cuadrático Medio (MSE) y el Coeficiente de Determinación (R²).
La Regresión Lineal, al ser un modelo simple y fácil de interpretar, proporcionó una primera aproximación a la tendencia de la matrícula, pero mostró limitaciones en la captura de variaciones complejas dentro de los datos históricos. Por otro lado, el modelo Random Forest Regressor demostró una mayor capacidad de predicción, ya que maneja datos no lineales y reduce el impacto del sobreajuste al trabajar con múltiples árboles de decisión.
Los resultados indicaron que Random Forest superó a la Regresión Lineal en todas las métricas de desempeño, con valores más bajos de MAE y MSE, y un coeficiente R² más alto, lo que confirma su precisión en la estimación de tendencias de matrícula, esto se debe a su capacidad para capturar relaciones no lineales entre las variables y minimizar la sensibilidad a valores atípicos.

# 3. Resultados y discusión. 
Los hallazgos sugieren que el uso de Machine Learning mejora la capacidad predictiva en comparación con modelos tradicionales,  sin embargo, los resultados mostraron que la Regresión Lineal, si bien es un modelo sencillo y fácil de interpretar, no logró capturar de manera precisa la variabilidad de los datos, reflejando limitaciones en su capacidad predictiva, en contraste, el modelo Random Forest Regressor mostró un mejor rendimiento al manejar datos más complejos y ofrecer predicciones más ajustadas a la realidad, la visualización de los resultados mediante gráficos comparativos permitió evidenciar la cercanía de las predicciones con los datos reales, validando la eficacia del modelo Random Forest en este contexto.
A través del proceso de predicción, se logró estimar el número de matrículas para los periodos 2014-1 y 2014-2, lo que refuerza la utilidad del aprendizaje automático como herramienta de apoyo en la planificación educativa, sin embargo, la precisión de los modelos está directamente relacionada con la calidad de los datos utilizados, lo que resalta la importancia de un pre procesamiento adecuado y una selección rigurosa de las variables más relevantes.

# 4. Conclusiones. 
El estudio logró modelar y analizar las tendencias de matrícula en instituciones de educación superior, comparando diferentes modelos de predicción para determinar su eficacia, se concluyó que, aunque la Regresión Lineal proporciona una aproximación inicial, el modelo Random Forest Regressor es más robusto y adecuado para este tipo de datos, ofreciendo predicciones más precisas y adaptadas a la variabilidad de las matrículas a lo largo del tiempo.
Además, la capacidad de generar predicciones futuras con base en datos históricos demuestra el potencial del machine learning en la toma de decisiones en el sector educativo.

# 5. Conflicto de intereses.
No existe ningún conflicto de intereses en la realización de este trabajo.

# 6  . Referencias.
Pérez, M., & Rodríguez, L. (2020). Análisis predictivo en la educación superior: retos y oportunidades. Editorial Académica.
Ramírez, J. (2019). Big Data y educación: un enfoque innovador para la toma de decisiones. Universidad Nacional de Colombia.
Ministerio de Educación Nacional. (2021). Sistema Nacional de Información de la Educación Superior (SNIES).
