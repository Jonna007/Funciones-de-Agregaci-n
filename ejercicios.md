# Tarea TAS9 - Funciones de Agregación

## 1. Obtener la edad promedio de los miembros
  - Sentencia:
  ```sql
    SELECT AVG(EXTRACT(YEAR FROM AGE(birth_date))) AS average_age
    FROM members;
  -Captura:

![sentence01 png](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/9d68aec4-87ba-4062-bcd6-a290c1b9292a)

## 2. Obtener la edad mínima de los miembros
  - Sentencia:
  ```sql
    SELECT MIN(EXTRACT(YEAR FROM AGE(birth_date))) AS minimum_age
    FROM members;
 - Captura:
<img src="![sentence02](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/95c649c5-259c-479f-82ac-018dfad05f30)
" alt="drawing" width="500"/>

## 3. Obtener el número total de registros asistidos
  - Sentencia:
  ```sql
    SELECT COUNT(*) AS total_registrations
    FROM registrations;
  Captura:

![sentence03](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/0b895d35-8c72-47d9-8b91-922e4a5a78f4)

## 4. Obtener el número total de asistentes a todas las conferencias
  - Sentencia:
  ```sql
    SELECT COUNT(DISTINCT member_id) AS total_attendees
    FROM registrations;
  Captura:

![sentence04](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/f6a0f335-ed90-402f-950a-df81f2383011)

## 5. Obtener el número total de eventos por cada ciudad
  - Sentencia:
  ```sql
    SELECT city, COUNT(*) AS total_events
    FROM events
    GROUP BY city;
  Captura:
![sentence05](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/e86ae9ef-0f19-46e3-9feb-f372427f78d0)

## 6. Obtener el número de registros por cada miembro
  - Sentencia:
  ```sql
    SELECT member_id, COUNT(*) AS total_registrations
    FROM registrations
    GROUP BY member_id;
  Captura:

![sentence06](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/16b8aef1-31b8-4d9d-8501-9793c00628ca)

## 7. Obtener el número de registros por cada conferencia
  - Sentencia:
  ```sql
    SELECT event_id, COUNT(*) AS total_registrations
    FROM registrations
    GROUP BY event_id;
  Captura:
![sentence07](https://github.com/Jonna007/Funciones-de-Agregaci-n/assets/146044709/eeda1a27-a308-40d1-bb59-162c807e8470)

