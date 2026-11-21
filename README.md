# brecha_educativa
# brecha_educativa

## Desplegar el artículo con sus gráficos

El artículo carga los diez gráficos interactivos desde `graficos/grafico_01.html`
hasta `graficos/grafico_10.html`. Por eso, la carpeta `graficos` debe quedar en
el mismo nivel que `articulo_brecha_educativa.html`.

1. Ejecuta todas las celdas de `brecha_educativa_exportar_graficos.ipynb` en
   Google Colab.
2. Descarga la carpeta `/content/graficos/` que se genera al final.
3. Coloca esa carpeta junto a `articulo_brecha_educativa.html` antes de subir
   los archivos al servicio de despliegue.

La estructura mínima publicada debe ser:

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

No abras el HTML desde una vista previa que bloquee `iframe`; comprueba el
resultado mediante el servidor o servicio donde lo vas a publicar.