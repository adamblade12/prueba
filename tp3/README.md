ejecucion1: sinhilos:5.17938 segundos
	    conhilos:4.00972 segundos
ejecucion2:sinhilos:5.15340 segundos
	   conhilos:4.02542 segundos
ejecucion3:sinhilos:5.13686 segundos
	   conhilos:4.15249 segundos
ejecucion4:sinhilos:5.15417 segundos
	   conhilos:4.02192 segundos
ejecucuion5:sinhilos:5.15174 segundos
	    conhilos:4.01702 segundos

1)
  a- Lo que se nota con respecto al tiempo de ejecucion, es que con hilos tarda menos que sin hilos
    se nota que el tiempo de ejecucion es que con hilos no pasa de 5 segundos y sin hilos es mas de 5 segundos
  b- Los tiempos de ejecucion no son iguales

Ejecucion de suma_resta.py
  Sin lineas 11,12,19 y 20:
	Tiempo de ejecucion: al rededor de 0.02200 segundos
	Resultado final:0
	Los hilos se ejecutan simultaneamente, acceden al recurso compartido pero nunguno lo llega a actualizar.
	No tiene retraso por la ausencia del bucle for con pass que simula tiempo de trabajo para la maquina
  Con lineas 11,12,19 y 20:
	La zona critica del programa seria cuando los hilos quieren leer y modificar un recurso compartido, en este caso, la variable acumulador.
	Ambos hilos tienen acceso al acumulador al mismo tiempo lo que causa retrasos porque si un hilo intenta acceder al acumulador y el otro lo esta usando, este tendra que esperar a que el otro termine para recien acceder al acumulador.Esto causa que el tiempo de ejecucion crezca.
	Si los hilos acceden al acumulador (zona critica) sin un orden, el resultado final de acumulador depende del orden en que se ejecutan los hilos, o sea es impredecible, esto seria una "race condition"
