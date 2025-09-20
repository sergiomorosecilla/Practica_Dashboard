
📊 Proyecto: Dashboard & Análisis de Datos
📌 Descripción

Este proyecto forma parte del módulo Dashboard & Análisis de Datos y, a partir de un conjunto de datos de libre elección, he realizado un análisis exploratorio de datos (EDA) y construido un dashboard en Excel, redactando un informe explicativo con las principales conclusiones.

En mi caso me he decantado por bases de datos sobre temporadas de partidos de torneos de la ATP, con el objetivo de mostrar la magnitud de la leyenda del Big Three (Rafael Nadal, Roger Federer y Novak Djokovic), centrado en los años en los que han coincidido al menos dos de ellos (temporadas 2003 a 2024).

📂 Estructura del repositorio

El repositorio contiene los siguientes archivos y carpetas:

Carpeta temporada con datos de las temporadas 1998 a 2024 sobre los partidos de los diferentes torneos de todos los niveles de la ATP.

Archivo Jupyter Notebook con el merge de todos los datos.

Archivo estadísticas_atp_1998_2024.csv creado desde el Jupyter Notebook, destinado al desarrollo del EDA y Dashboard en Excel.

🔎 Metodología seguida

Selección del dataset

Dataset elegido: https://github.com/JeffSackmann

Fuente: https://github.com/JeffSackmann/tennis_atp.git

Dimensiones iniciales: 327.324 registros y 49 columnas. Tras la limpieza (eliminación de torneos por equipos como Copa Davis y creación de nuevas columnas para separar el Big Three) quedaron 58.998 registros y 57 columnas.

**Transformación y limpieza**

Procesos realizados:

Modificación de la columna tourney_date a formato fecha.

No existe columna de identificador único.

Revisión manual de las columnas.

El valor 36 en winner_seed y loser_seed se usa como referencia para agrupar NO cabezas de serie.

El valor DD en winner_entry y loser_entry se usa como referencia para agrupar los que entran directamente a cuadro (Direct Draw).

Creación de una columna binaria para identificar al Big Three (1 si es Federer, Nadal o Djokovic; 0 si es el resto).

Creación de la columna año para segmentar por temporadas.

**Dashboard**

<img width="1242" height="680" alt="image" src="https://github.com/user-attachments/assets/92cf77a3-468d-4bf0-ba26-9268539098c8" />


KPIs representados: total de partidos ganados y porcentaje, total de torneos ganados y porcentaje, así como clasificaciones Top 10 en títulos, aces y break points salvados.

Tipos de visualización utilizados:

Tablas dinámicas para los KPIs.

Gráficos circulares 3D para la proporción Big Three vs resto.

Gráficos de columnas agrupadas por año para mostrar el dominio temporada a temporada.

Segmentadores añadidos: año (temporada), superficie y nivel de torneo.

**Informe explicativo**
Conclusiones principales:

Dominio absoluto: El Big Three no solo gana más del 80% de sus partidos individuales, sino que también concentra un 20% de todos los títulos del circuito en dos décadas.

Consistencia temporal: Mantienen un nivel top durante más de 15 años consecutivos, algo inédito en la historia del tenis.

Versatilidad y fortaleza: No solo ganan títulos, también lideran en métricas de servicio (aces) y en defensa (break points salvados), demostrando un dominio integral del juego.
Nota: los datos de Federer no son completos, ya que su carrera se inició en 1998, pero se ha acotado el análisis a la etapa en que coincidieron al menos dos miembros del Big Three para mantener la relevancia de los datos.

Legado histórico: Comparados en conjunto, se consolidan como el bloque más dominante en la era profesional, con una ventaja clara frente al resto de jugadores ATP.


