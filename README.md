# ParcialHerramientasComputacionales

**Nombre: Mohamad Shayeb/ Andres Diaz**

**Parcial de Herramientas Computacionales**

**Punto B**


**1.Qué tipo de errores se presentaron o se pueden presentar con su implementación al problema?**

•	se le pide al usuario responder con dos opciones (Estudiante/Docente) y el usuario ingresa un valor o respuesta distinto a las opciones dadas.

•	Errores encontrados en la estructura del código al compilarlo encontrados:
error al tratar de operar los datos obtenidos del usuario sin haberlos convertido a su tipo de dato

•	se le pide un dato numérico dentro de un rango, por ejemplo, cedula, el usuario ingresa un dato fuera de este rango.

Los errores producto de entrada del usuario son de errores en tiempo de ejecución.

Los errores producto de la estructura del código al compilarlo son errores de sintaxis.

**2. Que estrategias podría usar para solucionar estos errores?**

Los errores en tiempo de ejecución fueron solucionados mediante la implementación de validaciones frente a los casos de error como por ejemplo validación de tipos de datos y excepciones al leer los datos.

De las estrategias de depuración usamos La estrategia que más utilizo es vuelta atrás.



**Integrantes: Mohamad Shayeb, Andres Diaz**

**Parcial de Herramientas computacionales**

**Punto A**





def cafeteriaDescuento():

    cantidad=0
    

    while True:
        
        print('Seleccione una opción:')
        print('(1) Realizar compra')
        print('(0) Salir')


        # leer la opción del usuario 
        option = input('Opción: ')

        if option == '1':

            response = input('¿Es Estudiante o Docente de la universidad?(Estudiante/Docente): ')
            if response == 'Estudiante':
                print('Se le a identificado como estudiante')
             # terminar formulario y volver al menú
            elif response == 'Docente':
                print('Se le a identificado como docente ')
            elif response != 'Estudiante' and 'Docente':
                print('El valor ingresado es incorrecto, inténtelo nuevamente')
                continue # terminar formulario y volver al menú            

            cedula = input('Ingrese su cédula: ')

            # comprobar si el input del usuario es un número
            try:
                float(cedula)
            except ValueError:
                print('El valor ingresado no es un número de identificación correcto, inténtelo nuevamente')
                continue

            if len(cedula) < 10:
                print('El valor ingresado para su identificación es inválido, inténtelo nuevamente')
                continue # terminar formulario y volver al menú



        
            codigoDelProducto = input('Ingrese el codigo del producto: ')

            # comprobar si el input del usuario es un número
            try:
                float(codigoDelProducto)
            except ValueError:
                print('El valor ingresado no es un número de codigo correcto, inténtelo nuevamente')
                continue
            
            
            precioDelProducto= input('Ingrese el precio del producto: ')

            cantidad_productos = int(input('Ingrese la cantidad de unidades del producto:'))

            total1= float(precioDelProducto) * float(cantidad_productos) * 0.5

            total2= float(precioDelProducto) * float(cantidad_productos) * 0.2

            if response == 'Estudiante':
                print (total1)

            if response == 'Docente':
                print (total2)
                                                   
            if cantidad_productos <= 100:

                cantidad += cantidad_productos # contar la cita asignada
                print('Unidades'+ ' ' +str(cantidad_productos))                
            else:
                print('El valor ingresado es incorrecto, inténtelo nuevamente')
                continue # terminar formulario y volver al menú


                
            print('El ' + str(response) + ' con cedula ' + str(cedula) + ' debe pagar ' + str( total1 or total2 ) + ' por el producto ' + str(codigoDelProducto))

        # salir del ciclo
        if option == '0': break
            
cafeteriaDescuento()   

**Documentación en Software:**

**PROBLEMA**

Para recuperarse un poco del tiempo en cuarentena, las cafeterias de la universidad se encuentran dando descuentos a la comunidad estudiantil y dependiendo si es estudiante o profesor, tienen descuentos diferentes. Se desea saber entonces por cada compra cuanto debe pagar el usuario en caja. Para ello:

**Pida por teclado la siguiente informacion para el cliente: cedula y rol: profesor o estudiante** 

**Registrar el producto a comprar: codigo producto, cantidad de unidades y precio del producto. (un solo producto, varias unidades, por ejemplo: producto 076: gaseosa, 3 unidades)**

**Los descuentos estan dados de la siguiente forma: los estudiantes tienen un 50 % de descuento mientras que los profesores tienen un 20 % de descuento**

Al final el procedimiento por cada cliente deber´a imprimir el valor a pagar por sus productosde la forma: ”El Rol con cedula Numero, debe pagar Valor por el producto Codigo” Ejemplo: ”El profesor con Cedula 1454898 debe pagar $12.900 por el producto 076”.Tenga en cuenta que este valor final a pagar corresponde al precio de cada producto por lacantidad llevada menos el descuento otorgado, debe imprimir el rol y la cedula de cada cliente y el codigo del producto llevado en el mensaje.


El modelo computacional que usamos fue el Idle de python

**Input** 

Seleccione una opción:

(1) Realizar compra

(0) Salir

Opción: 1

¿Es Estudiante o Docente de la universidad?(Estudiante/Docente): Estudiante

Se le a identificado como estudiante

Ingrese su cédula: 9393939393

Ingrese el codigo del producto: 079

Ingrese el precio del producto: 2000

Ingrese la cantidad de unidades del producto:4

4000.0

**Output** 

El Estudiante con cedula 9393939393 debe pagar 4000.0 por el producto 079

**¿Como lo calcula?**

Si al correr el codigo se le identifica al programa que entro como Estudiante se le hace el descuento indicado el cual es el 50 porciento y si entra como docente se le aplica el 20 porciento.























        
