Nueva-Particion
Los pasos que se realizaron para formatear la Tabla de particiones de la memoria USB son los siguientes: 
-Cuando ya tenemos conectada la memoria abrimos la linea de comandos e ingresamos el comando sudo fdisk -l para poder ver todos los dispositivos conectados en nuestra maquina 
-Vamos a desmontar el dispositivo con el comando umount y  la direcc del dispositivo umount /dev/sdb
-Una vez identificado el dispositivo vamos a tipear el comando sudo fdisk con la direccion del dispositivo en este caso sudo fdisk /dev/sdb para entrar a configurar el dispositivo deseado 
-Aqui ya podemos manipular las tablas de particiones, podemos abrir el menu de opciones con la letra "m" 
-Lo siguiente es eliminar las partiiones con la letra "d", se eliminaran una a una hasta no tener particiones por eliminar
-El siguiente paso es crear la nueva particion, esto se hace con la letra "n", se escoge de que tipo será la particion, extendida o primaria, en este caso es primaria.
-Se van escogiendo los intervalos de memoria que se van a utilizar para la particion
-Despues de configurar el tipo de particion, se escoge el tipo con la letra "t" escogeremos el mas adecuado para nuestro dispositivo en este caso se escogio FAT32, para saber de que tipo de formato existen se puede consultar la lista una vz dentro del tipo con la letra "L".
-Una vez terminado el proceso de borrar, crear y escoger tipo de particion nos salimos y guardamos los cambios con la letra "w"
-Despues se le da un formato al dispositivo como podria ser NTFS con el comando mkfs el tipo de formato y la direcc del dispositivo mkfs.ntfs /dev/sdb
-Una vez terminado el proceso de formato pasamos a montar el dispositivo, esto se hace con el comando mount 
la direccion del dispositivo y la direccion donde se va a montar 
-Para crear la direccion a montar se hace con el comando mkdir y el nombre e la direccion deseada mkdir /media/temp
-mount /dev/sdb1 /media/temp
Y asi es como podemos eliminar, crear, desmontar, montar, y formatear particiones.
