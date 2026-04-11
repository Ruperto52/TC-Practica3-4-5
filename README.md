## Información de los Integrantes
* **Institución:** Instituto Politécnico Nacional (IPN)
* **Escuela:** Escuela Superior de Cómputo (ESCOM) 
* **Unidad de Aprendizaje:** Teoría de la Computación 
* **Programa Académico:** Ingeniería en Sistemas Computacionales / Plan 2020 
* **Grupo:** 4CM4
* **Alumnos:** 
   * Diego Ruperto Hernandez (Boleta: 2024630696)
   * Maria Jose Venegas Martinez (Boleta: 2024630831)

---

## Objetivo
El propósito de esta práctica es profundizar en la comprensión y aplicación de los Autómatas Finitos No Deterministas (AFND) mediante el uso de JFLAP, y desarrollar una aplicación con interfaz gráfica que permita simular Autómatas Finitos Deterministas (AFD) a partir de diferentes formatos de entrada.

## Introduccion 
En esta practica exploraremos los conceptos de: **Expreciones Regulares**, **Automata Finito No Determinista**, **Automata Finito No Determinista con transiciones lamda** y por ende **El Teorema De Kleene** todos estos conceptos recopilan nuestro conocimiento previo, tenemos que aplicar tanto los conceptos vistos en las practicas anteriores y probar estos nuevos conceptos en esta practica.

### **Expreciones Regulares**
Las expresiones regulares son un equivalente algebraico para un aut´omata. Utilizado en muchos lugares
como un lenguaje para describir patrones en texto que son sencillos pero muy ´utiles. Pueden definir
exactamente los mismos lenguajes que los aut´omatas pueden describir: Lenguajes regulares. Adem´as,
ofrecen algo que los aut´omatas no: Manera declarativa de expresar las cadenas que queremos aceptar.

De forma mas precisa, Las expresiones regulares denotan lenguajes. Por ejemplo, la expresi´on regular:
01∗ + 10∗ denota todas las cadenas que son o un 0 seguido de cualquier cantidad de 1’s o un 1 seguida
de cualquier cantidad de 0’s.

### **Autómata Finito No Determinista:**
Sea un autómata finito definido por la quíntupla  A=(Q,Σ,q0 ,δ,F) donde:
1. Q: es el conjunto finito de estados
2. Σ: es un alfabeto finito
3. q0 ∈ Q: es el estado inicial
4. F⊆Q: es un conjunto de estados finales o de aceptación
5. δ:Qx(∑∪{ε})→ P(Q): cuando contiene transiciones vacías
6. δ:Qx∑→ P(Q) ó δ: {qi,x,qj | qi 〖,q〗j ∈Q;x∈∑} - (del estado qi mediante el terminal x se va a qj  ), es la función de transición. 

### **Autómata Finito No Determinista Con Transiciones lamda:**
Es un modelo matemático formado por una quíntupla $N_\lambda = \{\Sigma, S, S_0, F, \delta_\lambda\}$, donde:

1. ∑: Conjunto de símbolos de transición o alfabeto (entradas).
2. Q: Conjunto finito de estados de transición.
3. q0: Conjunto de estados de inicio $S_0 \subseteq S$.
4. F: Conjunto finito de estados de finalización o aceptación, donde $F \subseteq S$.
5. $\delta_\lambda : Función de transición, se define como:
  $$\delta_\lambda: S \times (\Sigma \cup \{\lambda\}) \to P(S), (\forall s \in S \text{ y } \forall a \in \Sigma)$$

### **El Teorema De Kleene**
//to do: Pendiente por hacer la investigacion dentro de aqui se va a explicar, detalladamente pero iguamente de forma resumida como es que se se hacen los cambios entre AFD,AFN,AFN-Lambda,ExpresionesRegulares

## Funcionalidades del Sistema
La aplicación (desarrollada en Python con Tkinter) implementa los siguientes módulos:

1. **Subcadenas, Prefijos y Sufijos:**
   * Cálculo exhaustivo de todas las subcadenas, prefijos y sufijos de una cadena de entrada.
   * Interfaz gráfica organizada para la visualización de resultados.
   * Funcionalidad para guardar los resultados obtenidos en un archivo de texto (.txt).

2. **Cerraduras de Kleene y Positiva:** 
   * Cálculo de la cerradura de Kleene ($\Sigma^*$) y la cerradura positiva ($\Sigma^+$) para un alfabeto definido.
   * Opción para especificar la longitud máxima de las cadenas a generar.
   * Visualización interactiva y opción de exportación de resultados.

3. **Automatas Finitos Deterministas (Carga):**
   * Carga de AFD por distintos documentos, tanto .jff y .json.
   * Se nuestra el modelo del AFD. 
   * Apartir de estos datos se crea la quintupla de el AFD.
   * Opción para probar cualquier cadena en el ADF.
   * Visualización del camino tomado por cada digito de la cadena entre los estados del AFD hasta ser rechazada o aceptada.

4. **Automatas Finitos Deterministas (Construye):**
   * Opción de especificar la quintupla de un AFD de forma manual.
   * Apartir de esos datos se crea el diagrama del AFD.
   * Opción para probar cualquier cadena en el ADF.
   * Visualización del camino tomado por cada digito de la cadena entre los estados del AFD hasta ser rechazada o aceptada.
   * Se muestra el modelo del AFD. 
   * Opcion de guardar el modelo del AFD en los archivos .jff y .json

5. **Operaciones con AFN-> AFD y el AFD (Simplificado):**
    * Permite cargar el AFN para poder vizualizar como es que se ve de forma grafica
    * Permite hacer la conversion del AFN a un AFD
    * Permite la visualizacion de la conversion del AFD
    * Opcion para guardar el AFD que se haya creado
    * Permite minimizar/simplicar el AFD

6. **Operaciones con AF -> ER :**
    * Del AF que se cargo previamente en la pestaña anterior convertirlo en una expresion regular

7. **Operaciones con ER -> AF :**
    * Permite ingresar una expresion regular para poder transformarla a un Automata Finito
    * Una vez creado el AF permite vizualizar como es que este se ve
    * Opcion de poder guardar el AF convertido de la Expresion Regular 

## Instalación de entorno virtual
 **Instalación y Configuración de Python:** Antes de comenzar a utilizar **Tkinter** para desarrollar la interfaz gráfica de la práctica, es necesario tener Python instalado y configurado. Para ello, siga los siguientes pasos:

1.**Instalar Python**

* Descargue Python: Visite la página oficial de Python en https://www.python.org/downloads/.
* Instale Python: Ejecute el instalador. Durante la instalación, asegúrese de marcar la casilla **"Add Python to PATH"** para que Python se pueda ejecutar desde cualquier terminal.
* Verifique la Instalación : Una vez instalado, abra una terminal (símbolo del sistema en Windows o terminal en macOS/Linux) y ejecute el siguiente comando:

```
python --version
```

Esto debería mostrar la versión instalada de Python. Para esta aplicacion ocuparemos la version de python 3.12.3

2.**Instalar Visual Studio Code**

Visual Studio Code (VS Code) es un entorno de desarrollo ligero y flexible que puede utilizar para programar en Python.
* Descargue VS Code: Diríjase al sitio oficial de Visual Studio Code y descargue la versión para su sistema operativo.
* Instale la Extensión de Python: Abra **VS Code**, diríjase a la pestaña de **Extensiones** (ícono de cubo en la barra lateral), busque e instale la extensión de **Python**. Esto habilitará herramientas adicionales como el resaltado de sintaxis y depuración para Python.

## Preparación del entorno virtual
1.**Crear un Entorno Virtual en Python**

Es recomendable trabajar en entornos virtuales para mantener las dependencias del proyecto aisladas. A continuación, se explica cómo crear un entorno virtual para su proyecto:
* Abra una terminal en Visual Studio Code.
* Navegue hasta la carpeta de su proyecto o cree una nueva carpeta para su proyecto con:

```
mkdir MiProyecto
cd MiProyecto
```

* Cree un entorno virtual ejecutando el siguiente comando:

```
python -m venv venv
```

Esto creará una carpeta llamada venv que contendrá su entorno virtual.

* Active el entorno virtual :
   * En Windows: ```venv\Scripts\activate```
   * En macOS/Linux: ```source venv/bin/activate```

* Verifique que el entorno está activado: El nombre del entorno (venv) debería aparecer al principio de la línea en su terminal.

2.**Instalar Tkinter**

Con el entorno virtual activado, instale el paquete de Tkinter, que es necesario para desarrollar la interfaz gráfica.
Para ello, ejecute el siguiente comando en la terminal:

   * En Windows: ```pip install tk```
   * En macOS/Linux: ```sudo apt-get install python3-tk   ```

**Probar un Programa Simple en Tkinter**
* Cree un archivo Python: En la carpeta de su proyecto, cree un archivo con el nombre **app.py**.
* Escriba el siguiente código básico en el archivo app.py para probar Tkinter:

 ```python
from tkinter import Tk, Label

app = Tk()
app.title("Hola mundo")
label = Label(app, text="¡Hola, mundo!")
label.pack()
app.mainloop()   
```

* Ejecute el archivo desde la terminal : ```python app.py```

* Verifique que se abre la aplicación: Esto debería abrir una ventana de navegador con el mensaje: **¡Hola Mundo!**

Recomendación
Asegúrese de activar el entorno virtual cada vez que trabaje en su proyecto, para garantizar que las dependencias se instalen correctamente en el entorno aislado.

Una vez listo nuestro compilador, nuestro lenguaje de programacion y las librerias que instalamos dentro de nuestro entorno virtual aislado pasaremos con la funcionalidad de nuestro codigo. 

# Funcionalidad del código

## Logica de las cadenas (Operaciones sobre cadenas) ```strings_logic.py```

### Prefijos: 
Un prefijo es una subcadena que aparece al inicio de una cadena original $w$. Formalmente, una cadena $x$ es un prefijo de $w$ si existe una cadena $y$ tal que $w = xy$.

$$P(w) = \{x \mid \exists y \in \Sigma^*, w = xy\}$$

**Implementacion del codigo**
```python
def get_prefixes(string):
    """Calcula todos los prefijos de una cadena."""
    # Retorna una lista de rebanadas (slices) desde el inicio
    return [string[:i] for i in range(len(string) + 1)] 
```
**Como funciona**:
**Rango de Iteración**: El range(len(string) + 1) asegura que se incluya desde el índice 0 hasta la longitud total, permitiendo capturar tanto la cadena vacía ($\lambda$) como la cadena completa.
**Slicing Dinámico**: Utiliza la sintaxis de Python [:i] para extraer subcadenas que comienzan siempre en la posición inicial (índice 0) y terminan en la posición $i$.
**Comprensión de Listas**: Genera la colección completa de prefijos en una sola línea, manteniendo una complejidad de tiempo $O(n^2)$ debido a la creación de las subcadenas.Resultado Estructurado: Para una cadena como "abc", la función devuelve de forma ordenada: ['', 'a', 'ab', 'abc'].

### Sufijos: 
Un sufijo es una subcadena que aparece al final de una cadena original $w$. Formalmente, una cadena $y$ es un sufijo de $w$ si existe una cadena $x$ tal que $w = xy$.

$$S(w) = \{y \mid \exists x \in \Sigma^*, w = xy\}$$

**Implementacion del codigo**
```python
def get_suffixes(string):
    """Calcula todos los sufijos de una cadena."""
    # Retorna una lista de rebanadas (slices) hasta el final
    return [string[i:] for i in range(len(string) + 1)] 
```
**Como funciona**:
**Desplazamiento del Índice**: El range(len(string) + 1) define el punto de inicio de cada subcadena. Al incrementar $i$, el punto de corte se mueve hacia la derecha.
**Slicing Inverso**: Utiliza la sintaxis de Python [i:] para extraer todo el contenido desde la posición $i$ hasta el último carácter de la cadena original.
**Inclusión de la Cadena Vacía**: Cuando $i$ alcanza el valor de len(string), el slice [len:] genera automáticamente la cadena vacía ($\lambda$), cumpliendo con la definición formal de sufijos.
**Orden de Generación**: Para una cadena como "abc", la función genera los sufijos en orden decreciente: ['abc', 'bc', 'c', ''].

### Subcadenas:
Una subcadena es cualquier segmento contiguo de una cadena original $w$. Formalmente, una cadena $z$ es una subcadena de $w$ si existen dos cadenas $x, y \in \Sigma^*$ tales que $w = xzy$.

$$\text{Sub}(w) = \{z \mid \exists x, y \in \Sigma^*, w = xzy\}$$

**Implementacion del codigo**
```python
def get_substrings(string):
    """Calcula todas las subcadenas posibles ordenadas por longitud."""
    substrings = {""} # Inicializa con la cadena vacía (λ)
    n = len(string)
    for i in range(n):
        for j in range(i + 1, n + 1):
            substrings.add(string[i:j])
    return sorted(list(substrings), key=lambda x: (len(x), x))
```
**Como funciona**:
**Doble Iteración (Anidada)**: Utiliza dos ciclos for para definir los límites de cada segmento. El índice i marca el inicio de la subcadena, mientras que j marca el final (exclusivo).
**Uso de Conjuntos (set)**: Se utiliza substrings = {""} para evitar duplicados de forma eficiente. Esto es crucial cuando la cadena original tiene caracteres repetidos (ej. "aaaa").
**Slicing de Rangos**: La operación string[i:j] extrae todas las combinaciones posibles de caracteres contiguos dentro del rango $[i, j)$.
**Criterio de Ordenamiento**: La función sorted utiliza una llave lambda para organizar los resultados primero por su longitud (len(x)) y, en caso de empate, de forma alfabética (x).
**Resultado Estructurado**: Para una cadena "abc", el conjunto se transforma en una lista ordenada: ['', 'a', 'b', 'c', 'ab', 'bc', 'abc'].

## Logica de las lenguajes (Operaciones sobre Lenguajes) ```languajes_logic.py```
Este módulo implementa las operaciones de potencias de un alfabeto $\Sigma$ para generar conjuntos de cadenas según las reglas de los lenguajes formales.

### Detalles tecnicos de Implementacion
* **Uso de ```itertools```**: Se eligió esta librería estándar de Python porque es altamente eficiente para manejar combinaciones y permutaciones, evitando el uso de múltiples ciclos anidados manuales que aumentarían la complejidad computacional.
* **Concatenación**: Debido a que ```itertools.product``` devuelve tuplas $(ej: ('a', 'b'))$, utilizamos ```''.join(c)``` para unir esos caracteres en una sola cadena de texto $("ab")$ antes de mostrarla en la interfaz.

### Cerradura de Kleene
La cerradura de Kleene de un alfabeto $\Sigma$, denotada como $\Sigma^*$, es el conjunto de todas las cadenas posibles que pueden formarse con los símbolos de $\Sigma$, incluyendo la cadena vacía ($\lambda$). Formalmente, es la unión infinita de potencias del alfabeto.

$$\Sigma^* = \bigcup_{i=0}^{\infty} \Sigma^i = \Sigma^0 \cup \Sigma^1 \cup \Sigma^2 \cup \dots$$

**Implementacion del codigo**
```python
def get_kleene_closure(alphabet, max_n):
    """Calcula la unión de Sigma^0 hasta Sigma^n."""
    closure = set()
    for i in range(max_n + 1):
        # Acumula las potencias desde i = 0 hasta max_n
        closure.update(get_sigma_n(alphabet, i))
    return sorted(list(closure), key=lambda x: (len(x), x))
```
**Como funciona**:
**Unión de Potencias**: Utiliza un ciclo for que itera desde $0$ hasta max_n. En cada paso, invoca a una función auxiliar (get_sigma_n) que genera todas las combinaciones de longitud exacta $i$.
**Base de la Cerradura**: Al iniciar el rango en $0$, la función garantiza la inclusión de $\Sigma^0$, que por definición siempre contiene únicamente a la cadena vacía ($\lambda$).
**Estructura de Conjunto**: El uso de set() y el método .update() asegura que no existan elementos duplicados durante la construcción del lenguaje, permitiendo una gestión de memoria eficiente.
**Ordenamiento Canónico**: Al igual que en las subcadenas, el resultado final se organiza primero por longitud y luego de forma lexicográfica, lo que facilita la lectura del lenguaje generado.
**Resultado Estructurado**: Para $\Sigma = \{a, b\}$ y $n=2$, el resultado es: ['', 'a', 'b', 'aa', 'ab', 'ba', 'bb'].

### Cerradura Positiva
La cerradura positiva de un alfabeto $\Sigma$, denotada como $\Sigma^+$, es el conjunto de todas las cadenas posibles que pueden formarse con los símbolos de $\Sigma$, con una longitud mínima de 1. 
Formalmente, es la cerradura de Kleene excluyendo la cadena vacía ($\lambda$).

$$\Sigma^+ = \Sigma^* - \{\lambda\} = \bigcup_{i=1}^{\infty} \Sigma^i$$

**Implementacion del codigo**
```python
def get_positive_closure(alphabet, max_n):
    """Calcula la unión de Sigma^1 hasta Sigma^n."""
    closure = set()
    for i in range(1, max_n + 1):
        # El rango inicia en 1 para excluir la cadena vacía
        closure.update(get_sigma_n(alphabet, i))
    return sorted(list(closure), key=lambda x: (len(x), x))
```
**Como funciona**:
**Exclusión de $\Sigma^0$**: A diferencia de la cerradura de Kleene, el ciclo for inicia en $1$. Esto garantiza que todas las cadenas generadas tengan al menos un símbolo del alfabeto original.
**Crecimiento Exponencial**: La función acumula los conjuntos de cadenas de longitud $1, 2, \dots, n$. El tamaño del conjunto resultante crece según la fórmula $|\Sigma|^1 + |\Sigma|^2 + \dots + |\Sigma|^n$.
**Gestión de Memoria**: Al igual que en los módulos anteriores, el uso de set().update() permite integrar las potencias del alfabeto eliminando cualquier redundancia técnica antes de la conversión final a lista.
**Criterio de Ordenamiento**: El resultado se entrega organizado bajo un esquema de longitud ascendente y luego lexicográfico, lo cual es el estándar para representar lenguajes formales en computación.
**Resultado Estructurado**: Para $\Sigma = \{0, 1\}$ y $n=2$, el resultado es: ['0', '1', '00', '01', '10', '11'].

## Logica de los AF
//Explicar el nuevo automaton_logic.py

## Implementacion dentro del ```main.py```

### Pestaña 1
### Pestaña 2
### Pestaña 3
### Pestaña 4
### Pestaña 5
### Pestaña 6
### Pestaña 7


## Como ocupar el software
### Primeros pasos
Lo primero que haremos sera como anteriormente lo habiamos explicado crear nuestro entorno virtual,en el cual debemos de verificar que la version de ```python es 3.12.3```, una vez comprobado esta version lo que tenemos que hacer es instalar Tkinter, la version que ocuparemos de Tkinter sera: ```8.6.14``` dentro de nuestro entorno virtual para estar listos para poder ejecutar el programa y asi ver la interfaz grafica.

* Para saber que version tenemos dentro de nuestro entorno virtual desde la linea de comando es: 
  * Saber version de python: ```python3 --version```
  * Saber que version de Tkinter: ```python3 -m tkinter```

Una vez creado nuestro entorno virtual y la libreria de Tkinter estamos listos para ejecutar el comando dentro de la terminal para compilar asi nuestro archivo principal que seria el comando: 

```
python3 main.py
```

Se desplegara la interfaz grafica con la pestaña de logica de cadenas, que nos permitira calcular el **sufijo, prefijo y subcadena**.
* El usuario debera introducir una cadena de la longitud que sea necesaria. 
* Una vez ingresada la cadena se mostraran los resultados dentro de la misma interfaz grafica.

Dentro de la otra pestaña tenemos la de logica de lenguajes que nos permitira calcular **Cerradura de Kleene y la Cerradura Positiva**.
* El usuario debera introducir el  alfabeto separado por comas cada uno de los simbolos que se introduzcan, para despues pedir la longitud maxima que se podran tener en las cadenas. 
* Una vez ingresada la informacion generaremos los lenguajes que se mostraran dentro de la interfaz grafica.

//Explicar como es que se tienen que ocupar las demas pestañas del programa
