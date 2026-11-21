# Brecha educativa urbano-rural en el Perú

Artículo interactivo sobre la evolución de las desigualdades educativas entre
las áreas urbanas y rurales del Perú durante el periodo 2004–2025. El análisis
usa la ENAHO del INEI y presenta diez gráficos interactivos de Plotly, además
de un árbol de decisión.

## Contenido del proyecto

| Archivo o carpeta | Descripción |
|---|---|
| `articulo_brecha_educativa.html` | Artículo web listo para publicar |
| `portada_brecha_educativa.png` | Imagen de portada |
| `graficos/` | Diez gráficos HTML interactivos |
| `brecha_educativa_exportar_graficos.ipynb` | Notebook para procesar los datos y exportar los gráficos |
| `brecha_educativa_exportar_graficos.py` | Versión Python del notebook |

## Indicadores analizados

El proyecto compara, entre áreas urbana y rural:

- secundaria completa o más;
- estudios universitarios;
- población sin nivel o con primaria incompleta;
- años promedio de estudio;
- analfabetismo;
- matrícula de adolescentes de 12 a 16 años.

También incluye comparaciones por generaciones, departamento, sexo y lengua
materna, y un modelo predictivo basado en un árbol de decisión.

## Generar los gráficos

El notebook está preparado para ejecutarse en Google Colab:

1. Abre `brecha_educativa_exportar_graficos.ipynb` en Google Colab.
2. Ejecuta las celdas en orden.
3. Monta Google Drive cuando Colab lo solicite.
4. Cuando termine, descarga la carpeta `/content/graficos/`.
5. Coloca esa carpeta en el mismo nivel que el archivo HTML.

Los gráficos se generan con los nombres `grafico_01.html` a
`grafico_10.html`. El HTML principal los carga mediante rutas relativas, por
lo que no se deben renombrar ni mover fuera de `graficos/`.

## Estructura necesaria para publicar

```text
articulo_brecha_educativa.html
portada_brecha_educativa.png
graficos/
  grafico_01.html
  grafico_02.html
  grafico_03.html
  grafico_04.html
  grafico_05.html
  grafico_06.html
  grafico_07.html
  grafico_08.html
  grafico_09.html
  grafico_10.html
```

## Publicar con GitHub Pages

Desde la carpeta del proyecto:

```powershell
git add .
git commit -m "Actualizar artículo y gráficos"
git push origin main
```

Después, en GitHub:

1. Abre **Settings → Pages**.
2. En **Build and deployment**, selecciona **Deploy from a branch**.
3. Selecciona la rama `main` y la carpeta `/ (root)`.
4. Guarda los cambios y espera unos minutos.

El artículo se puede abrir en:

```text
https://angieb26.github.io/brecha_educativa/articulo_brecha_educativa.html
```

Los gráficos deben conservar la misma dirección relativa, por ejemplo:

```text
https://angieb26.github.io/brecha_educativa/graficos/grafico_01.html
```

## Comprobarlo localmente

No se recomienda abrir el HTML haciendo doble clic, porque algunos navegadores
restringen los `iframe` y las rutas locales. Para probarlo con un servidor
local, ejecuta:

```powershell
python -m http.server 8000
```

Luego abre <http://localhost:8000/articulo_brecha_educativa.html>.

Si aparece un `404` en los gráficos publicados, comprueba que la URL incluya
`/brecha_educativa/`, que exista la carpeta `graficos/` en GitHub y recarga con
`Ctrl + F5`.

## Fuente y precauciones

- Fuente principal: INEI, Encuesta Nacional de Hogares (ENAHO), módulo 300 de
  Educación.
- Periodo: 2004–2025.
- Las cifras usan el factor de expansión de la encuesta.
- 2020 corresponde a una encuesta telefónica durante la pandemia y debe
  interpretarse con cautela.
- El análisis muestra asociaciones y diferencias poblacionales; no demuestra
  relaciones causales.
