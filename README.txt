SISTEMA DE GESTIÓN DE PAÍSES


INTRODUCCIÓN

El presente trabajo fue realizado en conjunto por Alan Monzón y Joaquín Montero, siendo las tareas divididas de forma dinámica dado que ambos tuvimos incidencia en la confección de todas las partes del código (main menu + funciones)

Este programa es una aplicación de consola en Python para gestionar una lista de países, permitiendo al usuario cargarlos, agregarlos, actualizarlos, buscarlos, filtrarlos, ordenarlos y obtener estadísticas básicas.

Los datos de los países se almacenan en un archivo CSV (paises.csv).

REQUISITOS PREVIOS

Es preciso tener instalado Python 3.

De la misma forma asegurarse de que main.py y funciones.py se encuentran en la misma carpeta.

USO

Asegurate de tener los archivos main.py y funciones.py en el mismo directorio.

Ejecuta el programa principal desde la terminal:

python main.py

El menú principal se mostrará, y podrás interactuar con las siguientes opciones. Si el archivo paises.csv no existe, se creará uno nuevo al momento de guardar datos.

FUNCIONAMIENTO DEL MENÚ

Agregar país: Permite ingresar un nuevo país con su nombre, población, superficie y continente. Valida que los campos no estén vacíos y que el país no sea un duplicado.

Actualizar datos de un país: Permite modificar la población y la superficie de un país existente, buscándolo por nombre.

Buscar país: Permite buscar países por coincidencia parcial o exacta de su nombre, mostrando una lista de resultados.

Filtrar países: Ofrece opciones para listar países basándose en:

Continente

Rango de población

Rango de superficie

Ordenar países: Permite reordenar la lista de países por:

Nombre (alfabético)

Población (ascendente)

Superficie (ascendente o descendente)

Mostrar estadísticas: Calcula y muestra indicadores clave:

País con mayor y menor población.

Promedio de población y superficie.

Cantidad de países por continente.

Salir: Termina la ejecución del programa.

ESTRUCTURA DE ARCHIVOS

main.py: Contiene la lógica del menú principal y el flujo de la aplicación.

funciones.py: Contiene todas las funciones de gestión de datos (cargar, guardar, agregar, actualizar, buscar, filtrar, ordenar y estadísticas) que operan sobre la lista de países.

paises.csv: Archivo utilizado para la persistencia de datos.

FUNCIONES CLAVE (en funciones.py)

cargar_paises(nombre_archivo): Lee el CSV, convierte los datos a una lista de diccionarios y maneja errores de formato/archivo no encontrado.

guardar_paises(nombre_archivo, paises): Sobrescribe el CSV con los datos actuales de la lista.

agregar_pais(paises): Solicita los datos de un nuevo país y lo agrega a la lista. No permite campos vacíos ni duplicados.

actualizar_pais(paises): Permite modificar la población y superficie de un país existente.

buscar_pais(paises): Busca un país por coincidencia parcial o exacta del nombre.

filtrar_paises(paises): Permite filtrar países por continente, rango de población o superficie.

ordenar_paises(paises): Ordena los países por nombre, población o superficie.

mostrar_estadisticas(paises): Implementa los cálculos para obtener el máximo/mínimo, promedios y el conteo por continente.

EJEMPLOS DE ENTRADAS/SALIDAS

EJ1:

Entrada

> Seleccione una opción: 1
> Nombre del país: Uruguay
> Población: 3400000
> Superficie (km²): 176215
> Continente: América

Salida

País 'Uruguay' agregado con éxito.
Datos guardados correctamente.

EJ2:

Entrada

> Seleccione una opción: 3
> Ingrese el nombre (o parte) del país a buscar: gent

Salida

Resultados encontrados:
- Argentina | Población: 45,808,000 | Superficie: 2,780,400 km² | América

EJ3:

Entrada

> Seleccione una opción: 6

Salida

📊 ESTADÍSTICAS
- País con mayor población: China (1,402,000,000)
- País con menor población: Uruguay (3,400,000)
- Promedio de población: 350,200,000
- Promedio de superficie: 3,500,000 km²
- Cantidad de países por continente:
  • Asia: 1
  • América: 2


