# sakila-crud-orm
Caso Práctico 2 MACDIA — CRUD/ORM nativo en Python sobre MySQL Sakila
=========================================================================
   UNIVERSIDAD AUTÓNOMA DE SANTO DOMINGO (UASD)
   FACULTAD DE CIENCIAS - MAESTRÍA EN DATA SCIENCE & AI
   ASIGNATURA: CIENCIA DE DATOS I - GRUPO PETER NAUR
=========================================================================

GUÍA DE DESPLIEGUE: PASO A PASO PARA EJECUTAR EL PROYECTO

Para inicializar la arquitectura ORM y auditar correctamente el esquema 
de base de datos, debes ejecutar los componentes siguiendo este orden 
secuencial estricto:

-------------------------------------------------------------------------
Paso 1: Configuración de la Base de Datos en MySQL Workbench
-------------------------------------------------------------------------
Antes de levantar la aplicación en Python, es obligatorio asegurar la 
consistencia del catálogo relacional.

1. Abre MySQL Workbench e ingresa a tu instancia relacional local.
2. Abre y ejecuta el script completo llamado "Consultas SQL Sakila.sql"[cite: 3].
3. Este script aplicará de manera automática las restricciones de 
   integridad únicas (DDL) sobre las tablas core para mitigar la duplicidad 
   de registros huérfanos antes de la ingesta de datos[cite: 3]:

   USE sakila;
   ALTER TABLE country ADD CONSTRAINT unique_country UNIQUE (country);
   ALTER TABLE city ADD CONSTRAINT unique_city_country UNIQUE (city, country_id);
   ALTER TABLE film ADD CONSTRAINT unique_film_title UNIQUE (title, release_year);

-------------------------------------------------------------------------
Paso 2: Instalación de Dependencias Técnicas
-------------------------------------------------------------------------
Asegúrate de contar con las librerías necesarias ejecutando el siguiente 
comando en tu terminal, consola o símbolo del sistema (cmd):

pip install sqlalchemy pymysql pandas matplotlib seaborn numpy

-------------------------------------------------------------------------
Paso 3: Lanzar la Capa de Control Interactiva ("Flujo.py")
-------------------------------------------------------------------------
Este archivo orquesta la navegación de todo el sistema a través de menús 
interactivos desplegados en la consola[cite: 4].

1. Abre tu terminal en la carpeta física donde guardaste los archivos.
2. Corre el script principal con el siguiente comando:
   
   python Flujo.py

3. El sistema llamará dinámicamente a "Data Sakila.py" para establecer 
   la conexión segura mediante la clase DbContext[cite: 4].

4. Funciones Operativas del Menú de Consola:
   * Opción 1: Calcula en tiempo real las métricas descriptivas y de 
     relación lineal (como la covarianza) usando procesamiento nativo 
     en memoria sin librerías externas de persistencia[cite: 4].
   * Opción 2: Corre de forma automática e indexada las 15 consultas 
     analíticas de auditoría oficial, mostrando sus resultados directos 
     en la pantalla como evidencia técnica de la corrida.
   * Opción 3: Ejecuta un caso de uso CRUD inyectando una nueva entidad 
     de película mapeada dentro de la base de datos relacional.
   * Opción 4: Convierte y serializa las colecciones list<object> en 
     archivos planos de intercambio listos para el negocio en formatos 
     estándar .csv y .json[cite: 4].

-------------------------------------------------------------------------
Paso 4: Generar el Respaldo Gráfico Avanzado ("Entregables.py")
-------------------------------------------------------------------------
Una vez ejecutada la auditoría del menú, corre el módulo gráfico 
especializado para producir las figuras de densidad científica requeridas 
para el informe escrito final[cite: 5]:

1. En tu terminal, ejecuta el script analítico visual:

   python Entregables.py

2. El script extraerá automáticamente las tendencias agregadas de la 
   base de datos (como el promedio de duración por clasificación de la 
   Consulta 15 y el volumen por categorías de la Consulta 8) utilizando 
   queries nativos conectados al motor local[cite: 5].
3. Las imágenes de alta definición se guardarán de manera directa en tu 
   ruta física preestablecida de entregables de la maestría[cite: 5].

=========================================================================
Fin del Instructivo Operativo - 2026
=========================================================================
