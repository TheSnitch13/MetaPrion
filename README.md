# 🧬 MetaPrion v1.0  
**Simulación metaheurística de la conversión de proteínas priónicas**

---

## 📘 Descripción general

**MetaPrion** es un software científico diseñado para **modelar y optimizar el proceso de conversión conformacional de proteínas priónicas (PrP<sup>C</sup> → PrP<sup>Sc</sup>)** utilizando algoritmos metaheurísticos.  
El sistema permite explorar el paisaje energético de la proteína, identificar estados intermedios y visualizar trayectorias de conversión que podrían explicar la aparición de formas patológicas.

MetaPrion combina la **biofísica computacional**, la **optimización multiobjetivo** y la **visualización científica interactiva**, convirtiéndose en una herramienta de simulación accesible y reproducible.

---

## ⚙️ Características principales

- Interfaz web científica en tonos metálicos grises y blancos.  
- Módulo de configuración y validación de parámetros de simulación.  
- Ejecución de algoritmos metaheurísticos en tiempo real.  
- Visualización dinámica de energía, Rg, RMSD y frente de Pareto.  
- Exportación de resultados (`metrics.csv`, `pareto.json`, `log.txt`, `config.json`).  
- Historial de simulaciones y trazabilidad completa (`metadata.json`).  
- Sección de ayuda con documentación de algoritmos y métricas.

---

## 🧠 Algoritmos implementados

| Algoritmo | Tipo | Objetivos | Descripción breve |
|------------|------|-----------|-------------------|
| **SA – Simulated Annealing** | Monoobjetivo | Minimizar energía libre | Simula enfriamiento físico para escapar de óptimos locales y hallar mínimos globales. |
| **NSGA-II** | Multiobjetivo | Min. energía / Max. similitud / Max. estabilidad | Usa dominancia de Pareto para equilibrar varios objetivos. |
| **NSGA-III** | Multiobjetivo avanzado | 3–4 objetivos simultáneos | Extiende NSGA-II con “reference points” para optimizar más de tres métricas. |

---

## 📊 Métricas de análisis

| Métrica | Unidad | Objetivo | Interpretación |
|----------|---------|-----------|----------------|
| Energía libre (*E*) | kcal/mol | Minimizar | Estado más estable del sistema. |
| Radio de giro (*Rg*) | nm | Minimizar | Compactación estructural (plegamiento). |
| RMSD | nm | Observacional | Cambio estructural respecto a referencia. |
| Estabilidad (*S*) | adimensional | Maximizar | Permanencia de un estado estructural. |
| Similitud (*Sim*) | 0–1 | Maximizar | Cercanía con el modelo priónico conocido. |

---

## 🧩 Arquitectura general del sistema
MetaPrion/
│
├── src/
│ ├── algorithms/
│ │ ├── sa.py
│ │ ├── nsga2.py
│ │ └── nsga3.py
│ ├── core/
│ │ ├── pipeline.py
│ │ ├── validation.py
│ │ └── scoring.py
│ ├── analysis/
│ │ ├── metrics.py
│ │ └── visualization.py
│ └── app.py
│
├── runs/
│ ├── 2025-11-10_001/
│ │ ├── config.json
│ │ ├── metrics.csv
│ │ ├── pareto.json
│ │ └── log.txt
│
├── docs/
│ ├── Manual_de_Usuario.pdf
│ ├── SDD_MetaPrion.pdf
│ └── README.md
│
└── requirements.txt


---

## 🧭 Innovación del proyecto

MetaPrion es pionero al:
- Modelar la conversión priónica como un **problema de optimización multiobjetivo**.  
- Combinar **biofísica computacional** con **metaheurísticas evolutivas**.  
- Presentar resultados **en tiempo real con visualización 3D y análisis de Pareto**.  
- Ser **modular, reproducible y ampliable** para investigaciones biomoleculares futuras.

---


📘 Créditos

Proyecto: MetaPrion
Autores: Equipo de desarrollo académico
Año: 2025
Institución: Proyecto Modular – Simulación Metaheurística de la Conversión de Proteínas Priónicas
Licencia: MIT
