# Implementación del algoritmo de Deutsch-Jotza
El algoritmo de grover es importante porque muestra cómo utilizando computación cuántica se puede determinar una propiedad de una función evaluandola una sola vez.

En este trabajo, deben implementar el algoritmo de Deutsch-Jotza en qiskit. Deben tener presente los siguientes elementos:
- Dado que el algoritmo de grover utiliza una función oráculo, que se representa mediante una matriz unitaria $U_f$, en el código deben implementar una función que reciba una lista de tuplas de dos elementos, donde el primer elemento es el valor del dominio y el segundo elemento es el valor de la función. Por ejemplo, si el parámetro que recibe la función que genera $U_f$ a partir de la función $f(x)$ es `[[0, 1], [1,0]]` es porque $f(x)$ se define de la siguiente manera: 

$$
f(x) = 
\begin{cases} 1 & \text{si } x = 0 \\
0 & \text{si } x = 1
\end{cases}
$$

- Dado el valor de $n$, o sea el tamaño del arreglo donde se busca el elemento, el algoritmo debe generar el circuito con $n+1$ qubits. 

En resumen: Deben desarrollar un programa en qiskit que reciba una lista que representa la función $f(x)$ y genere el circuito cuántico que representa el algoritmo de Deutsch-Jotza para esa función en particular. 

**Nota 1:** Puede asumir que $x \in \\{ 0,1 \\} ^n$, donde $n$ es el número de qubits que tiene el circuito. 
**Nota 2:** Recuerde que el algoritmo de Dutsch-Jotza funciona para funciones balanceadas o constantes. En la función que calcula $U_f$ debe verificar que $f$ cumpla con las propiedades. 
