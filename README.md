# Manual de Usuario: Esquema de Secreto Compartido de Shamir

## Introducción

Este manual describe la implementación y uso del Esquema de Secreto Compartido de Shamir, una herramienta diseñada para cifrar y descifrar archivos confidenciales mediante un enfoque colaborativo.

## Funcionamiento

El Esquema de Secreto Compartido de Shamir permite ocultar una clave secreta K dentro de un polinomio de grado \(t-1\). Este polinomio se evalúa en \(n\) puntos diferentes, generando fragmentos que pueden ser distribuidos entre los usuarios autorizados. Para recuperar la clave K, se necesitan al menos \(t\) de estos fragmentos.

## Instalación y Requisitos

El programa requiere de bibliotecas de software libre para manejar cifrado AES, SHA-256, y manipulación de números enteros grandes. Asegúrese de tener estas bibliotecas instaladas antes de proceder.

## Uso del Programa

### Modo Cifrado

Para cifrar un archivo:

1. Ejecute el programa con la opción `c`.
2. Proporcione el nombre del archivo para guardar las \(n\) evaluaciones del polinomio.
3. Especifique el número total de evaluaciones requeridas (\(n > 2\)).
4. Indique el número mínimo de puntos necesarios para descifrar (\(1 < t \leq n\)).
5. Ingrese el nombre del archivo con el documento claro.
6. Durante la ejecución, el programa solicitará una contraseña que se utilizará para generar la clave de cifrado.

### Modo Descifrado

Para descifrar un archivo:

1. Ejecute el programa con la opción `d`.
2. Proporcione el nombre del archivo que contiene al menos \(t\) de las \(n\) evaluaciones del polinomio.
3. Ingrese el nombre del archivo cifrado.

## Salidas del Programa

- **Modo Cifrado**: Se generan dos archivos: uno con el documento cifrado y otro con las \(n\) parejas \((x_i, P(x_i))\) de las evaluaciones del polinomio.
- **Modo Descifrado**: Se recupera el documento en su forma original.

## Consideraciones Adicionales

- El programa está diseñado para ser robusto y eficiente.
- Cada función está documentada para explicar su propósito, parámetros y resultados.
- Se incluyen pruebas unitarias para cada módulo.

## Implementación

El programa es una implementación práctica y segura del Esquema de Secreto Compartido de Shamir, enfocado en la protección de información confidencial a través de un enfoque colaborativo. Su diseño permite a los usuarios autorizados acceder a la información cifrada de manera segura y eficiente, siempre que se cumplan los requisitos mínimos de fragmentos recolectados.
