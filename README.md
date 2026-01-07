# 🫁 COVID-19 Lung CT Segmentation

Este proyecto implementa una arquitectura de **Deep Learning (U-Net)** para la segmentación automática de lesiones pulmonares causadas por COVID-19 en Tomografías Computarizadas (CT-Scans).

El modelo utiliza estrategias de **Transfer Learning** integrando un encoder **MobileNetV2** pre-entrenado para optimizar la extracción de características en datasets médicos limitados.

## 🚀 Características Técnicas

* **Arquitectura:** U-Net (Encoder-Decoder) con conexiones residuales.
* **Backbone:** MobileNetV2 (ImageNet Weights) para eficiencia computacional.
* **Métrica de Optimización:** Implementación manual de **Dice Loss** (específico para segmentación semántica médica).
* **Procesamiento de Datos:** Manejo de imágenes médicas formato **NIfTI** (.nii) y normalización de unidades Hounsfield.

## 🛠 Tech Stack

* **Core:** Python 3.x
* **Deep Learning:** TensorFlow 2.x / Keras
* **Computer Vision:** OpenCV, Nibabel (Medical Imaging)
* **Data Analysis:** Pandas, NumPy

## 📊 Metodología de Entrenamiento

1.  **Pre-processing:** Conversión de volúmenes CT 3D a cortes 2D y normalización.
2.  **Training:** Entrenamiento con encoder congelado (Frozen Weights).
3.  **Fine-Tuning:** Descongelamiento progresivo de capas superiores para adaptación específica al dominio médico.
4.  **Evaluation:** Validación mediante Coeficiente Dice y Visualización de Máscaras.

---
*Developed by Darwin Caceres - Computer Engineering Student @ PUCP*
