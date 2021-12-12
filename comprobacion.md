# Comprobaciones
 
1.- Creación de un pod:

``` ruby
k0s kubectl run pod-nginx-victor --image=nginx
```
 ![pod](https://github.com/victorsanmar/k0s/blob/main/imagenes/pod1.PNG)
 
2.- Comprobamos que al lanzar el pod no da error y accedemos dentro del pod de forma interactiva
  ``` ruby
  k0s kubectl exec pod/pod-nginx-victor -it -- /bin/bash
  ```
![pod](https://github.com/victorsanmar/k0s/blob/main/imagenes/pod2.PNG)  
3.- Creamos una pasarela: port-forward y comprobamos la web desde otra terminal con el comando curl
   ``` ruby
   k0s kubectl port-forward pod/pod-nginx-victor 8085:80
   curl localhost:8085
   ```
 ![pod](https://github.com/victorsanmar/k0s/blob/main/imagenes/podcomprobacion.PNG)
