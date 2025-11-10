# Machine-Learning-in-Bioengieneering - Clasificación Taxonómica a Partir de Sesgos en el Uso de Codones

### Proyecto Final – Bioinformática | Universidad del Norte Santo Tomás de Aquino  
**Autor:** Joaquín Bravo López  

## Descripción del Proyecto

Este proyecto explora cómo el sesgo en el uso de codones puede utilizarse como señal informativa para clasificar organismos en diferentes grupos taxonómicos mediante algoritmos de **Machine Learning**.  A partir del **Codon Usage Dataset (UCI Repository)**, se construyeron y evaluaron modelos supervisados y no supervisados para determinar si las frecuencias de los 64 codones del codigo genetico son suficientes para distinguir entre bacterias, virus, arqueas, plantas y vertebrados, entre otros.

El trabajo combina **biología molecular**, **bioinformática** y **aprendizaje automático**, mostrando cómo los patrones evolutivos se reflejan en la estructura de los datos genéticos.

## Objetivos

- Analizar el **sesgo en el uso de codones** como rasgo distintivo entre grupos taxonómicos.  
- Entrenar y comparar modelos de clasificación supervisada y no supervisada.  
- Evaluar el poder predictivo de algoritmos como **Árboles de Decisión, Random Forest, SVM y MLP**.  
- Validar la generalización mediante una prueba con **CDS reales de NCBI**.

## Metodología

1. **Dataset:**  
   - Fuente: [UCI Machine Learning Repository – Codon Usage Dataset](https://archive.ics.uci.edu/dataset/577/codon+usage)  
   - 13,028 instancias, 64 codones + metadatos taxonómicos  
   - Clases: 11 grupos (bct, arc, vrl, phg, plm, pln, inv, vrt, mam, pri, rod)

2. **Preprocesamiento:**  
   - Normalización con `MinMaxScaler`  
   - Balanceo de clases mediante `class_weight="balanced"`  
   - División en Train / Validation / Test  

3. **Modelos Supervisados:**  
   - Árbol de Decisión  
   - Random Forest  
   - SVM (kernels RBF y Polinomial)  
   - MLP (Multilayer Perceptron con BatchNorm y Dropout)

4. **Modelos No Supervisados:**  
   - PCA (reducción de dimensionalidad)  
   - K-Means y 🔸 Clustering Jerárquico  

5. **Prueba con CDS reales:**  
   - Conversión de secuencias FASTA → frecuencias de codones  
   - Clasificación con modelos entrenados (SVM-RBF y MLP)  
   - Evaluación por margen, confianza y entropía  

Contacto

Joaquín Bravo López
📧 bravojoaquinlo@gmail.com
