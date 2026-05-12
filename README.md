# Explicación técnica del proceso modelado

1.Nodo inicial: El proceso arranca cuando el usuario pulsa Finalizar pedido
2.Se ejecuta la acción
3.Fork node: El sistema lanza en paralelo Stock y Validación de la sesión
4.Ambas validaciones se ejecutan simultaneamente e independientemente
5.Join node: El flujo espera a que ambas varificaciones terminen
6.Decision node: Si falla termina, si no sigue
7.Accion: Pasarela de pago
8.Decision node: si falla se cierra, si no sigue
9.Fork node lanza 3 tareas post-pago
10.Se realizan las 3 acciones
11.Join node: Espera a que todas las acciones terminen
12.Acción: Se notifica que todo esta correcto
13.Nodo final: Acaba el proceso
