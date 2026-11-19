# Anexo de Uso de IA y Componentes Reutilizados

## Componentes Externos Reutilizados
* **Ultralytics YOLOv8s-Worldv2 & MobileSAM** (Licencia AGPL-3.0): Detección abierta por texto y segmentación por instancia píxel a píxel.
* **Torchvision MobileNetV2** (Pesos ImageNet, Licencia BSD-3): Clasificación binaria (`Sano` vs. `Deteriorado`).
* **Gradio** (Licencia Apache 2.0): Interfaz web interactiva para pruebas en vivo y ajuste de umbrales.

## Trazabilidad de Apoyo con IA Generativa
Se utilizó IA generativa como apoyo para estructurar la documentación bajo metodología CRISP-DM, verificar la partición sin fuga de datos (`70/15/15`) en PyTorch y ajustar las dimensiones de máscaras entre `YOLO-World` y `MobileSAM`. Todas las decisiones experimentales (elección de *Cocos nucifera*, criterios de deterioro, calibración de umbrales en Gradio, ejecución en Google Colab y análisis de errores) fueron definidas, ejecutadas y validadas por **Juan Diego Mercado, Aizar Racero y Diego Caro**.
