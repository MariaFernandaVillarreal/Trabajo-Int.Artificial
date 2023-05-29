# H&M prediction
## Miembros
- Miguel López Vélez cc 1001014378 Bioingeniería
- Maria Fernanda Villareal Teherán cc 1233345251 Bioingeniería

## Resumen
H&M es un grupo con 53 mercados en línea, los cuales al ofrecer una amplia selección de productos es posible que los clientes no encuentran rápidamente lo que buscan y finalmente se decidan por no realizar la compra o tomar una decisión incorrecta la cual lleve a devoluciones, es por eso por lo que se quiere desarrollar recomendaciones de productos basadas en datos de transacciones anteriores, así como en metadatos de cliente y productos. Estos metadatos abarcan desde datos simples como el tipo de prenda y la edad del cliente hasta datos de texto de descripciones de productos y datos de imágenes de prendas. 
Se intentará predecir qué artículos recomprará cada cliente en el período aleatorio con respecto a los datos totales. Los clientes que no hayan realizado ninguna compra durante ese tiempo quedan excluidos de la puntuación. Para esto se utilizan datos obtenidos de: https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data los cuales tienen información de clientes, artículos, imágenes de artículos (estos no se utilizan para simplificar el problema), transacciones, entre otros, teniendo en cuenta que de ser necesario se reducirá la cantidad de datos. 
En este caso el modelo se evaluará con varias métricas, principalmente usando RMSE pero incluyendo MAE, MSE, neg R2 score y los ratios de MAE y RMSE. Finalmente, si las recomendaciones no aumentan las ventas en un 10% con las predicciones, el modelo no vale la pena.  

## Instrucciones
Al ser un dataset de Kagel este necesitara una autentificación, mediante un token que puede ser descargado desde el propio Kagel siguiendo el siguiente tutorial: https://www.kaggle.com/docs/api, específicamente en la parte de "Authentication". Después de esto se corre la parte de código:

``` python
from google.colab import files

files.upload()
```
Esto solo aplica para los notebooks 0.1 y 0.2, en el 0.3 se tiene la opción de descargar el dataset desde google drive o directamente del github.
## Videos 
- [Entrega 2](https://youtu.be/QIGSypTM7jk) (Este video es de la entrega anterior y como se tuvo que cambiar el dataset no se vuelve a hacer)
- [Entrega Final](https://youtu.be/JUZFiu5h6j4)
##
```
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
⣿⣿⣿⣿⠟⠉⠉⠀⠉⠉⠉⠉⠉⠁⠈⠉⠙⢿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
⣿⣿⣿⡟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⢿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
⣿⣿⡿⠀⠀⣤⡄⠀⠀⠀⠀⠀⠀⠀⠀⣤⡀⠀⠸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
⣿⣿⣥⡀⣼⣿⠇⠀⠀⠀⠀⠀⠀⠀⠀⣿⣷⡀⣠⣽⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿
⣿⣿⣿⣿⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀⠀⣿⠿⠿⠿⠿⠿⠿⠿⠿⠿⠿⣿⣿⣿⣿
⣿⣿⣿⣿⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀⢸⡟⠛⠛⠛⠛⠛⠛⠛⠛⠛⠛⢿⣿⣿⣿
⣿⣿⣿⣿⣿⡏⠀⠀⠀⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⢀⡀⠀⠀⠀⠀⢸⣿⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠇⠀⠀⠀⠀⣿⣷⠀⠀⠀⠀⢸⣿⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⠀⠀⠀⢰⣿⣿⡆⠀⠀⠀⠀⣿⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠀⠀⠀⠀⣼⣿⣿⣷⠀⠀⠀⠀⣿⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡇⠀⠀⠀⢠⣿⣿⣿⣿⡄⠀⠀⠀⢹⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡇⠀⠀⠀⢸⣿⣿⣿⣿⣧⠀⠀⠀⢸⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⠁⠀⠀⠀⣾⣿⣿⣿⣿⣿⡀⠀⠀⠘⣿⣿
⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿

```