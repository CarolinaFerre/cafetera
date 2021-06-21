# cafetera
ejercicio de objetos con getter y setter

 Desarrolla una clase Cafetera con atributos capacidadMáxima (la cantidad máxima de café que puede
contener la cafetera) y cantidadActual (la cantidad actual de café que hay en la cafetera). Implementa, al 
menos, los siguientes métodos:
• Constructor común (sin parámetros): establece la capacidad máxima en 1000 (c.c.) y la actual en 
cero (cafetera vacía).
• Constructor de inicialización que sólo recibe la capacidad máxima, poniendo la actual a cero.
• Constructor de inicialización con los dos parámetros: con la capacidad máxima y la cantidad 
actual. Si la cantidad actual es mayor que la capacidad máxima de la cafetera, la ajustará al 
máximo.
• llenarCafetera(): pues eso, hace que la cantidad actual sea igual a la capacidad Máxima.
• servirTaza(int cantidad): simula la acción de servir una taza con la capacidad indicada. Si la 
cantidad actual de café “no alcanza” para llenar la taza, se sirve lo que quede.
• vaciarCafetera(): pone la cantidad de café actual en cero.
• agregarCafe(int cantidad): añade a la cafetera la cantidad de café indicada. Solo se puede llenar 
hasta la capacidad Máxima.
