1. AUTENTICACIÓN DE USUARIOS
----------------------------

La autenticación es el proceso mediante el cual los usuarios se identifican en la aplicación. Para esto, se utilizan credenciales como correo electrónico y contraseña.

Pasos básicos para implementar autenticación:

a) Registro de Usuario (Sign Up):
   - El usuario proporciona su nombre, correo electrónico y contraseña.
   - La contraseña se encripta (por ejemplo, usando bcrypt) antes de guardarse en la base de datos.
   - Se verifica si el correo electrónico ya está en uso.

b) Inicio de Sesión (Login):
   - El usuario introduce su correo electrónico y contraseña.
   - Se busca el correo en la base de datos y se compara la contraseña ingresada con la almacenada (usando la función de verificación del algoritmo de encriptación).
   - Si son válidos, se genera un token de sesión (por ejemplo, JWT) o se establece una sesión en el servidor.

c) Cierre de Sesión (Logout):
   - Si se usa JWT, el token se elimina del cliente.
   - Si se usa sesión en el servidor, esta se destruye.

d) Seguridad:
   - Usar HTTPS para proteger los datos en tránsito.
   - Limitar intentos de inicio de sesión para evitar ataques de fuerza bruta.
   - Almacenar las contraseñas siempre encriptadas.
