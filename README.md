# ParcialHerramientasComputacionales

**Nombre: Mohamad Shayeb**

**Parcial de Herramientas Computacionales**

**Punto B**


1.Qué tipo de errores se presentaron o se pueden presentar con su implementación al problema?

•	se le pide al usuario responder con dos opciones (Estudiante/Docente) y el usuario ingresa un valor o respuesta distinto a las opciones dadas.

•	Errores encontrados en la estructura del código al compilarlo encontrados:
error al tratar de operar los datos obtenidos del usuario sin haberlos convertido a su tipo de dato

•	se le pide un dato numérico dentro de un rango, por ejemplo, cedula, el usuario ingresa un dato fuera de este rango.

Los errores producto de entrada del usuario son de errores en tiempo de ejecución.

Los errores producto de la estructura del código al compilarlo son errores de sintaxis.

2. Que estrategias podría usar para solucionar estos errores?

Los errores en tiempo de ejecución fueron solucionados mediante la implementación de validaciones frente a los casos de error como por ejemplo validación de tipos de datos y excepciones al leer los datos.

De las estrategias de depuración usamos La estrategia que más utilizo es vuelta atrás.



Integrantes: Mohamad Shayeb, Andres Diaz
Parcial de Herramientas computacionales
Punto A





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
        
