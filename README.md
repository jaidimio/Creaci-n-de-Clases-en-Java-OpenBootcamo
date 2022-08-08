# Creaci-n-de-Clases-en-Java-OpenBootcamo
Creación de clases y variables en Java. Ejercicio Tema 9 de Introducción a la Programación en OpenBootcamp.
//Crear una clase persona con las siguientes variables: La edad, el nombre, el teléfono.
// Una vez creada la clase, crear una nueva clase cliente que herede de persona, esta nueva clase tendrá la variable crédito solo para esa clase.
// Crea ahora un objeto de la clase cliente que debe tener como propiedades la edad, el teléfono, el nombre y el crédito, tienes que darles
// valor y mostrarlos en pantalla.
// Una vez hecho esto, haz lo mismo con la clase trabajador que herede de persona, y con una variable salario que solo tenga la clase trabajador.

public class Main {
    public static void main(String[] args) {
// creando el objeto
        Cliente cliente1 = new Cliente();
        cliente1.setNombre("Carlos Perez");
        cliente1.setEdad(38);
        cliente1.setTelefono(6034820);
        cliente1.setCredito(2200);

        // Imprimiendo datos en pantalla
        System.out.println("Su nombre es: " + cliente1.getNombre());
        System.out.println("La edad es " + cliente1.getEdad() + " años");
        System.out.println("Su Telefono es: " + cliente1.getTelefono());
        System.out.println("El monto del credito es: " + cliente1.getCredito());

        // Creación del trabajador con los datos
        Trabajador trabajador1 = new Trabajador();
        trabajador1.setNombre("Marcos Marin");
        trabajador1.setEdad(33);
        trabajador1.setTelefono(3286576);
        trabajador1.setSalario(3200);

        // Imprimir datos
        System.out.println("\nEl nombre del trabajador es: " + trabajador1.getNombre());
        System.out.println("Tiene " + trabajador1.getEdad() + " años");
        System.out.println("El numero de Telefono es: " + trabajador1.getTelefono());
        System.out.println("El salario del trabajador es: " + trabajador1.getSalario());
    }
}
// creación de la clase con sus variables
class Persona {
    private int edad, telefono;
    private String nombre;

   public void setEdad(int edad) {
        this.edad = edad;
    }

    public void setTelefono(int telefono) {
        this.telefono = telefono;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public int getEdad() {
        return this.edad;
    }

    public int getTelefono() {
        return this.telefono;
    }

    public String getNombre() {
        return this.nombre;
    }
}

class Cliente extends Persona {
    private int credito;

    public void setCredito(int credito) {
        this.credito = credito;
    }

    public int getCredito() {
        return this.credito;
    }
}

class Trabajador extends Persona {
    private int salario;

    public void setSalario(int salario) {
        this.salario = salario;
    }

    public int getSalario() {
        return this.salario;
    }
}
