# Control de Calidad de Cocos (*Cocos nucifera*) mediante Segmentación por Instancia

Prototipo de visión artificial desarrollado para la asignatura **Aprendizaje Computacional** (Universidad de Córdoba — Docente: Oswaldo Vélez Langs, PhD).

## Integrantes
* **Juan Diego Mercado**
* **Aizar Racero**
* **Diego Caro**

## Propósito del Sistema
A partir de una fotografía con múltiples cocos, el sistema delimita cada fruto individualmente mediante segmentación por instancia, clasifica su estado sanitario (**Sano** o **Deteriorado**) y entrega un conteo resumen del lote a través de una interfaz web en **Gradio**.

## Arquitectura (Ruta A: Desacoplada)
1. **Detección abierta:** `YOLOv8s-Worldv2` ubica cada coco en escena (`prompt: coconut`).
2. **Segmentación por instancia:** `MobileSAM` recorta la silueta exacta píxel a píxel de cada fruto para eliminar el fondo.
3. **Clasificación sanitaria:** `MobileNetV2` (entrenada con partición anti-fuga 70/15/15 y aumentos coherentes imagen+máscara) evalúa cada recorte y etiqueta en verde (`SANO`) o rojo (`DETERIORADO`).

## Estructura del Repositorio
* `notebooks/prototipo_dia7_cocos.ipynb`: Cuaderno ejecutable en Google Colab con descarga filtrada desde iNaturalist, entrenamiento y app Gradio.
* `docs/`: Informe de avance en PDF (`Avance_Dia7_Control_Calidad_Cocos.pdf`).
* `pruebas_demo/`: Imágenes multifruta utilizadas para validar aciertos y fallos.
* `BITACORA.md`: Registro cronológico de problemas, hipótesis y mejoras.
* `ANEXO_IA.md`: Componentes reutilizados y trazabilidad de apoyo con IA.
