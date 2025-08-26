<h2>Pydantic<h2> 
Es la biblioteca de validación de datos más popular de Python, que puede convertir sugerencias de tipo en reglas de validación en tiempo de ejecución.
En lugar de escribir docenas de si isinstance() y funciones de validación personalizadas, define tu estructura de datos una sola vez utilizando la conocida sintaxis de Python.
Pydantic se encarga del resto: valida los datos entrantes, convierte los tipos cuando es necesario y proporciona mensajes de error claros cuando falla la validación.
Considera esta sencilla función de Python con sugerencias de tipo y la documentación adecuada:

def calculate_user_discount(age: int, is_premium_member: bool, purchase_amount: float) -> float:
   if age >= 65:
       base_discount = 0.15
   elif is_premium_member:
       base_discount = 0.10
   else:
       base_discount = 0.05
  
   return purchase_amount * base_discount

Este fragmento de código define una función calcular_descuento_usuario que calcula un descuento en función de la edad, el estado de afiliación y el importe de compra de un usuario. Aquí tienes un desglose: - La función toma tres parámetros: age (un entero), is_premium_member (un booleano) y purchase_amount (un flotante). - Comprueba la edad del usuario para determinar el descuento base: - Si el usuario tiene 65 años o más, recibe un descuento del 15% (descuento_base = 0,15). - Si el usuario es miembro premium, recibe un descuento del 10% (descuento_base = 0,10). - En caso contrario, el usuario recibe un descuento del 5% (descuento_base = 0,05). - La función devuelve el importe del descuento multiplicando el "importe_compra" por el "descuento_base". El objetivo es calcular el importe del descuento al que tiene derecho un usuario en función de su perfil y del importe que compra.

<h2>Funcionalidades clave<h2>
Validación de tipos:
Garantiza que los datos se ajusten a los tipos especificados en el modelo, fallando la creación del modelo si los datos son inválidos. 

Conversión de tipos (Coerción):
Intenta convertir automáticamente los valores de los datos de entrada al tipo de dato del campo del modelo. Por ejemplo, un texto "123" para un campo entero se convertirá a 123. 

Gestión de la configuración:
Facilita la administración de archivos de configuración y variables de entorno, incluyendo la recarga dinámica y la validación de estos datos. 

Serialización de datos:
Permite exportar los modelos de datos a formatos como diccionarios Python o cadenas JSON. 

Integración:
Se integra perfectamente con IDEs, linters y frameworks web como FastAPI, lo que permite generar esquemas JSON y documentación OpenAPI. 

¿Por qué usar Pydantic?
Código más robusto:
Reduce errores al garantizar la calidad de los datos antes de que se procesen en la aplicación. 

Mayor legibilidad:
Las anotaciones de tipo hacen que el código sea más claro y fácil de entender. 

Facilidad de uso:
Permite definir la estructura de los datos de forma declarativa, simplificando el manejo de configuraciones y datos. 

Soporte de editores:
Proporciona autocompletado y sugerencias de tipo, lo que mejora la experiencia de desarrollo. 
