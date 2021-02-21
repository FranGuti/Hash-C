# TDA Tabla Hash
Es un trabajo realizado durante la cursada de Algoritmos y Programación II.
El mismo consta de la implementación y desarrollo del Tipo de Dato Abstracto Tabla Hash en el lenguaje de programación C. 
Tiene como objetivo la creación del mismo para posterior uso como librería con un correcto manejo de memoria, la implementación de un iterador propio que sea capaz de recorrer la tabla, y sus métodos :

 - Hash Crear
     > Crea y devuelve una Tabla Hash vacía

 - Hash Guardar
    >Recibe una clave y un valor, si la clave ya se encuentra en la tabla, reemplaza el valor de la misma
    
 - Hash Borrar
    >Borra el elemento de la tabla y devuelve el valor asociado
    
 - Hash Obtener
   > Devuelve el valor asociado en la tabla a la clave pasada por parámetro
 
 - Hash Pertenece
   > Devuelve True si el elemento está en la tabla, False en caso contario

 - Hash Cantidad
   > Devuelve la cantidad de elementos que hay en la Tabla

- Hash Destruir
  >Destruye la tabla de Hash
  

Las tablas Hash son un tipo de estructura para almacenar datos del tipo clave-valor. La particularidad de estas tablas es que logran realizar la búsqueda de un dato perteneciente con una complejidad algorítmica de O(1) en notación Big-O. 

¿Como lo logran?

Estas tablas básicamente son formadas por un arreglo en el cual se inserta el bloque Clave-Valor. Para conseguir el índice donde van a ser insertadas primero se pasa la clave por una función de Hashing, que es una simple función matemática con la capacidad de transformar la clave a un entero el cual se manipula para que sea un índice válido dentro de nuestro arreglo.
 Esto, por otra parte, tiene sus defectos ya que ocurren "colisiones" que se generan cuando dos claves adquieren el mismo índice en la tabla. Para estos casos la Tabla de Hash toma uno de dos caminos:
 

 - Hashing abierto
    > En el Hashing abierto cada índice del arreglo en vez de llevar un bloque clave-valor lleva una lista asociada que, ahora sí, esta contiene cada bloque clave-valor asociado a la posición en el arreglo
 - Hashing cerrado
   >En el Hashing Cerrado no se agregan listas, sino que el arreglo se convierte en un arreglo circular, es decir, un arreglo "infinito". Osea, si el arreglo tiene n posiciones la posición n+1 pasa a ser la primer ubicación. En el caso de que dos claves colisionen la nueva clave en vez de entrar en el índice "i" entraria en el índice "i+1". La desventaja de este sistema es que las redimensiones de la tabla se realizarian de manera mas frecuente.

También se implementa un Iterador Externo que implementa los métodos:

 - Iter Crear
    >Crea el iterador externo
 - Iter Avanzar
    >Si el iterador puede avanzar devuelve True, en caso contrario devuelve False
 - Iter Ver Actual
    >Devuelve el elemento sobre el cual está "parado" el iterador
 - Iter Al Final 
    >Devuelve True si el iterador esta en la última posición de la lista, False en caso contrario
 - Iter Destruir
   >Destruye el iterador
