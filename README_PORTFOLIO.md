# ⚔️ K A I R O S  R H Y T H M O S
![Banner Concept](assets/banner_kairos.png)

**Autor:** Leonardo Ahumada (+ Antigravity Co-Pilot)  
**Versión:** 1.0 (MVP Espartano)

---

## 🎬 Demo Completa (Video)

[![Ver en YouTube](https://img.youtube.com/vi/4qZCabFRvFs/maxresdefault.jpg)](https://www.youtube.com/watch?v=4qZCabFRvFs)
*(Clic en la imagen para ver la demostración narrada de la arquitectura y UX "Espartana")*

---

## 📸 Galería Visual (Showcase)

| El Reloj Táctico | Modo Focus (Arena) | Edición Inteligente |
| :---: | :---: | :---: |
| ![Reloj](assets/transcursoTiempo.gif) | ![Focus](assets/focusTime.gif) | ![Notif](assets/notificacion.gif) |

---

## 📄 Descripción del Proyecto

**Kairos Rhythmos** no es otra lista de tareas. Es un **Sistema de Combate contra la Procrastinación** diseñado bajo la filosofía del estoicismo y la gestión temporal agresiva. 
Más allá del producto, este proyecto es una demostración técnica avanzada de **Kotlin Multiplatform (KMP)** y **Compose Multiplatform**.

### 📱 Estado del Proyecto
| Plataforma | Estado | Nivel de Soporte |
| :---: | :---: | :--- |
| ![Android Badge](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white) | **Producción** | Alertas de Alta Prioridad ("Mini-Kairos"), Vibración Infinita, UI Nativa. |
| ![iOS Badge](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=apple&logoColor=white) | **Producción** | UI Compartida al 100%, Persistencia Nativa (NSUserDefaults). |
| ![Desktop Badge](https://img.shields.io/badge/Desktop-JVM-blue?style=for-the-badge) | **Tooling** | Entorno de desarrollo rápido y validación de lógica pura. |

---

## 🏛️ Filosofía de Arquitectura

1.  **Kairos (Oportunidad) vs Chronos (Reloj):** La app visualiza el tiempo como arcos físicos de "Masa" y "Gravedad".
2.  **Disciplina Espartana:** El sistema no sugiere, obliga. En Android, utiliza `FullScreenIntent` y vibración en bucle.
3.  **Monolito Espartano:** UI compartida al 99%.

---

## 🛠️ Stack Tecnológico

* **Lenguaje:** Kotlin 2.0+ (K2 Compiler).
* **UI Framework:** Jetpack Compose Multiplatform (Material 3).
* **Persistencia Profunda:** AndroidX Room KMP (SQLite nativo embebido).
* **Persistencia Ligera:** Implementación propia de `Expect/Actual`.

---

## 🧬 Diagrama de Arquitectura

```mermaid
graph TD
    subgraph Common Main [Cerebro Compartido (95%)]
        UI[Compose UI (Reloj, Screens)]
        VM[ViewModel]
        DOM[Dominio]
        REP[Repositorio]
    end
    
    subgraph Android Main [Músculo Android]
        ACT[Activity]
        ALARM[AlarmManager]
    end

    subgraph iOS Main [Agilidad iOS]
        VC[MainViewController]
        NOTIF_IOS[UNUserNotificationCenter]
    end

    UI --> VM
    VM --> DOM
    DOM --> REP
    REP --> DB[(SQLite / Room)]
    ACT --> UI
    VC --> UI
```

---

## � Documentación Detallada

Para profundizar en las decisiones de diseño, algoritmos matemáticos y diagramas de flujo detallados, consulta el informe técnico completo:

### [� LEER INFORME TÉCNICO DE INGENIERÍA (Markdown)](docs/INFORME_TECNICO_KAIROS.md)

---
*Kairos Rhythmos - Forjado en código, templado en disciplina.*
