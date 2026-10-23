Promt juego : Hazme un juego, de tic tac toe el cual cotenga un algoritmo de decision basado en las acciones tomadas por el jugador y eligiendo, la mejor ruta para ganar la partida contando, con un minuto en total. Que sea en total 3 rondas consecutivas, en caso de empate una partida final de decision para saber si gana, pierde o empata uno de los rivales. Que la jugabilidad sea multijugador. 
Que las estetica, sea simple pero no plana, que la cruz sea roja y el circulo verde, que tenga 3 filas y 3 columnas de 3 cuadrados. Que arriba tenga un teporizador marcando el tiempo (recorda que es un minuto), abajo del temporizador que muestre los puntos de cada uno (debe ser un punto por partida). 
Esto generalo en Index.html. Los colores en css y la interacion con javascript

• ¿De qué trata? : Trata de ta te ti
• ¿Qué hace el jugador?: Jugas contra tu amigo o una ia 
• ¿Cómo se gana? : conectando 3 x o O
• ¿Cómo se pierde? : Se pierde no conectando las 3 X o O
• ¿Cuántas vidas o cuánto tiempo?: Tenes 1 minuto y 3 rondas, en caso de empatar ronda definitiva 

Arbol de decision:
¨¨¨¨
[Inicio de Aplicación]
│
├── [Selección de Modo]
│   ├── Multijugador (Local 2 Jugadores)
│   └── vs IA (Jugador vs Computadora)
│
├── [Inicio de Ronda (1, 2 o 3)]
│   └── [Temporizador Global: 60 Segundos Activo]
│       ├── ¿Tiempo Agotado? (0s) ──> Fin de ronda actual por tiempo
│       └── ¿Movimiento Válido? ──> Marcar Casilla (Rojo: X / Verde: O)
│
├── [Evaluación de Estado de Tablero]
│   ├── ¿Hay Tres en Raya? ──> Asignar +1 Punto al ganador ──> Fin de Ronda
│   ├── ¿Tablero Lleno? ──────> Empate (Sin puntos) ──────────> Fin de Ronda
│   └── ¿Juego en Curso? ────> Cambiar Turno
│
└── [Gestión de Rondas (Post-Ronda 3)]
    ├── ¿Ronda < 3? ──> Incrementar contador de ronda y reiniciar tablero
    └── ¿Ronda == 3 (Completadas)?
        ├── ¿Hay un ganador con más puntos? ──> ¡Fin del Juego / Mostrar Campeón!
        └── ¿Empate en puntos? ──────────────> ¡Activar Ronda de Desempate Final!
¨¨¨¨
