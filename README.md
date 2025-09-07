# PROYECTO 1 PRIMER CORTE
## Elaborado por: Laura Rodriguez y Diana Bernal

### 1. Interactuando con Pepper
Para realizar una presentación con Pepper. Se aplicaron conceptos del Laboratorio II. En el cual, se explicó como fue el proceso de conexión por medio de la terminal de Ubuntu. En este caso, Pepper tenía un número de IP distinto el cuál era: </br>
+ 192.168.0.106

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
        		animated_speech_service.say("El día de hoy les estaré presentando el proyecto realizado por Laura Rodríguez y Diana 					Bernal")
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
        		animated_speech_service.say("Actualmente, se están desarrollando rockets reutilizables que emplean combustibles derivados 				de biomasa y propulsión eléctrica")
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

        		animated_speech_service.say("A esta se le conoce como el comportamiento colectivo observado en sistemas descentralizados 				y autoorganizados")
        		time.sleep(2)
	      		animated_speech_service.say("Sabías que muchas son las empresas que estudian el vuelo de enjambres de drones en la 						actualidad")
	      		time.sleep(2)
	      		animated_speech_service.say("Para puntualizar, la idea central de la inteligencia de enjambre es que la inteligencia 					colectiva puede surgir de una población de agentes simples")
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

       			animated_speech_service.say("Esta hace referencia a los algoritmos criptográficos diseñados para protegerse contra un 					ataque de un ordenador cuántico potente.")
        		time.sleep(2)
        		animated_speech_service.say("A su vez, la encriptación puede proteger los datos digitales tanto en tránsito como en 					reposo.")
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
De tal forma que, el video resultante se puede visualizar mediante los siguientes links de Youtube:

+ Parte I: https://youtu.be/gxtcSoR2fdE?si=3BizRtFQ6ibYWJhN
+ Parte II: https://www.youtube.com/shorts/0MyrbHWdv9I

### 2. Desarrollando Chatbot Personalizado
Para la realización de este iteral fue necesario tener en cuenta la instalación de las siguientes librerías en el terminal de Python:</br>
+ pip install chatterbot
+ pip install chatterbot_corpus
  
Ya realizado el paso anterior, es necesario importarlas para ello se realizó lo siguiente:</br>

<img width="355" height="40" alt="image" src="https://github.com/user-attachments/assets/57c0bcc9-5e80-405c-a73e-66ae6dfe18ff" /></br>

<strong>Figura 1.</strong> Importación de las Librerías en Python.

De tal forma que, el código resultante para la realización del Chatbot para las tres novedades tecnológicas fue el siguiente:</br>

		from chatterbot import ChatBot
		from chatterbot.trainers import ListTrainer

		bot=ChatBot('Hulk')
		name=input("Ingresa tu nombre: ")
		print("¡Bienvenido a Hulk Server!🏃‍♀️ ¿Cómo puedo ayudarte?")
		while True:
    		request=input(name+':')
    		if request=='Chao' or request =='chao'or request ==' Chao':
       			print('Hulk 🏃‍♀️ : Chao')
        		break
    		else:
        		response=bot.get_response(request)
        		print('Hulk 🏃‍♀️ : Claro')
    		if request=='¿Podrías brindarme información acerca de los Sistemas Digitales en Cohetes Reutilizables?' or request =='Podrías 			brindarme información acerca de los Sistemas Digitales en Cohetes Reutilizables'or request=='podrías brindarme información 				acerca de los Sistemas Digitales en Cohetes Reutilizables' :
       			print('Hulk 🏃‍♀️ : Los Sistemas Digitales son fundamentales para la operación y control de los cohetes reutilizables de 					nueva generación, permitiendo la autonomía, navegación, gestión de combustible y aterrizaje seguro de las naves en 						misiones espaciales frecuentes y sostenibles.')
        		print('Hulk 🏃‍♀️ : Estos Sistemas Digitales avanzados son la base para la reutilización y el reciclaje de componentes, lo 				que reduce costos, genera menos desechos espaciales y posibilita el acceso a nuevas misiones y exploraciones 							interplanetarias.')
        		print('Hulk 🏃‍♀️ : Espero te haya sido de utilidad 😊 ')
        		break
    		else:
        		response=bot.get_response(request)
        		print('Hulk 🏃‍♀️ : Dame unos segundos')    
    		if request=='¿Me podrías decir el papel de la IA en el vuelo de enjambres?' or request =='Me podrías decir el papel de la IA 			en el vuelo de enjambres'or request =='me podrías decir el papel de la IA en el vuelo de enjambres' :
       			print('Hulk 🏃‍♀️ : La inteligencia artificial es la columna vertebral de un enjambre de drones. Esta tecnología permite 					que los drones tomen decisiones autónomas, analicen su entorno y se ajusten a las condiciones cambiantes, lo que 						garantiza una actuación coordinada y precisa en todo momento.')
        		print('Hulk 🏃‍♀️ : Espero te haya sido de utilidad 😊 ')
        		break
    		else:
        		response=bot.get_response(request)
       			 print('Hulk 🏃‍♀️ : ...')
    		if request=='¿Me podrías decir algunas ventajas de la Criptografía Post-Cuántica (PQC)?' or request =='Me podrías decir 				algunas ventajas de la Criptografía Post-Cuántica (PQC)'or request =='me podrías decir algunas ventajas de la Criptografía 				Post-Cuántica (PQC)':
        		print('Hulk 🏃‍♀️ : Protección contra computadoras cuánticas: Los algoritmos PQC se basan en problemas matemáticos 						diferentes y más difíciles de resolver para las computadoras cuánticas, asegurando que los datos permanezcan seguros 					incluso con el avance de estas tecnologías.')
        		print('Hulk 🏃‍♀️ : Seguridad a largo plazo: A diferencia de los sistemas actuales como RSA y ECC, la PQC está diseñada 					para ser resistente a los ataques cuánticos, lo que garantiza la confidencialidad y autenticidad de la información a lo 				largo del tiempo. ')
       			print('Hulk 🏃‍♀️ : Mayor resistencia a ataques clásicos: Los algoritmos PQC también están diseñados para resistir ataques 				de fuerza bruta y otros tipos de ataques clásicos, ofreciendo una capa de seguridad adicional. ')
        		print('Hulk 🏃‍♀️ : Espero te haya sido de utilidad 😊 ')
        		break
    		else:
        		response=bot.get_response(request)
        		print('Hulk 🏃‍♀️ : No encuentro respuesta a tu pregunta😞')
        		break 
La visualización de como se ven los tres Chatbots para cada novedad tecnológica será mostrada enseguida:

<img width="824" height="183" alt="Chatbot_NT1" src="https://github.com/user-attachments/assets/7bb82b7a-03fa-44a9-b8cd-1b4a462ae4a1" /></br>

<strong>Figura 2.</strong> Aplicación Chatbot Novedad Tecnológica 1.

<img width="820" height="153" alt="Chatbot_NT2" src="https://github.com/user-attachments/assets/9c591f35-3556-417d-967e-858250bb60fb" /></br>

<strong>Figura 3.</strong> Aplicación Chatbot Novedad Tecnológica 2.







