# Calculadora de IMC

Este es un proyecto de Android en Kotlin que implementa una calculadora de Índice de Masa Corporal (IMC) utilizando Jetpack Compose.

## Características
- Permite ingresar el peso en kilogramos.
- Permite ingresar la altura en centímetros.
- Calcula automáticamente el IMC.
- Muestra la categoría correspondiente del IMC.
- Diseño moderno con Jetpack Compose.

## Requisitos
- Android Studio Arctic Fox o superior.
- Kotlin 1.5 o superior.

## Instalación
1. Abre el proyecto en Android Studio.
2. Compila y ejecuta la aplicación en un dispositivo o emulador.

## Uso
1. Introduce tu peso en kilogramos.
2. Introduce tu altura en centímetros.
3. La aplicación calculará y mostrará tu IMC junto con su categoría.

## Código principal
El código principal de la calculadora está en `MainActivity.kt`.  
La función `calculateBMI` realiza el cálculo y `getBMICategory` determina la categoría del IMC.

![Código principal](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Codigoprincipal.jpg)

## Capturas de Pantalla
![Captura de pantalla 1](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Captura%20de%20pantalla.jpg)  
![Captura de pantalla 2](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Capturadepantallados.jpg)  

## Test Unitario realizado
![Captura de pantalla del test realizado](Capturas%20Pantalla%20IMC/Test.jpg)

Este test unitario verifica que:
1. La función `calculateBMI()` devuelve los valores correctos de IMC.
2. La función `getBMICategory()` clasifica correctamente el IMC en una categoría.
3. Se manejan correctamente los casos borde (altura = 0).

## Test de Interfaz realizado
![Captura de pantalla del test realizado](Pantallas_IMC/TestdeInterfaz.jpg)

Este código es una prueba de UI en Jetpack Compose que:
- Renderiza la pantalla de cálculo de IMC.
- Simula la entrada de datos del usuario.
- Hace clic en el botón de cálculo.
- Verifica que el resultado mostrado es el esperado.

Esto asegura que la funcionalidad de cálculo de IMC en la interfaz gráfica funciona correctamente.

---

## Autor: Sergio Rodríguez Guerrero

