**Clase Rotor:**

1. *__init__(self, wiring, notch, position=0):* Constructor que inicializa el mapeo interno, la posición de la muesca y la posición inicial del rotor.
2. *rotate(self):* Método que rota el rotor y devuelve True si el rotor alcanza la muesca, lo que indica que el siguiente rotor debe girar.
3. *encrypt_forward(self, char):* Método que cifra una letra al pasar por el rotor en la dirección hacia adelante.
4. *encrypt_backward(self, char):* Método que cifra una letra al pasar por el rotor en la dirección hacia atrás.

**Clase Reflector:**

1. *__init__(self, wiring):* Constructor que inicializa el mapeo del reflector.
2. *reflect(self, char):* Método que refleja una letra.

**Función encrypt_message:**

1. Cifra un mensaje utilizando los rotores, el reflector y el panel de conexiones.
2. El mensaje pasa por el panel de conexiones antes de los rotores, luego por los rotores hacia adelante, se refleja, y luego pasa por los rotores en dirección inversa antes de pasar nuevamente por el panel de conexiones.

**Función configurar_y_cifrar_mensaje:**

1. Solicita al usuario la cantidad de rotores (entre 3 y 5).
2. Configura cada rotor basado en el número ingresado por el usuario.
Configura el reflector.
3. Configura el panel de conexiones, permitiendo reemplazar conexiones existentes si el usuario así lo decide.
4. Solicita al usuario el mensaje a cifrar y lo cifra utilizando los rotores, el reflector y el panel de conexiones.