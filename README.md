# PROYECTO 1 PRIMER CORTE
## Elaborado por: Laura Rodriguez y Diana Bernal

### Interactuando con Pepper
Para realizar una presentación con Pepper. Se aplicaron conceptos del Laboratorio II. En el cual, se explicó como fue el proceso de conexión por medio de la terminal de Ubuntu. En este caso, Pepper tenía un número de IP distinto el cuál era: </br>
+ 192.168.0.106</br>
Eso fue necesario tenerlo en cuenta a la hora de realizar la conexión por medio del terminal y a su vez, para establecer la conexión en el código de Python. De tal forma que, aplicando los conceptos del Laborario II el código resultante fue el siguiente:</br>

		import qi
		import argparse
	import sys
	import almath
	import math
	import motion
	import time
	import webbrowser
	import os

	session = qi.Session()
	session.connect("tcp://192.168.0.106:9559")
	animated_speech_service = session.service("ALAnimatedSpeech")
	motion_service = session.service("ALMotion")
	tablet_service=session.service("ALTabletService")

a = 1
while a == 1:

	tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen3.jpg")
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(1)
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-1.0, 1.0], 0.5)
        time.sleep(2)
	      motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-0.3, 0.3], 0.5)
        time.sleep(1)
	      animated_speech_service.say("Bienvenidos a una nueva sesión informativa ")
	      time.sleep(2)

        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(1)
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-1.0, 1.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-0.3, 0.3], 0.5)
        time.sleep(1)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen1Proyecto.jpg")
        time.sleep(2)
        animated_speech_service.say("El día de hoy les estaré presentando el proyecto realizado por Laura Rodríguez y Diana Bernal")
        time.sleep(2)
	
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(1)
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-1.0, 1.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-0.3, 0.3], 0.5)
        time.sleep(1)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen2Proyecto.jpg")
        time.sleep(2)
        animated_speech_service.say("Vamos a empezar con los Rockets reutilizables")
        time.sleep(2)
	
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(1)
        motion_service.setAngles(["LShoulderPitch","RShoulderPitch"], [0.0, 0.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-1.0, 1.0], 0.5)
        time.sleep(2)
        motion_service.setAngles(["LElbowRoll","RElbowRoll"], [-0.3, 0.3], 0.5)
        time.sleep(1)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen3Proyecto.png")
        time.sleep(2)
        animated_speech_service.say("Son una tecnología de punta en la industria aeroespacial")
        time.sleep(2)
        animated_speech_service.say("Están diseñados para recuperar y reutilizar sus partes mas costosas")
        time.sleep(2)
        animated_speech_service.say("Actualmente, se están desarrollando rockets reutilizables que emplean combustibles derivados de biomasa y propulsión eléctrica")
        time.sleep(2)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen3.jpg")
        time.sleep(2)
        animated_speech_service.say("Que tal si vemos un video que muestre acerca de esta tecnología")
        time.sleep(2)
	      tablet_service.enableWifi()
	      tablet_service.playVideo("http://198.18.0.1/apps/usta/Rockets.mp4")
	      time.sleep(164)

	      tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen4Proyecto.png")
        time.sleep(2)
        animated_speech_service.say("Ahora hablemos un poco acerca de Enjambres de drones Autocoordinados")
        time.sleep(2)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen4Proyecto.png")
        time.sleep(2)

        animated_speech_service.say("A esta se le conoce como el comportamiento colectivo observado en sistemas descentralizados y autoorganizados")
        time.sleep(2)
	      animated_speech_service.say("Sabías que muchas son las empresas que estudian el vuelo de enjambres de drones en la actualidad")
	      time.sleep(2)
	      animated_speech_service.say("Para puntualizar, la idea central de la inteligencia de enjambre es que la inteligencia colectiva puede surgir de una población de agentes simples")
	      time.sleep(2)
	      tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen3.jpg")
	      time.sleep(2)
        animated_speech_service.say("Una aplicación interesante es la Coordinación de enjambres de drones autónomos")
	      time.sleep(2)
	      animated_speech_service.say("Vamos a verlo")
        time.sleep(2)
	      tablet_service.enableWifi()
	      tablet_service.playVideo("http://198.18.0.1/apps/usta/Drones.mp4")
	      time.sleep(90)
	
	      tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen5Proyecto.png")
        time.sleep(1)
        time.sleep(1)
        tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen5Proyecto.png")
        time.sleep(1)

        animated_speech_service.say("Esta hace referencia a los algoritmos criptográficos diseñados para protegerse contra un ataque de un ordenador cuántico potente.")
        time.sleep(2)
        animated_speech_service.say("A su vez, la encriptación puede proteger los datos digitales tanto en tránsito como en reposo.")
        time.sleep(2)
        animated_speech_service.say("Esta ho ha sido todo por esta sesión.")
        time.sleep(2)
        animated_speech_service.say("Espero que haya sido de su agrado la presentación.")
        time.sleep(2)
	      animated_speech_service.say("Nos vemos en una próxima.")
        time.sleep(2)

	      tablet_service.showImage("http://198.18.0.1/apps/usta/Imagen3.jpg")
	      time.sleep(2) 
	      a=0





