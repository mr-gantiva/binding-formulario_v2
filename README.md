# Proyecto de Formulario en Vue

Este proyecto es una aplicación desarrollada con Vue.js que incluye un formulario con diversos tipos de campos como entradas de texto, selecciones, botones de radio, casillas de verificación y áreas de texto. Los datos ingresados por el usuario se actualizan y muestran en tiempo real en la interfaz.

## Demo
Puedes ver una demo del proyecto funcionando en el siguiente enlace: [Demo](https)

## Tabla de Contenidos

- [Proyecto de Formulario en Vue](#proyecto-de-formulario-en-vue)
  - [Demo](#demo)
  - [Tabla de Contenidos](#tabla-de-contenidos)
  - [Descripción del Proyecto](#descripción-del-proyecto)
  - [Tecnologías Utilizadas](#tecnologías-utilizadas)
  - [Instalación](#instalación)
  - [Uso](#uso)
    - [Elementos del Formulario](#elementos-del-formulario)
  - [Componentes](#componentes)
  - [Estilos](#estilos)

## Descripción del Proyecto

Esta aplicación en Vue permite a los usuarios llenar un formulario y ver los resultados reflejados en tiempo real en el lado derecho de la página. El formulario incluye:

- **Título**: Un campo de texto para ingresar una descripción de lo que se está aprendiendo.
- **Selector de Emoji**: Un menú desplegable con opciones de emojis.
- **Apreciación**: Botones de radio para calificar la experiencia de aprendizaje.
- **Competencias Aprendidas**: Casillas de verificación para seleccionar las habilidades adquiridas.
- **Opinión**: Un área de texto para proporcionar comentarios adicionales.

## Tecnologías Utilizadas

- **Vue 3**: Utiliza la Composition API para gestionar el estado y propiedades computadas.
- **Bootstrap**: Para el diseño responsivo y estilos básicos.
- **CSS**: Estilos personalizados aplicados con `scoped` para limitar su alcance al componente.

## Instalación

Para ejecutar este proyecto localmente, sigue los siguientes pasos:

1. **Clona el repositorio**:
    ```bash
    git clone https://github.com/mr-gantiva/binding-formulario_v2
    ```

2. **Navega al directorio del proyecto**:
    ```bash
    cd binding-formulario_v2
    ```

3. **Instala las dependencias**:
    ```bash
    npm install
    ```

4. **Inicia el servidor de desarrollo**:
    ```bash
    npm run dev
    ```

## Uso

Una vez que el servidor esté en funcionamiento, puedes abrir la aplicación en tu navegador. Completa el formulario y verás los resultados actualizados en tiempo real en el lado derecho de la página.

### Elementos del Formulario

- **Título**: Campo de texto para ingresar una descripción.
- **Selector de Emoji**: Menú desplegable para seleccionar un emoji.
- **Apreciación**: Botones de radio para seleccionar una valoración.
- **Competencias Aprendidas**: Casillas de verificación para seleccionar las habilidades adquiridas.
- **Opinión**: Área de texto para comentarios adicionales.

## Componentes

- **Sección del Formulario**: Los campos de entrada del formulario están definidos en la sección `<template>`.
- **Gestión del Estado**: Utiliza las funciones `ref` y `computed` de la Composition API de Vue para gestionar el estado del formulario.

## Estilos

Los estilos personalizados se aplican al formulario utilizando CSS con el atributo `scoped`. La sección izquierda del formulario tiene un fondo semi-transparente con un efecto de desenfoque, mientras que la sección derecha utiliza un fondo claro con texto oscuro para un mejor contraste.

```css
.container {
  color: #fff;
}

.left__side {
  background: rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
}

:is(.left__side, .right__side) {
  border-radius: 10px;
  padding: 20px;
}

.right__side {
  background-color: #fff;
  color: #202b38;
}
```
