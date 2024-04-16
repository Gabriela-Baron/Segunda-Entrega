# Segunda-Entrega

 * INSTITUCION UNIVERSITARIA POLITECNICO GRANCOLOMBIANO
 * MODULO CONCEPTOS FUNDAMENTALES DE PPROGRAMACION [GRUPO B02]
 * ENTREGA PROYECTO 2 - SEMANA 5 
 * 
 * INTEGRANTES SUBGRUPO 10
 * ROBINSON AMADO PEÑA - 100273913
 * GABRIELA ALEXANDRA BARÓN BARRETO - 100285411
 * JEFERSON MEDINA GOMEZ - 100289745
 * KAROL MELISSA GOMEZ COLMENARES - 100252576
 */

La primera parte de la segunda entrega consistió en encontrar al vendedor que recaudó menos dinero, en donde tuvimos en cuenta el índice de Vendedor con menos ventas y las Ventas totales por vendedor, gracias a esto podemos ver el índice mínimo de ventas por vendedor.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/4d63acaf-0561-4020-9f19-0dc5ec6f4e73)

Para encontrar al vendedor que recaudó menos dinero, fue con ayuda del comando (System.out.println) buscamos al vendedor que recaudó menos dinero, en donde también codificamos para ver el nombre, apellido, tipo de documento, número de documento para finalizar mostrándonos el total recaudado. Luego le dimos un número a cada vendedor, esto con el fin de poder filtrar más rápido a cada vendedor y así mismo realizamos la operación matemática simplificando la ecuación para obtener el resultado para este vendedor. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/6ae06927-7271-446d-bdbc-6bf5366abad7)

Después pasamos a crear la lista de cadenas con la información de cada vendedor, generando los datos en el formato CSV, en la que tuvimos en cuenta la información de cada vendedor teniendo en cuenta sus respectivos nombres y apellidos para proceder a ver las ventas totales de cada uno de ellos.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/5d1d077e-661d-4d1d-a566-25cccbe3f1ec)

Nosotros organizamos la lista de cadenas por ventas totales de mayor a menor en la cual tuvimos presente la información de cada vendedor junto con el total del recaudo.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/84dfb033-04ac-4543-aca9-bb2a979aa2f1)


Para escribir en el archivo SCV ingresamos a la ruta del archivo, validamos por nombre y el total del recaudo para así visualizar la información de los vendedores. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/a8368b0a-d415-4dc4-adec-93ff35755f3e)




# NOVEDADES DEL CÓDIGO 

Se corrige el método para organizar a los vendedores por medio de las ventas totales de mayor a menor cantidad de dinero recaudado por cada vendedor. Utilizamos el algoritmo de ordenamiento como lo es el algoritmo de (BURBUJA) el cual nos sirvió para organizar los nombres como las ventas totales de cada vendedor. 

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/e928af3d-dc8e-4d44-ab76-d2b93f15d9a1)


En el código agregamos la variable (TEMP) la cual nos ayudo a almacenar temporalmente un valor durante la operación de intercambio, en este caso nos permitió utilizar esto para guardar los valores como nombre, apellido, tipo de documento de cada vendedor en el proceso de intercambio. 

NOTA: Si ocurre un error este se va imprimir en un mensaje de (ERROR) por consola señalando que tipo de error ocurrió, esto nos va a permitir identificar los bugs para así permitirnos solucionarlos, todo esto con base a la escritura de los archivos.



![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/10025a44-f344-4fac-9227-12e0f766c49f)


Esta parte del código es el encargado de escribir datos sobre los vendedores en un archivo CSV llamado (reporte_ventas_vendedores.csv) donde cada vendedor está representado como una fila de datos y los atributos del vendedor como una columna que está separada por punto y coma, la parte del código (BufferredWriter writer = new BufferedWriter( “reporte_ventas_vendedore.csv))), BufferedWriter es un “envoltorio” alrededor del FileWriter que lo que hace es mejorar la eficiencia de escritura. Y FileWriter se encarga de escribir en un archivo, si no existe, lo crea; si ya existe lo que hará es sobreescribirlo.


![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/01664fc4-bd91-4022-a5a0-5e7b5414759d)


Aquí también se añade uno de los puntos solicitados de la entrega, que los productos vendidos por cantidad están ordenados en forma descendente.

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/23cadc0b-c73b-4295-9020-1ced8a99e103)


En el código agregamos el método createSalesMenFile, el cual es el encargado de crear el archivo pseudoaleatorio CSV con los datos del vendedor que proporcionamos al cual se llamó productos.csv.

NOTA: Si ocurre un error este se va imprimir en un mensaje de (ERROR) por consola señalando que tipo de error ocurrió, esto nos va a permitir identificar los bugs para así permitirnos solucionarlos, todo esto con base a la escritura de los archivos.


![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/364df78a-4fa8-4249-8d66-3850c4b2c2c9)


Encontramos también una función en java llamada printProductsFile que nos permite imprimir el contenido del archivo por consola, adicional a eso incluimos FileName de tipo String que representa la ruta del archivo que se imprimirá. El bloque  Try-with-resources, es otra función para abrir y manejar un la lectura de archivos, en el caso de BufferedReader que lee el archivo fileName, hay que tener presente que cada una de las iteraciones del bucle éste va a leer una línea del archivo con el método readLine(), del BufferedReader y que Line (variable) es la linea leida que es la que almacena esta, si la línea no es nula, quiere decir que hay contenido y este va imprimir por consola utilizando el System.out.pintIn(Line).

![image](https://github.com/Gabriela-Baron/Segunda-Entrega/assets/164106618/d65ad97f-d1e5-442b-9cdd-0729ee85cc0b)

# CODIGO UTILIZADO EN LA SEGUNDA ENTREGA.

        // Encontrar el vendedor que recaudó menos dinero
		int indiceVendedorMenosVentas = 0;
        double minVentas = ventasTotalesPorVendedor[0];
        for (int i = 1; i < ventasTotalesPorVendedor.length; i++) {
            if (ventasTotalesPorVendedor[i] > minVentas) {
                 minVentas = ventasTotalesPorVendedor[i];
                 indiceVendedorMinVentas = i;
                
			}
			
		 // Mostrar el vendedor que recaudó menos dinero
		System.out.println("El vendedor que recaudó menos dinero es:");
		System.out.println("Nombre: " + nombresVendedores[indiceVendedorMasVentas]);
		System.out.println("Apellido: " + apellidosVendedores[indiceVendedorMasVentas]);
		System.out.println("Tipo de Documento: " + tipoDocumentos[indiceVendedorMasVentas]);
		System.out.println("Número de Documento: " + numeroDocumentos[indiceVendedorMasVentas]);
		System.out.println("Total Recaudado: " + ventasTotalesPorVendedor[indiceVendedorMasVentas]);
				
			}
		createSalesMenFile
		int n1, n2, n3;
		string CARLOS ANTONIO CASTRO BERNAL, VERONICA LISNEY CARO BUENO, ANDRES SOTO RODRIGUEZ

		n1 = ¨CARLOS CASTRO¨
		n2 = ¨VERONICA CARO¨
		n3 = ¨ANDRES SOTO¨ 


		n1 = INTEGRANTEs.parseInt(ventasTotalesPorVendedor(¨digite un numero: ¨));
		n2 = INTEGRANTEs.parseInt(ventasTotalesPorVendedor(¨digite un numero: ¨));
		n3 = INTEGRANTEs.parseInt(ventasTotalesPorVendedor(¨digite un numero: ¨));

		if ((n1>n2)&&(n2>n3)) {
			joptionPane.showMessageDialog(null,¨Order:¨+n1+¨ - ¨+n2+¨ - ¨+n3+¨);
			
		}
			
		}
		// GENERAR DATOS EN FORMATO CSV
    // CREAR LISTA DE CADENAS CON LA INFORMACIÓN DE CADA VENDEDOR
    List<String> infoVendedores = new ArrayList<String>();
    for (int i = 0; i < nombresVendedores.length; i++) {
      String info = nombresVendedores[i] + " " + apellidosVendedores[i] + ";"
          + ventasTotalesPorVendedor[i];
      infoVendedores.add(info);
    }

    // ORDENAR LA LISTA DE CADENAS POR VENTAS TOTALES DE MAYOR A MENOR
    Collections.sort(infoVendedores, Collections.reverseOrder());

    // ESCRIBIR ARCHIVO CSV
    FileWriter writer = null;
    String rutaArchivo = "./reporte_ventas.csv";
    try {
      writer = new FileWriter(rutaArchivo);
      writer.write("Nombre;Total Recaudado\n");
      for (String info : infoVendedores

	  //NOVEDADES DEL CODIGO

	ORDENAR VENDEDORES POR VENTAS TOTALES (Burbuja)
        for (int i = 0; i < ventasTotalesPorVendedor.length - 1; i++) {
            for (int j = 0; j < ventasTotalesPorVendedor.length - 1 - i; j++) {
                if (ventasTotalesPorVendedor[j] < ventasTotalesPorVendedor[j + 1]) {
                    // Intercambiar valores
                    double tempVentas = ventasTotalesPorVendedor[j];
                    ventasTotalesPorVendedor[j] = ventasTotalesPorVendedor[j + 1];
                    ventasTotalesPorVendedor[j + 1] = tempVentas;


                    // Intercambiar datos de vendedores correspondientes
                    String tempNombre = nombresVendedores[j];
                    nombresVendedores[j] = nombresVendedores[j + 1];
                    nombresVendedores[j + 1] = tempNombre;


                    String tempApellido = apellidosVendedores[j];
                    apellidosVendedores[j] = apellidosVendedores[j + 1];
                    apellidosVendedores[j + 1] = tempApellido;


                    String tempTipoDocumento = tipoDocumentos[j];
                    tipoDocumentos[j] = tipoDocumentos[j + 1];
                    tipoDocumentos[j + 1] = tempTipoDocumento;


                    String tempNumeroDocumento = numeroDocumentos[j];
                    numeroDocumentos[j] = numeroDocumentos[j + 1];
                    numeroDocumentos[j + 1] = tempNumeroDocumento;
	
	//SE AÑADE LA LINEA DE CATCH  (I0Exception e) {..}
	catch (IOException e) {
            System.err.println("Error al escribir en el archivo CSV: " + e.getMessage());

	//Bloque para abrir el archivo en modo de escritura
	try (BufferedWriter writer = new BufferedWriter(new FileWriter("reporte_ventas_vendedores.csv"))) {
		writer.write("Nombre;Apellido;Tipo Documento;Numero Documento;Ventas Totales\n");
		for (int i = 0; i < nombresVendedores.length; i++) {
			writer.write(nombresVendedores[i] + ";" + apellidosVendedores[i] + ";" + tipoDocumentos[i] + ";" + numeroDocumentos[i] + ";" + ventasTotalesPorVendedor[i] + "\n");

			System.out.println("Productos vendidos por cantidad, ordenados en forma descendente:");
            for (int i = 0; i < nombresProductos.length; i++) {
                System.out.println(nombresProductos[i] + ";" + " $ " + preciosProductos[i] + ";" + cantidadesTotales[i]);

	// Método para crear el archivo de productos con información pseudoaleatoria
	public static void createProductsFile( int productsCount) {
		String[] nombresProductos = {"VEHICULO", "CAMIONETA", "CAMION"};


		try (BufferedWriter writer = new BufferedWriter(new FileWriter("productos.csv"))) {
			writer.write("ID;Nombre;Precio\n");
			Random rand = new Random();
			for (int i = 1; i <= productsCount; i++) {
				int randomIndex = rand.nextInt(nombresProductos.length);
				int precio = rand.nextInt(10000) + 1000; // Precio aleatorio entre 1000 y 11000
				writer.write(i + ";" + nombresProductos[randomIndex] + ";" + precio + "\n");
			}
		} catch (IOException e) {
			System.err.println("Error al escribir en el archivo de productos: " + e.getMessage());
		}
		System.out.println("Archivo de productos generado correctamente.");
	}
	public static void printProductsFile(String fileName) {
            try (BufferedReader reader = new BufferedReader(new FileReader(fileName))) {
                String line;
                while ((line = reader.readLine()) != null) {
                    System.out.println(line);
                }
            } catch (IOException e) {
                System.err.println("Error al leer el archivo de productos: " + e.getMessage());





	


	

 





























