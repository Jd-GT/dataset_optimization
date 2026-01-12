# 🏡 Optimización de Predicción de Precios: California Housing

Este proyecto explora la evolución de un modelo predictivo, desde una Regresión Lineal simple hasta un modelo Polinómico Regularizado, aplicando técnicas avanzadas de Machine Learning para controlar el Underfitting y Overfitting.

## 🎯 Objetivo
Predecir el precio medio de viviendas en distritos de California, minimizando el Error Cuadrático Medio (MSE) y maximizando la varianza explicada ($R^2$).

## 🛠️ Tecnologías y Conceptos Clave
* **Python** (Pandas, NumPy, Matplotlib, Seaborn)
* **Scikit-Learn** (Pipelines, Preprocessing)
* **Ridge Regression**: Para manejar la multicolinealidad y penalizar coeficientes complejos.
* **Polynomial Features**: Para capturar relaciones no lineales en los datos.
* **Grid Search CV**: Para la optimización sistemática de hiperparámetros ($\alpha$).

## 📊 Evolución del Modelo

| Modelo | $R^2$ Score | MSE | Diagnóstico |
| :--- | :---: | :---: | :--- |
| **Lineal Simple** | 0.6302 | 0.4937 | **Underfitting**: El modelo era demasiado simple para capturar la realidad del mercado. |
| **Polinómico (Grado 2)** | 0.6102 | 0.5205 | **Overfitting**: No era el objetivo ya que el modelo memorizó el ruido y falló en validación. |
| **Polinómico + Ridge ($\alpha=100$)** | 0.6941 | 0.4084 | **Optimizado**: Equilibrio ideal entre sesgo y varianza. |
| **Polynomial Features + Log-Transform** | **0.7090** | **0.3886** | **Best Fit**: Manejo de la asimetría en la variable precio. |

## 🚀 Observaciones 
1.  **Diagnóstico de Errores**: Identificar cuándo un modelo es "demasiado simple" vs "demasiado complejo".
2.  **El Poder de Ridge**: Cómo el hiperparámetro Alpha actúa como una "un metodo control" para domar modelos polinómicos inestables.
3.  **Grid Search**: La importancia de no adivinar los parámetros, sino probarlos sistemáticamente con Validación Cruzada.

## 📈 Resultado Final
La gráfica compara el desempeño inicial del modelo lineal (línea azul) frente al modelo polinómico optimizado (línea verde), evidenciando una mejora del ~10% en la precisión.
<img width="1149" height="633" alt="image" src="https://github.com/user-attachments/assets/42706414-d954-4a37-b1e3-07364493a393" />

Exprimiendo lo maximo que se puede sacar con Log Transform
<img width="588" height="134" alt="image" src="https://github.com/user-attachments/assets/328255e6-f87f-4b61-af65-f778434ff164" />
