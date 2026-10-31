# Práctica 16

**¿Por qué se usa un contexto y no props para la sesión?**
Porque la sesión la usan varios componentes (el encabezado, Entrar y Registro). Con props habría que pasarla de componente en componente. Con el contexto, cualquiera la lee directo con useSesion().

**¿Qué pasa si un componente usa la sesión fuera del proveedor?**
El contexto vale null porque nadie le da valor, y mi hook useSesion lanza un error que dice que debe usarse dentro de ProveedorSesion.

**¿Dónde se guarda el token y qué riesgo tiene ese lugar?**
Se guarda en el localStorage del navegador. El riesgo es que cualquier script que corra en la página puede leerlo y robarlo, y con el token podría hacer peticiones como si fuera el usuario.
