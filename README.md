# Docker

La prima volta dopo aver scaricato l'immagine
Entrare dentro la directory scaricata e lanciare i seguenti comandi da terminale:

'''
git submodule init
git submodule update
'''
```
docker compose up
```
Per forzare la build senza cache (nel caso si vogliano apportare modifiche al container)
```
docker compose build --no-cache
```


Per visualizzare tutti i container istanziati in ogni stato (attivo/sospeso)
```
docker ps -a
```
Per aprire una shell verso il container già in stato di run:
attach (al servizio in esecuzione sul container, interfaccia in/out al servizio) vs bash (apro bash sul container) -> attach vs console su Portainer 
noto il nome del container (in questo caso il nome è sempre "ros_app"), comando
```
docker exec -it ros_app bash
``'

# ROS

Entrati nel container fare la build del workspace
'''
colcon build
source install/setup.bash
'''

Per lanciare la simulazione gazebo

'''
export TURTLEBOT3_MODEL=burger
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
'''

