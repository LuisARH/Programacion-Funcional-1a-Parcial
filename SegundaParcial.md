![image](https://camo.githubusercontent.com/35e9d7d200795e6ec6bbf764d7f700d8da81cb5bc28ef9787d104a22eb3293a6/68747470733a2f2f696d67732e7365617263682e62726176652e636f6d2f37315a705a5949444b4a46463468797a765a5f4b6133636f2d625875356d5330756f496a637635757679342f72733a6669743a313230303a3638373a312f673a63652f6148523063446f764c336433647935312f593239734c6d31344c324e76626e526c2f626e51765932317a4c7a6b76615731682f5a3255765657526c51305644556c4d342f4d4734756347356e)
# Universidad de Colima
## Facultad de Ingeniería mecánica y Eléctrica
### Ingeniería em Computación Inteligente

---

#### Alumno: Luis Angel Ruiz Hurtado
#### Profesor: Dr. Walter Alexander Mata Lopez

---

## Introducción
#### Aqui se mostraran los codigos de lenguaje Dart, trabajados en clase durante la 2a parcial

---

## Datos numericos y asignacion de operaciones

---

    void main(){
        num a =4;
        a as int; //casting sobre datos numericos
        print(a.isEven); // saber si es impar

        var infInt = 5;
        var infDouble = 9.81;
        print("${infInt.runtimeType}"); //saber el tipo de dato que es
        print("${infDouble.runtimeType}");

        num infNum;
        infNum = 3.6;
        print("${infNum.runtimeType}");
        infNum = 5;
        print("${infNum.runtimeType}");

        print(5.isEven); // saber si es impar
        print(5.isOdd); // saber si es par
    }

---

    void main(List<String> args){
        int a = -3000;
        doble b = 9.89;

        print(a.isNegative); // saber si es negativo

        print(b.floor()); // pone el numero menor
        print(b.ceil()); // pone el numero mayor

        print(b.round()); // redondear

        print(b.truncate()); // quitar decimales

        var c = "HOla";

        print(!b.isNaN); //saber si es un numero
    }

---

    void main(List<String> args) { //division
        print((10/3).truncate());
        print(10~/3);

        print(cos(45 * pi / 180));
        print(sin(45 * pi / 180));
        print(sqrt(9));
        print(pow(2, 3));
        print(max(6, 10));
        print(min(6, 10));
    }

---

    void main(List<String> args){ //incrementos

        var contador = 0;
        contador = contador + 1;
        print(contador);
        contador += 1;
        print(contador);
        contador++;
        print(contador);
        ++contador;
        print(contador);

        var c = 10;
        print(++c);
        c =10;
        print(c++); //primero imprimira la expresion y luego hara la accion
        print(c);
    }

---

      void main(List<String> args){ //decrementos

          var contador = 0;
          contador = contador - 1;
          print(contador);
          contador -= 1;
          print(contador);
          contador--;
          print(contador);
          --contador;
          print(contador);

          var c = 10;
          print(--c);
          c =10;
          print(c--); //primero imprimira la expresion y luego hara la accion
          print(c);
      }

---

    void main(List<String> args){
        int a = 5;
        doble b = 3.5;

        print(a.toDouble());
        print(b.toInt());
        print("El valor es: $a");
        print("El valor es: " + a.toString());
        print(a + b);
        print(a / b);
    }

---

    void main(List<String> args){
        var a = "10";
        var b = "8.5";

        print(int.parse(a) * 2);
        print(double.parse(b) * 2);

        var numero = 3.14159256874588;

        print(numero.toStringAsFixed(3));
    }
 
 ---
 ## Clases
 ---
 
     class User { //1
      String? nombre; //2
      int? edad; //3
    }

    void main(List<String> args) {
      User usuario1 = User(); //4
      print(usuario1); //5
      print(usuario1.nombre); //6
      print(usuario1.edad); //7
    }

1. Creacion de la clase User, las claves van con mayuscula
2. Propiedad nombre de tipo String. Se declaran igual que una variable se llaman propiedad al ir dentro de la clase
3. Propiedad de edad
4. Creacion de instancia usuario1 de la clase User
5. Impresion de la instancia usuario1
6. Impresion de la propoiedad nombre de la instanca usuario1
7. Impresion de la propiedad edad de la instancia usuario1

---

    class User {
      String nombre = "Alex";
      int edad = 50;
    }

    void main(List<String> args) {
      User usuario1 = User();
      print(usuario1.nombre);
      print(usuario1.edad);
    }

---

    class User {
      String nombre = "Alex";
      int edad = 50;
    }

    void main(List<String> args) {
      User usuario1 = User();
      User usuario2 = User();

      print(usuario1.nombre);
      print(usuario1.edad);
      print(usuario2.nombre);
      print(usuario1.edad);
    }

---

    class User {
      String? nombre;
      int? edad;
    }

    void main(List<String> args) {
      User usuario1 = User();
      var usuario2 = User();

      usuario1.nombre = "Alex";
      usuario1.edad = 50;
      usuario2.nombre = "Jimena";
      usuario2.edad = 11;

      print(usuario1.nombre);
      print(usuario1.edad);
      print(usuario2.nombre);
      print(usuario2.edad);
    }

---

    class User {
      String? nombre;
      int? edad;

      void reporte() { //1
        print("Nombre: $nombre"); //2
        print("Edad: $edad años"); //3
      }
    }

    void main(List<String> args) {
      User usuario1 = User();
      usuario1.nombre = "Alex";
      usuario1.edad = 50;

      usuario1.reporte(); //4
    }

1. Metodo reporte, es parecido a una duncion. Al estar dentro de la clase se convierte en metodo
2. Imprime la propiedad nombre
3. Imprime la propiedad edad
4. Se invoca al metodo de la instancia usuario1

---

## Encapsulamiento
- Capacidad de ocultar los atributos de clase
- Hacerlos locales dentro de la clase
- Las propiedades privadas inician con _

---

## Metodos contructores: Getter y Setter
#### Setter: Son metodos que establecen/inicializan los atributos de la clase
#### Getter: Son metodos que retornan los valores de los atributos de la clase

---

    class User {
      String? _nombre;
      int? _edad;

      void set nombre(String nombre) { //1
        _nombre = nombre; //2
      }

      String get nombre{ //3
       _nombre!; //4
      }

      void reporte() {
        print("Nombre: $_nombre");
        print("Edad: $_edad años");
      }
    }

    void main(List<String> args) {
      final usuario1 = User();
      usuario1.nombre = "Alex"; //5
      print(usuario1.nombre); //6
      usuario1.reporte();
    }

1. Metodo Setter
2. Establece el argumento que recibe la propiedad propiedad privada. Solo puede recibir un argumento
3. Metodo Getter
4. Retorna la propiedad privada. Solo puede retornar una propiedad
5. Establece el valor de la propiedad haciendo uso del setter
6. Obtiene el valor de la propiedad haciendo uso del getter

---

    class User {
      String? _nombre;
      int? _edad;

      void set nombre(String nombre) {
        _nombre = nombre;
      }

      String get nombre{
       return _nombre!;
      }

      void set edad(int edad) {
        _edad = edad;
      }

      int get edad{
       return _edad!;
      }

      void reporte() {
        print("Nombre: $_nombre");
        print("Edad: $_edad años");
      }
    }

    void main(List<String> args) {
      final usuario1 = User();
      usuario1.nombre = "Alex";
      usuario1.edad = 50;
      print(usuario1.nombre);
      print(usuario1.edad);
      usuario1.reporte();
    }

---

#### Usando metodos arrow

    class User {
      String? _nombre;
      int? _edad;

      void set nombre(String nombre) => _nombre = nombre;
      void set edad(int edad) => _edad = edad;

      String get nombre => _nombre!;
      int get edad => _edad!;

      void reporte() {
        print("Nombre: $_nombre");
        print("Edad: $_edad años");
      }
    }

    void main(List<String> args) {
      final usuario1 = User();
      usuario1.nombre = "Alex";
      usuario1.edad = 50;
      print(usuario1.nombre);
      print(usuario1.edad);
      usuario1.reporte();
    }

---

## Constructores
- Metodo de la clase que se encarga de inicializar los atributos
- Es el primer metodo que se llama al crear la instancia
- El metodo lleva el nombre de la clase

---

    class User {
      User() { //1
        print("Constructor User");
      }
    }

    void main(List<String> args) {
      final usuario1 = User(); //2
      print(usuario1);
    }

1. Creacion del contructor User dentro de la clase User
2. Creacion de la instancia usuario1 que invoca al constructor User al momento de su creacion

---

#### Equivalencia a los setters y getters 

    class User {
      String? _nombre; //1
      int? _edad;

      User(String nombre, int edad) { //2
        this._nombre = nombre;
        this._edad = edad;
      }

      String? get nombre => _nombre; //3
      int? get edad => _edad;
    }

    void main(List<String> args) {
      final usuario1 = User("Alex", 50); //4
      print(usuario1.nombre);
      print(usuario1.edad);
    }

1. Cracion de las propiedades de la clase User
2. Creacion del contructor User de la clase User
3. Creacion de getters
4. Creacion de la instancia usuario1

---

#### Version corta de constructores {short hand}

    class User {
      String _nombre; //1
      int _edad;

      User(this._nombre, this._edad); //2

      String get nombre => _nombre; //3
      int get edad => _edad;
    }

    void main(List<String> args) {
      final usuario1 = User("Alex", 50); //4
      print(usuario1.nombre);
      print(usuario1.edad);
    }

1. Creacion de las propiedades
2. Creacion del contructor
3. Creacion de los getters
4. Creacion de la instancia User con su contruccion

---


#### Constructores con propiedades nombradas

    class User {
      String? nombre; //1
      int? edad;

      User({this.nombre, this.edad}); //2

      String? get getNombre => nombre; //3
      int? get getEdad => edad;
    }

    void main(List<String> args) {
      final usuario1 = User(nombre: "Alex", edad: 50); //4
      print(usuario1.nombre);
      print(usuario1.edad);
    }

1. Creacion de las propiedades
2. Creacion del contructor
3. Creacion de los getters
4. Creacion de la instancia User con su contruccion

---

#### Varios constructores para una clase


    class User {
      String? nombre;
      int? edad;

      User.nombre(this.nombre); //1
      User.edad(this.edad); //2

      String? get getNombre => nombre;
      int? get getEdad => edad;
    }

    void main(List<String> args) {
      final usuario1 = User.nombre("Alex"); //3
      final usuario2 = User.edad(50); //4

      print(usuario1.getNombre);
      print(usuario1.getEdad);

      print(usuario2.getEdad);
      print(usuario2.getNombre);
    }

1. Constructor para la propieda nombre
2. Constructor para la propiedad edad
3. Creacion de la instancia usuario1 con el constructor nombre
4. Creacion de la instancia usuario2 con el constructor edad

---

    class User {
      String? _nombre;
      int? _edad;

      User.nombre(String nombre) {
        _nombre = nombre;
        _edad = 0;
      }

      User.edad(int edad) {
        _nombre = "-";
        _edad = edad;
      }

      String? get getNombre => _nombre;
      int? get getEdad => _edad;
    }

    void main(List<String> args) {
      final usuario1 = User.nombre("Alex");
      final usuario2 = User.edad(50);

      print(usuario1.getNombre);
      print(usuario1.getEdad);

      print(usuario2.getEdad);
      print(usuario2.getNombre);
    }

---

## Herencia y polimorfismo

### Herencia
- Mecanismo con el que se puede extender la funcionalidad de una clase
- Por ejemplo usuario puede ser:
   - Estudiante
   - Profesor
   - Directivo
   - Etc.

---

    class Estudiante {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    class Profesor {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    class Directivo {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

---

    class User {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    class Estudiante extends User {}

    class Profesor extends User{}

    class Directivo extends User{}

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

--- 

#### Sobreescritura de metodos (Overriding)

    class User {
      String nombre = "";
      int edad = 0;

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    class Estudiante extends User {
      @override
      void mostrarDatos() {
        print("Estudiante: $nombre");
        print("Edad: $edad");
      }
    }

    class Profesor extends User{}

    class Directivo extends User{}

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Hugo";
      estudiante1.edad = 15;
      estudiante1.mostrarDatos();

      final profesor1 = Profesor();
      profesor1.nombre = "Paco";
      profesor1.edad = 25;
      profesor1.mostrarDatos();

      final directivo1 = Directivo();
      directivo1.nombre = "Luis";
      directivo1.edad = 30;
      directivo1.mostrarDatos();
    }

---

#### Uso del constructor super

    class User {
      String nombre = "";
      int edad = 0;
      User(this.nombre, this.edad);

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    class Estudiante extends User {
      Estudiante(String nombre, int edad) : super(nombre, edad);
    }

    class Profesor extends User {
      Profesor(String nombre, int edad) : super(nombre, edad);
    }

    class Directivo extends User {
      Directivo(String nombre, int edad) : super(nombre, edad);
    }

    void main(List<String> args) {
    final estudiante1 = Estudiante("Hugo", 15);
    estudiante1.mostrarDatos();

    final profesor1 = Profesor("Paco", 25);
    profesor1.mostrarDatos();

    final directivo1 = Directivo("Luis", 30);
    directivo1.mostrarDatos();
    }

---

#### Ejecucion de metodos de la superclase

    class User {
      String nombre = "";
      int edad = 0;
      User(this.nombre, this.edad);

      void mostrarDatos() {
        print("Nombre: $nombre");
        print("Edad $edad");
      }
    }

    class Estudiante extends User {
      Estudiante(String nombre, int edad) : super(nombre, edad);

      @override
      void mostraDatos() {
        print("Estudiante");
        super.mostrarDatos();
      }
    }

    class Profesor extends User {
      Profesor(String nombre, int edad) : super(nombre, edad);

      @override
      void mostraDatos() {
        print("Profesor");
        super.mostrarDatos();
      }
    }

    class Directivo extends User {
      Directivo(String nombre, int edad) : super(nombre, edad);

      @override
      void mostraDatos() {
        print("Directivo");
        super.mostrarDatos();
      }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante("Hugo", 15);
      estudiante1.mostrarDatos();

      final profesor1 = Profesor("Paco", 25);
      profesor1.mostrarDatos();

      final directivo1 = Directivo("Luis", 30);
      directivo1.mostrarDatos();
    }

---

## Clase Abstractas con metodos

- Permites la creacion de metodos y propiedades generales
sin su implementacion
- No son instanciables

---

    abstract class User {
      String? nombre;
      int? edad;

      void mostarDatos();
    }

    class Estudiante extends User {
      void mostrarDatos() {
        print("Estudiante");
        print("Nombre: $nombre");
        print("Edad: $edad");
      }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Alex";
      estudiante1.edad = 50;
      estudiante1.mostarDatos();
    }

---

#### Clases abstractas con constructores

    abstract class User {
      String? nombre;
      int? edad;

      User(this.nombre, this.edad);
      void mostrarDatos();
    }

    class Estudiante extends User {
      Estudiante(String nombre, int edad) : super(nombre, edad);
      void mostrarDatos() {
        print("Estudiante");
        print("Nombre $nombre");
        print("Edad: $edad");
      }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante("Alex", 50);
      estudiante1.mostrarDatos();
    }

---

#### Interfaces

    class User {
      String? nombre;
      int? edad;

      void mostrarDatos() {}
    }

    class Estudiante implements User {
      String? nombre;
      int? edad;

      void mostrarDatos() {
        print("Estudiante");
        print("Nombre $nombre");
        print("Edad $edad");
      }
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Alex";
      estudiante1.edad = 52;
      estudiante1.mostrarDatos();
    }

---

#### Multi interfaces

    class User {
      String? nombre;
      int? edad;

      void mostrarDatos() {}
    }

    class Estudiante implements User, Materia {
      String? nombre;
      int? edad;
      String? materia;

      void mostrarDatos() {
        print("Estudiante");
        print("Nombre: $nombre");
        print("Edad $edad");
      }
    }

    class Materia {
      String? materia;
    }

    void main(List<String> args) {
      final estudiante1 = Estudiante();
      estudiante1.nombre = "Alex";
      estudiante1.edad = 50;
      estudiante1.mostrarDatos();
      estudiante1.materia = "Matematicas";
      print("Materia: ${estudiante1.materia}");
    }

---

### Atributos y metodos de clase (estaticos)
#### Propiedades de instancia

    void main(List<String> args) {
      final usuario1 = User();
      final usuario2 = User();
      print(usuario1.maxUsers);
      print(usuario2.maxUsers);
    }

    class User {
      int maxUsers = 10;
    }

---

#### Propiedades de clase

    void main(List<String> args) {
      print(User.maxUsers);
    }

    class User {
      static int maxUsers = 10;
    }

---

#### Metodos de clase

    void main(List<String> args) {
      print(User.maxUsers);
      print("Maximo de usuarios: ${User.getMAxUsers()}");
    }

    class User {
      static int maxUsers = 10;

      static int getMAxUsers() {
        return maxUsers;
      }
    }
