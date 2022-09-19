![image](https://camo.githubusercontent.com/35e9d7d200795e6ec6bbf764d7f700d8da81cb5bc28ef9787d104a22eb3293a6/68747470733a2f2f696d67732e7365617263682e62726176652e636f6d2f37315a705a5949444b4a46463468797a765a5f4b6133636f2d625875356d5330756f496a637635757679342f72733a6669743a313230303a3638373a312f673a63652f6148523063446f764c336433647935312f593239734c6d31344c324e76626e526c2f626e51765932317a4c7a6b76615731682f5a3255765657526c51305644556c4d342f4d4734756347356e)
# Universidad de Colima
## Facultad de Ingeniería mecánica y Eléctrica
### Ingeniería em Computación Inteligente

---

#### Alumno: Luis Angel Ruiz Hurtado
#### Profesor: Dr. Walter Alexander Mata Lopez

---

## Introducción
#### Aqui se mostraran los codigos trabajados en clase durante la primera parcial

---

* Print

      print("Hola mundo")
     
* Encabezados en Markdown

      ## Universidad de Colima
      ## Facultad de Ingeniería mecánica y Eléctrica
      ### Ingeniería em Computación Inteligente
      
* Interpolacion de cadenas

      name="Luis"
      edad=19
      print("hola",name,"tienes",edad,"años")
      
* Interpolacion de cadenas con fstrings

      mensaje=f"hola {name} ,tienes {edad} años"
      mensaje
      print(mensaje)
      print(f"hola {name},tienes {edad} años")
      
* Funciones

      def saludo():

        print("Hola mundo")

      mi_funcion=saludo()    
      saludo()               
      print(mi_funcion)

      def saludo2():
        return"Hola mundo"
        saludo2()  

      mi_funcion2= saludo2()
      print(mi_funcion2)

      a=5
      b=10
      res = f" La suma de {a}+{b} = {a+b}"
      print(res)

      def suma(a,b):

        return a+b

      res = f"La suma de {a}+{b} = {suma(a,b)}"
      print(res)
      
* Listas, sets, Tuplas y Diccionarios

      lista_numeros = ["uno","dos","tres"]
      msg_numeros= f"Numeros:{lista_numeros}"
      print(msg_numeros)

      tupla_numeros=("uno","dos","tres")
      msg_numeros=f"numeros:{tupla_numeros}"
      print(msg_numeros)

      set_numeros={"1","2","3","4","5","6","7","8","9","10"}
      print(set_numeros)

      dict_numeros={"1":"uno","2":"dos","3":"tres"}
      msg_dict_numeros=f"numeros:{dict_numeros}"
      print(msg_dict_numeros)

      dos= f"Numeros:{dict_numeros['2']}"
      print(dos)
      
* Escribir una funcion, que retorne por fstrings el mensaje "Hola -nombre- tienes -edad- años"

       nombre="Luis"
       edad=19
       
       def msj(nombre, edad):
        return(nombre, edad)
       
       mensaje=f"Hola {nombre} tienes {edad} años"
       print(mensaje)
       
* Ejemplos de listas con fstrings

      alumnos=["Hugo", "Paco", "Luis", "Paola", "Laura"]
      materia1=[10,9,10,8,10]
      materia2=[7,7,8,7,9]
      materia3=[6,7,8,9,5]
      materia4=[6,6,7,6,7]

      encabezado=["Nombre", "Estructura de Datos", "Ecuaciones Diferenciales", "Metodos numericos", "Programacion funcional"]

      def reporte(fmt):
          print(f"{encabezado[0]:^{fmt}} {encabezado[1]:^{fmt}} {encabezado[2]:^{fmt}} {encabezado[3]:^{fmt}} {encabezado[4]:^{fmt}}")
          for i in range(5):
              print(f"{alumnos[i]:^{fmt}} {materia1[i]:^{fmt}} {materia2[i]:^{fmt}} {materia3[i]:^{fmt}} {materia4[i]:^{fmt}}")

      reporte(20)
      
* Funciones con manejo de fstring

  		# %%
		def saludo_edad_(nombre:str,a_nacimiento:int):
				edad= 2022-a_nacimiento
				print("Hola",nombre,"tienes",edad,"años")

		def calcular_edad(a_actual:int,a_nacimiento:int)->int:
				return a_actual-a_nacimiento

		def saludo(nombre:str,edad:int):
				print ("Hola",nombre,"tienes",edad,"años")

		def cuadrados(numu:int,numd:int):
				return (numu*numu) + (numd*numd)
		if __name__=="__main__":
				print(cuadrados(2,2))
		# %%
		def tabla(x):
				for i in range (11):
						print(x,"*",i,"=",x*i)


		if __name__=="__main__":
				print(tabla(3))
		# %%
		#Clase del 12 de septiembre 
		def tabla(t,n):
				for i in range (1,n+1):
						print(t,"*",i,"=",t*i)
		if __name__=="__main__":
				print(tabla(3,2))
		# %%
		def tabla(t:int,n:int,spc:int):
				for i in range (1,t+1):
						for j in range (1,n+1):
								print(f""i,"*",j,"=",i*j)
		t=int(input("¿Hasta que tablas quieres calcular?"))
		n=int(input("¿Hasta que numero quieres calcular?"))
		tabla(t,n)
		# %%
		def tabla(t:int,n:int,spc:int):
				for i in range (1,t+1):
						for j in range (1,n+1):
								print(f"{i:^{spc}} * {j:^{spc}} = {i*j:^{spc}}")
		t=int(input("¿Hasta que tablas quieres calcular?"))
		n=int(input("¿Hasta que numero quieres calcular?"))
		spc=int(input("¿Que espaciado quieres?"))
		tabla(t,n,spc)
    
* Suma

      def sum(num:int,num2:int)->int: return num+num2

      if __name__ == "__main__":
          print(suma(3,7))

* Resta

      def res(num: int, num2: int) -> int: return num - num2

      if __name__ == "__main__":
          print(resta(3, 7))

* Multiplicacion

      def mult(num: int, num2: int) -> int: return num * num2

      if __name__ == "__main__":
           print(multi(3, 7))
         
* Division

      def divisi(num: int, num2: int) -> float: return num / num2

      if __name__ == "__main__":
          print(divisi(3, 7))
        
* Cuadrado

      def cuadrado(num: int) -> int: return num*num

      if __name__ == "__main__":
          print(cuadrado(3))
        
---

* Uso de listas

      i_lista=[1,2,3,4]
      print(mi_lista)
      lista_vacia=[]
      print(lista_vacia)


      mi_lista2=[1,"Hola",True,3.14,[1,2,3],(1,2,3),{1,2,3}]
      print(mi_lista2)

      print(len(mi_lista))
      print(len(mi_lista2))
      print(f"Mi lista:{mi_lista}")

      print(f"No de elementos:{len (mi_lista)}")
      print(f"Primer elemento:{mi_lista[0]},{mi_lista[1]},{mi_lista[2]},{mi_lista[3]}")
      print(f"Primer elemento:{mi_lista[-1]},{mi_lista[-2]},{mi_lista[-3]},{mi_lista[-4]}")
    
* Slices: Partes de una lista

      print(mi_lista[1:-1])
      print(mi_lista[0:3])
      print(mi_lista[0:])
      print(mi_lista[:])

* Modificar

      mi_lista[2]="tres"
      print(mi_lista)

      ml.extend([6,7,8])
      print(ml)

      ml.insert(4,"cinco")
      print(ml)

      del ml[5]
      print(ml)

      ml.remove(2)
      print(ml)

      ml.reverse()
      print(ml)

      l1=[1,2,3]
      l2=l1[:]
      print(l1)
      l1.reverse()
      print(l1)
      print(l2)
    
* Insertar elementos en una lista

      new_lista=[5,"seis",7,8]
      mi_lista[len(mi_lista):]=new_lista
      print(mi_lista)

      mi_lista=[1,2,3,4]
      mi_lista.append("cinco")
      print(mi_lista)

      ml=[]
      for i in range(1,5):
          ml.append(i)
      print(ml)
    
* Ordenar elementos de una lista

      ld=[[5,4,6],[7,8,2,1],[3,4,5],[6,7]]
      print(f"Desordenado: {ld}")
      ld.sort()
      print(f"Ordenado: {ld}")

      ld=[5,4,6,7,8,2,1,3,4,5,6,7]
      S1= sorted(ld)
      print(S1)
      ld=[5,4,6,7,8,2,1,3,4,5,6,7]
      S2= sorted(ld,reverse=True)
      print(S2)

      ceros=[0,0,0,0,0,0,0,0,0]
      print(ceros)
      ceros=[0]*9
      print(ceros)

      valor_max=max(ld)
      print(valor_max)

      valor_min=min(ld)
      print(valor_min)

      cuatros=ld.count(4)
      print(cuatros)

      repe=[]
      for i in range (1,9):
          repe.append(ld.count(i))
      print(repe)			
    
----

## Caliz de examen

* Escribe una funcion que reciba como argumentos T y N donde T es el limite de tablas de multiplicar que se desean obtener y N hasta un valor de las tablas se desea. Todas empiezan desde 1

      def tablas(t:int,n:int):
          for i in range(1,t+1):
              tabla(i,n,10)

      def tabla(t:int,n:int,spc:int):
          for i in range (1,n+1):
              print(f"{t:^{spc}}x{i:^{spc}}={t*i:^{spc}}")

      t=int(input("¿Hasta que tablas quieres calcular?"))
      n= int(input("¿Hasta que numero quieres calcular?"))
      tablas(t,n)
