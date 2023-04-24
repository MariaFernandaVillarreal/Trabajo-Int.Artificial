# ProyectoAIcoffe
## Miembros
- Miguel López Vélez cc 1001014378 Bioingeniería
- Maria Fernanda Villareal Teherán cc 1233345251 Bioingeniería
## Resumen
Se intentara predecir la calidad de café arábigo según sus características (altura, origen, variedad, método de proceso etc) y procedencia. A traves de la base de datos obtenida de URL: https://www.kaggle.com/datasets/volpatto/coffee-quality-database-from-cqi?select=arabica_data_cleaned.csv, dicha calidad se mide en aroma, textura,acidez, dulzura etc, para ello se usaran dichas columnas con valores de 1-10. Además de las columnas de origen y altura para tener una mejor estimación, inicialmente se piensa trabajar con los 1312 datos, pero esto se podrá reducir dependiendo de la capacidad computacional para procesarlos. En este caso el modelo se evaluara con varias pruebas, las que incluyen MAE, MSE, y R2 score. Finalmente se enfoca en nuevos caficultores que desean saber que impacto tendrá su café, si las ventas de café no aumentan a base de 10% con las predicciones para la adquisición de nuevos cafés el proyecto no vale la pena. 

## Instrucciones
Al ser un dataset de Kagel este necesitara una autentificación, mediante un token que puede ser descargado desde el propio Kagel siguiendo el siguiente tutorial: https://www.kaggle.com/docs/api, específicamente en la parte de "Authentication". Después de esto se corre la parte de código:
``` python
from google.colab import files

files.upload()
```
Donde se debe subir dicho token. Cabe resaltar que este proceso solo es necesario para el notebook "01_Exploracion_data".

## Videos 
- [Entrega 2](https://youtu.be/QIGSypTM7jk)

##
```
                              ░░              ░░              ░░                                
                              ░░              ░░              ░░                                
                                ░░              ░░              ░░                              
                                ░░              ░░              ░░                              
                              ░░              ░░              ░░                                
                              ░░              ░░              ░░                                
                            ░░              ░░              ░░                                  
                            ░░              ░░              ░░                                  
                              ░░              ░░              ░░                                
                              ░░              ░░              ░░                                
                                ░░              ░░              ░░                              
                                ░░              ░░              ░░                              
                              ░░              ░░              ░░                                
                              ░░              ░░              ░░                                
                                                                                                
                                    ▓▓██████████████████████                                    
                            ████████                        ████████                            
                        ████        ████████████████████████        ████                        
                      ██░░    ██████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒██▓▓██  ░░░░██                      
                    ██    ████▒▒▓▓▓▓▓▓▓▓░░░░░░▓▓▓▓░░░░░░▓▓▓▓▒▒▓▓▓▓████    ██                    
                  ██    ██▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓░░░░▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▒▒▓▓██    ██                  
                  ██  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▒▒▓▓▓▓  ██  ██▓▓▓▓▓▓██      
                  ██  ██▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒██  ████          ██    
                  ██    ██▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓██    ██              ██  
                    ██  ░░████▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓████░░  ██░░    ████      ██  
                    ██        ██████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓██████        ██  ████    ██    ██  
                    ██              ████████████████████████              ████        ██    ██  
                    ██                ░░  ░░░░░░░░░░░░░░░░░░              ██          ██    ██  
                ██████                                                    ██████    ██      ██  
            ████    ██                                                    ██    ██  ██    ██    
        ░░██▒▒░░    ▒▒▓▓                                                ▓▓▒▒    ░░██▒▒    ██    
      ▓▓  ░░          ██                                                ██  ██████      ▓▓      
    ██                ██                                                ████        ████  ██    
  ██                  ░░██                                            ██░░░░    ████░░░░  ░░██  
  ██                ██████                                            ██████████░░░░        ██  
██                ██▒▒░░▒▒██                                        ██▒▒▒▒██                  ██
██              ██▒▒██▒▒▒▒██                                        ██▒▒▒▒▒▒██                ██
██              ██░░▓▓████▒▒▓▓                                    ▓▓▒▒██░░▒▒██                ██
  ██            ██▒▒██▓▓░░▒▒▒▒██                                ██▒▒░░▒▒████                ██  
  ██              ██░░██▒▒████▒▒████                        ████▒▒██▒▒██▒▒██                ██  
    ██            ██▒▒▒▒██▓▓░░▒▒░░▒▒██▓▓▓▓            ▓▓▓▓██▒▒██▒▒░░██▒▒░░██              ██    
      ██            ██████▒▒▒▒▒▒██████▒▒▒▒████████████▒▒██▒▒▒▒▓▓██▒▒▒▒████░░            ██      
        ██                ██████░░▒▒██░░▒▒██▒▒▒▒░░▒▒██▒▒▒▒██░░▒▒▒▒████                ██        
          ████                ██▒▒▒▒▓▓▒▒▒▒██░░▒▒████▒▒░░▒▒▒▒██████                ████          
          ░░  ████              ████  ████░░████░░░░████████    ░░            ████              
                  ████                                                    ████                  
                      ██▓▓▓▓██                                    ▓▓▓▓▓▓██                      
                              ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                              

```
