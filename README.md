# redis2

intalar 
sudo apt install lsb-release curl gpg

curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg


 echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

 sudo apt-get update

 sudo apt-get install redis

 sudo apt install redis-server

 redis-server

 Correr el server en 2do plano 

 redis-server &

 comprobar si esta corriendo el servidos 
 ps -ef | grep redis

 Entrar a la linea de comando de redis 

 redis-cli

 Definir valores 

 set "nombre de varible" "valor"

 ver valores 
  get "nombre de varibale"

  dar varios valores a la ves 

  mset "nombre de varible" "valor" "nombre de varible" "valor"

Para optener valios valores a la vez 

mget nombre apellido apelido2


para obter la longitd de la variable(string)

strlen "nombre"

Para invrementar  uno a un entero 

incr "nombre del valor"

Para incrementar con un numero espesifico 
incrby "nombre del valor" "numero de incremento"

Para hacer un decremento 
decr numero
decrby numero 4

para definir un valor flotante 

set "nombre" "valo
incrbyfloat pi 0.2

para darle un tiempo de expiracion a un valor 
expire "variable" "numero"
ttl "variable"  (ver cuanto tiempo le queda)

para definir una variable con tiempo 

setex "hola" "tiempo" "adios" 

para ver todo variable definidas en la memoria 

keys *

para borrar las variables 

flushall


para dar valores a una lista 
lpush "estados" "hidalgo"
 para ecrlos 
 lrange estados 0 -1 (del 0 al ultimo -1)


 para poner uno abajo del ultimo valor

  rpush estados jalisco


  para borrar el ultimo de la lista 

  lpop estados

  para borrar el primero 

  rpop estados

---para poner nates de un valor---  
linsert estados before mexico "Lima peru"
linsert estados after  sonora "Huasca"


--solo para insertar a una lista que ya existe 

lpushx 


Para ordernar de forma acendente 

sort estados ALPHA
sort estados desc  ALPHA