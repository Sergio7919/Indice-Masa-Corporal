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
- Redactar interfaz de usuario.

## Instalación
1. Abre el proyecto en Android Studio.
2. Compila y ejecuta la aplicación en un dispositivo o emulador.

## Uso
1. Introduce tu peso en kilogramos.
2. Introduce tu altura en centímetros.
3. La aplicación calculará y mostrará tu IMC junto con su categoría.

## Código principal
El código principal de la calculadora está en MainActivity.kt. 
La función calculateBMI realiza el cálculo y getBMICategory determina la categoría del IMC.

![Codigo principal](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Codigoprincipal.jpg)

## Captura de Pantalla
![Captura de pantalla](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Captura%20de%20pantalla.jpg)
![Captura de pantalla](Imagenes%20de%20capturas%20de%20pantalla%20calculadora%20IMC/Capturadepantallados.jpg)

## Test realizado
Este es un test unitario escrito en Kotlin usando JUnit para probar una calculadora de índice de masa corporal (IMC o BMI por sus siglas en inglés).
Explicación del código
1.	Importaciones
import org.junit.Assert.assertEquals
import org.junit.Test
o	Se importan las funciones necesarias de JUnit para realizar pruebas unitarias.
2.	Definición de la clase de prueba
class BMICalculatorTest {
o	Es una clase de prueba donde se testean las funciones de cálculo de IMC.
________________________________________
Primera prueba: calcuLateBMI_correctValues()
@Test
fun calcuLateBMI_correctValues() {
    assertEquals(22.22, calculateBMI(weight: 70.0, height: 1.78), delta: 0.01)
    assertEquals(24.69, calculateBMI(weight: 80.0, height: 1.80), delta: 0.01)
    assertEquals(0.0, calculateBMI(weight: 70.0, height: 0.0), delta: 0.01) // Caso borde
}
•	Se prueban diferentes valores para calcular el BMI con la función calculateBMI(weight, height).
•	Se usa assertEquals(expected, actual, delta) para verificar que el resultado está dentro de un margen de error (delta) de 0.01.
•	Casos probados:
o	Persona con 70 kg y 1.78 m → BMI esperado: 22.22.
o	Persona con 80 kg y 1.80 m → BMI esperado: 24.69.
o	Caso borde: Peso 70 kg con altura 0.0 → BMI esperado: 0.0 (para evitar divisiones por cero).
________________________________________
Segunda prueba: getBMICategory_correctCategory()
@Test
fun getBMICategory_correctCategory() {
    assertEquals("Bajo peso", getBMICategory(bmi: 17.0))
    assertEquals("Normal", getBMICategory(bmi: 22.0))
    assertEquals("Sobrepeso", getBMICategory(bmi: 27.0))
    assertEquals("Obesidad", getBMICategory(bmi: 32.0))
}
•	Se prueban diferentes valores de BMI con la función getBMICategory(bmi).
•	Casos probados:
o	BMI 17.0 → "Bajo peso".
o	BMI 22.0 → "Normal".
o	BMI 27.0 → "Sobrepeso".
o	BMI 32.0 → "Obesidad".
________________________________________
Funciones auxiliares
1.	Función calculateBMI()
private fun calculateBMI(weight: Double, height: Double): Double {
    return if (height > 0) weight / (height * height) else 0.0
}
o	Calcula el índice de masa corporal usando la fórmula BMI = peso / (altura²).
o	Si la altura es 0, devuelve 0.0 para evitar errores.
2.	Función getBMICategory()
private fun getBMICategory(bmi: Double): String {
    return when {
        bmi < 18.5 -> "Bajo peso"
        bmi < 24.9 -> "Normal"
        bmi < 29.9 -> "Sobrepeso"
        else -> "Obesidad"
    }
}
o	Retorna la categoría según el valor del BMI:
	Menos de 18.5 → "Bajo peso".
	Entre 18.5 y 24.9 → "Normal".
	Entre 25 y 29.9 → "Sobrepeso".
	Más de 30 → "Obesidad".
________________________________________
Conclusión
Este test unitario verifica que:
1.	La función calculateBMI() devuelve los valores correctos de IMC.
2.	La función getBMICategory() clasifica correctamente el IMC en una categoría.
3.	Se manejan correctamente los casos borde (altura = 0).


---
## Autor: Sergio Rodríguez Guerrero
