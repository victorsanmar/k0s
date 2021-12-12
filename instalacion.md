# Instalación de k0s en un nodo.
### 1.- Descarga de k0s

``` ruby 
curl -sSLf https://get.k0s.sh | sh
```
![k0s](https://github.com/victorsanmar/k0s/blob/main/imagenes/k0s_instalacion.PNG)

Comprobamos la versión instalada:

``` ruby 
k0s version
```
![k0s](https://github.com/victorsanmar/k0s/blob/main/imagenes/k0s%20version.PNG)
### 2.- Instalamos k0s como servicio.
Con el atributo single de la etiqueta controller especificamos que nuestro nodo va a ser controller y worker

``` ruby 
k0s install controller --single
```

![k0s](https://github.com/victorsanmar/k0s/blob/main/imagenes/k0s%20controller.PNG)

### 3.- Iniciamos k0s y comprobamos que se haya iniciado

``` ruby 
k0s start
k0s status
```
![k0s](https://github.com/victorsanmar/k0s/blob/main/imagenes/k0s%20status.PNG)

### 4.- Usando kubectl que viene incluido en k0s comprobamos la información detallada sobre nuestro nodo

``` ruby
k0s kubectl get nodes -o wide
```
![k0s](https://github.com/victorsanmar/k0s/blob/main/imagenes/k0snodes.PNG)
