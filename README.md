# Ejercicio2_Adicional

---

1) En BDCelular:Inserta un nuevo celular en la base de datos.  
Establece una conexión, prepara una consulta `INSERT`, asigna los valores desde el objeto `Celular` y ejecuta la inserción. Finalmente, cierra la conexión y el statement.

![image](https://github.com/user-attachments/assets/87489fa9-dd0c-492b-bfc9-2ae6d5fd2ea7)

2) Obtiene un celular por su ID desde la base de datos.  
Realiza una consulta `SELECT` con el `idCel` indicado, y si encuentra un resultado, crea y retorna un objeto `Celular` con los datos obtenidos. Si no encuentra, retorna `null`.

![image](https://github.com/user-attachments/assets/416e6f0f-0121-4595-978e-b66de637a216)


3)Actualiza los valores de saldo y megas de un celular en la base de datos.  
Utiliza una sentencia `UPDATE` con el ID del celular para establecer los nuevos valores de saldo y megas.


![image](https://github.com/user-attachments/assets/6037e107-408e-4926-b870-336ada1a1cde)

---

4) En BDCliente: Inserta un nuevo cliente en la base de datos.  
Abre una conexión, prepara una sentencia `INSERT` con los datos del cliente (cédula, nombres y apellidos), la ejecuta y luego cierra los recursos.

![image](https://github.com/user-attachments/assets/59d12b0c-8a69-4f42-b22b-b358349e37cf)

---

5) En BDRecarga: Realiza una recarga manual a un celular bloqueado.  
Suma el saldo y megas ingresados manualmente al celular, convirtiendo los megas a GB (5 GB por dólar). Luego registra la recarga y actualiza el celular en la base de datos.

![image](https://github.com/user-attachments/assets/95f8913b-e578-4506-a357-99cf3e2a9d60)


6) Realiza una recarga automática a un celular activo.  
Distribuye el valor ingresado asignando 2/3 al saldo y 1/3 a megas (convertido a GB a razón de 5 GB por dólar). Luego registra la recarga y actualiza el celular en la base de datos.


![image](https://github.com/user-attachments/assets/8d17f68e-6702-4606-8607-37ac1e6ffdd0)


7) Registra una nueva recarga en la base de datos.  
Inserta un registro en la tabla `Recargas` con el valor total, la parte destinada a saldo, la parte destinada a megas y el ID del celular asociado.

![image](https://github.com/user-attachments/assets/4f9efd0f-edca-4752-96a7-4eec5e84e8de)


---

8) En LogSistema: Gestiona las operaciones principales del sistema.

- `guardarCliente(...)`: Crea un objeto `Cliente` con los datos ingresados y lo guarda en la base de datos.
- `guardarCelular(...)`: Registra un nuevo celular asociado a un cliente, iniciando con saldo y megas en 0.
- `realizarRecarga(...)`: Verifica el estado del celular para aplicar la recarga:
  - Si el celular está **activo** (`estado = 1`), realiza una recarga automática dividiendo 2/3 a saldo y 1/3 a megas (convertido a GB).
  - Si está **bloqueado** (`estado = 0`), requiere que el usuario indique manualmente cuánto se asigna a saldo y a megas, validando que la suma coincida con el valor total.


![image](https://github.com/user-attachments/assets/7013a646-e263-4fae-93b6-9bb427dbf499)

---

9) Diseño de la ventana

![image](https://github.com/user-attachments/assets/d335578e-0103-4454-96a6-8c37b09d1325)

---

10) Guarda un cliente
  
![image](https://github.com/user-attachments/assets/a7586e64-a01d-4908-8de8-093b9207ee73)


11) Registra el celular en donde estado= 0 SI ESTA BLOQUEADO y 1 si no tiene problemas

![image](https://github.com/user-attachments/assets/5d61adbe-c0a7-4138-980f-d5207b66a28c)

12) Si no esta Bloqueado dejara realizar la recarga solo ingresando el valor
 ![image](https://github.com/user-attachments/assets/fedd4623-2795-4eb9-bd33-1af6f6f1bbed)

13) En la base de datos constara como se dividio este valor entre saldo y megas

![image](https://github.com/user-attachments/assets/53b39688-ab82-43ae-ab8c-5e75616ba1db)


14) En caso se quiera hacer una recarga con un celular BLOQUEADO = 0 este obligara a ingresar la recarga manualmente

    ![image](https://github.com/user-attachments/assets/499354ca-2f74-460f-b01f-24a8bbe5edb1)

    ![image](https://github.com/user-attachments/assets/55507b8d-51c6-4508-92bc-e6ba8215505b)

![image](https://github.com/user-attachments/assets/d679935b-8c14-4d6f-ac43-9a84e813c5e5)

---
15) Esquema SQL

![image](https://github.com/user-attachments/assets/cf48c712-cdba-4218-873d-e71a7f433ab0)

