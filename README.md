# Actividad-1-Mapeo-

## Sistema de referencia inercial
Es el marco de referencia fijo y absoluto. Este se define mediante las coordenadas [x,y,θ], donde x y y representan la posición en el plano y θ la orientación del robot respecto a este eje fijo.

## Sistema de referencia local
Es el marco de referencia que se mueve y rota junto con el robot. Sus ejes están alineados con la estructura del robot, por lo tanto, la posición de un punto de vista desde este sistea depende de hacia dónde esté apuntando el robot en ese momento. 

## Código
- Se construye la matriz de rotación en z que representa el ángulo θ. Esta matriz permite girar los vectores de un sistema a otro.
- Para la transformación global a local, se toma un vector de posición inercial y lo multiplica por la matriz de rotación para obtener la posición en el marco local del robot.
- Para verificar que el cálculo es correcto, se invierte la matriz de rotación y multiplica el vector local para regresar a las coordenadas inerciales.
- Se repite este proceso para varias entradas de x, y y θ. 
