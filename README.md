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

Solución del profe:

public class Cafetera implements Comparable <Cafetera>{

	private int capacidadMáxima;
	private int capacidadActual;
	
	Cafetera( int capacidadMáxima, int cantidad){
		this.capacidadMáxima = capacidadMáxima;
		this.capacidadActual = (capacidadMáxima > cantidad)? cantidad: capacidadMáxima;
	}
	
	Cafetera (){
		this(1000,0);
	}
	
	Cafetera( int valor){
		this(valor,0);
	}
	
	
	public int getCapacidadMáxima() {
		return capacidadMáxima;
	}

	public int getCapacidadActual() {
		return capacidadActual;
	}

	public void llenarCafetera(){
		capacidadActual = capacidadMáxima;
	}
	
	public void vaciarCafetera(){
		capacidadActual = 0;
	}
	
	public void servirTaza ( int vtaza){
		capacidadActual -= vtaza;
		if ( capacidadActual <0) capacidadActual = 0;
	}
	
	public void agregarCafe ( int vcafe){
		capacidadActual += vcafe;
		if ( capacidadActual > capacidadMáxima) capacidadActual = capacidadMáxima;
	}

    // Método para ordenar cafeteras por capacidad Actual
	public int compareTo(Cafetera o) {	
		return this.capacidadActual - o.capacidadActual;
	}
	
