# Pokédex - Primer Parcial

Este proyecto es una aplicación Android que implementa una lista de Pokémon (Pokédex) siguiendo los estándares de arquitectura moderna y desarrollo declarativo.

## 🚀 Arquitectura y Tecnologías

La aplicación ha sido refactorizada para implementar el patrón **MVVM (Model-View-ViewModel)** con **UDF (Unidirectional Data Flow)**:

*   **Jetpack Compose**: Interfaz de usuario 100% declarativa.
*   **Material Design 3**: Uso de componentes y sistema de diseño actual.
*   **ViewModel & StateFlow**: Gestión de estado reactiva y manejo de ciclo de vida.
*   **Repository Pattern**: Desacoplamiento de la fuente de datos de la lógica de UI.
*   **Coil**: Librería para carga y caché de imágenes de Pokémon.
*   **State Hoisting**: Aplicado para crear componentes Stateless y reutilizables.

## 📂 Estructura del Proyecto (Clean Architecture)

El código se organiza bajo el paquete `edu.uade.primerparcial`:

*   `model/`: Entidades de datos (ej. `Pokemon`).
*   `data/`: Repositorios para el manejo de información.
*   `ui/state/`: Representación del estado de la pantalla (`UiState`).
*   `ui/viewmodel/`: Lógica de presentación y comunicación con el repositorio.
*   `ui/screens/`: Pantallas de alto nivel (Screen-Content pattern).
*   `ui/components/`: Micro-componentes visuales.
*   `ui/theme/`: Configuración de Material 3 (Colores, Tipografía, Shapes).

## 🛠️ Requisitos e Instalación

1.  Abrir el proyecto en **Android Studio**.
2.  Realizar un **Gradle Sync**.
3.  Ejecutar la app en un dispositivo con API 26 o superior.

---
*Refactorizado por un Android Senior para cumplir con los principios de Clean Code.*
