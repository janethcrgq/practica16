# Práctica 17

## Ejercicio 1

**¿La ruta protegida hace segura la aplicación? ¿Qué es lo que de verdad protege los datos?**
No, solo esconde la página. Quien protege los datos es el backend, porque revisa el token en cada petición y responde 401 si no es válido.

## Ejercicio 2

**¿Por qué no se manda el miembroId al inscribirse?**
Porque el backend lo saca del token. Si lo mandara el frontend, alguien podría cambiarlo e inscribir a otra persona.

**¿Qué diferencia hay entre un 401 y un 403?**
El 401 es que la API no sabe quién eres (no hay token o es falso). El 403 es que sí sabe quién eres, pero no tienes permiso.