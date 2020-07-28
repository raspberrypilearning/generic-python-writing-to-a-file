- Escribir datos a un archivo con Python es muy fácil. Primero, necesitas algunos datos para escribir. Aquí se almacena como una variable llamada `texto`.

    ```python
    texto = 'Este es un dato a escribir'
    ```

- La siguiente etapa es abrir un archivo. Necesitas pasar el nombre del archivo a la función `open`. La función también necesita saber con qué **modo** abrir el archivo. Aquí el modo es `w`, que es la abreviatura de "write" (escribir en inglés).

    ```python
    archivo = open('mi_documento.txt', 'w', encoding="utf-8")
    ```
- A continuación, los datos se pueden escribir en el archivo.

    ```python
  archivo.write(texto)
  ```

- Por último, el archivo debe cerrarse.

  ```python
  archivo.close()
  ```

- Otra forma de hacer esto, es automáticamente **cerrar** el archivo usando la palabra clave `with`. Esto es a menudo preferible, ya que es fácil olvidarse **cerrar** el archivo.

  ```python
  texto = 'Este es un dato a escribir'
  with open('mi_documento.txt', 'w', encoding="utf-8") as archivo:
      archivo.write(texto)
  ```
