# Pokédex - Primer Parcial

Este proyecto es una aplicación Android que implementa una lista de Pokémon (Pokédex) siguiendo los estándares de arquitectura moderna y desarrollo declarativo.

## 🚀 Arquitectura y Tecnologías

La aplicación implementa el patrón **MVVM (Model-View-ViewModel)** con **UDF (Unidirectional Data Flow)**:

*   **Jetpack Compose**: Interfaz de usuario 100% declarativa.
*   **Material Design 3**: Uso de componentes y sistema de diseño actual.
*   **ViewModel & StateFlow**: Gestión de estado reactiva y manejo de ciclo de vida.
*   **Repository Pattern**: Desacoplamiento de la fuente de datos de la lógica de UI.
*   **Coil**: Librería para carga y caché de imágenes de Pokémon.
*   **State Hoisting**: Aplicado para crear componentes Stateless y reutilizables.

## 📂 Estructura de Archivos

1.  **Modelo de Datos (`edu.uade.primerparcial.model.Pokemon.kt`)**: Encapsula la lógica de la entidad (formateo de nombre, IDs y URLs de sprites).
2.  **Capa de Datos - Repository (`edu.uade.primerparcial.data.PokemonRepository.kt`)**: Gestiona la fuente de datos. El ViewModel no sabe de dónde vienen los Pokémon.
3.  **Estado de UI (`edu.uade.primerparcial.ui.state.PokemonUiState.kt`)**: Data class que agrupa todo el estado de la pantalla (lista, carga, errores).
4.  **ViewModel (`edu.uade.primerparcial.ui.viewmodel.PokemonViewModel.kt`)**: Implementa UDF usando StateFlow y expone un único UiState.
5.  **Componentes (`edu.uade.primerparcial.ui.components.PokemonItem.kt`)**: Componente Stateless para representar cada ítem de la lista.
6.  **Pantallas (`edu.uade.primerparcial.ui.screens.PokemonListScreen.kt`)**: Separa la lógica de obtención de estado (Screen) de la representación visual (Content).
7.  **MainActivity (`MainActivity.kt`)**: Limpia y simplificada, actuando solo como punto de entrada.

## ✨ Cambios Realizados

*   **Adiós al "God Composable"**: La lógica de la lista y los ítems ahora están en archivos separados.
*   **Unidirectional Data Flow**: El estado fluye desde el ViewModel a la vista, y los eventos suben al ViewModel.
*   **State Hoisting**: Los componentes visuales son stateless y reciben los datos necesarios por parámetros.
*   **Limpieza Total**: Se eliminaron los comentarios en otros idiomas y funciones redundantes (como Greeting) que no aportaban al proyecto.

## 🛠️ Requisitos e Instalación

1.  Abrir el proyecto en **Android Studio**.
2.  Realizar un **Gradle Sync**.
3.  Ejecutar la app en un dispositivo con API 26 o superior.

---
*El proyecto ahora es escalable, testeable y sigue los estándares de la industria.*
