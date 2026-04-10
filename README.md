# Laboratorio 1 - DL Fundamentals: Image Classification with MLP

**Curso:** SI7011 - Deep Learning  
**Entorno:** Kaggle Notebooks / PyTorch  
**Dataset:** Intel Image Classification (6 clases: buildings, forest, glacier, mountain, sea, street)

## Descripción

Implementación de una red neuronal tipo Multilayer Perceptron (MLP) en PyTorch para 
clasificación de imágenes de paisajes naturales. El objetivo es entender el flujo completo 
de entrenamiento y evaluación de un modelo de deep learning desde cero.

## Arquitectura del modelo

| Capa | Detalles |
|------|----------|
| Entrada | 22,500 features (150×150 px, escala de grises) |
| Capa oculta 1 | 128 neuronas + ReLU |
| Capa oculta 2 | 64 neuronas + ReLU |
| Salida | 6 neuronas (softmax implícito vía CrossEntropyLoss) |

## Parámetros de entrenamiento

- **Loss function:** Cross Entropy Loss  
- **Optimizador:** SGD  
- **Learning rate:** 0.01  
- **Batch size:** 32  
- **Épocas:** 10  

## Resultados

| Métrica | Valor |
|---------|-------|
| Train Loss (época 1) | ~1.48 |
| Train Loss (época 10) | ~0.75 |
| Test Loss | 1.579 |
| Test Accuracy | 44% |

## Archivos

- `si7011-dl-mlp-pytorch-daniel-restrepo.ipynb` — Notebook con implementación completa
- `Informe_Daniel_Rpo.pdf` — Informe técnico con descripción de arquitectura y resultados

## Notas

La accuracy de 44% es esperable para un MLP aplicado directamente a imágenes. 
Arquitecturas convolucionales (CNN) capturan mejor los patrones espaciales y 
son el siguiente paso natural para este tipo de tarea.
