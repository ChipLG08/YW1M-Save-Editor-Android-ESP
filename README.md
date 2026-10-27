# YW1S Save Editor Android (ESP)

Una aplicación de Android que carga el archivo `main.bin` de Yo-kai Watch 1 Smartphones mediante Shizuku, permitiendo editar y guardar los datos de `game0.yw` a `game3.yw`.

## Funcionalidades implementadas

- Portada a Kotlin de la lógica de cifrado y descifrado de `crypt.py` / `check.py`.
- Selección de `game0.yw`, `game1.yw`, `game2.yw` o `game3.yw` dentro de `main.bin` para extraer la lista de Yo-kai.
- Edición de estadísticas individuales y otros atributos mediante una interfaz de Compose.
- Visualización de la lista de objetos y modificación de las cantidades existentes dentro de límites seguros.
- Visualización en modo de solo lectura del Equipamiento, los Objetos Clave, el estado de la Expendekai y la Mansión del Viajero.
- Creación automática de una copia de seguridad llamada `main.bin.bak` al guardar. El archivo temporal se valida antes de sustituir el original.

## Archivo de destino (Cambiado respecto al repo original)

- `/data/user/<ID_del_usuario_actual>/Android/media/jp.co.level5.yws1/save/main.bin`

Si no posees esta carpeta deberás crearla tú y meter dentro tu `main.bin`.

## Uso

1. Inicia Shizuku tras haberlo configurado previamente.
2. Abre la aplicación y concede los permisos de Shizuku cuando aparezca el diálogo correspondiente.
3. Selecciona la partida que quieras editar, desde `game0` hasta `game3`.
4. Edita los Yo-kai o los datos de la partida.
5. Pulsa `Guardar` para aplicar los cambios a la partida seleccionada.
6. En caso de que no hayas cambiado la ruta de la partida guardada de `/Android/data/jp.co.level5.yws1/files/save/main.bin` a `/Android/media/jp.co.level5.yws1/save/main.bin`, pega el `main.bin` resultante en `/Android/data/jp.co.level5.yws1/files/save/` para aplicar los cambios.

## Advertencias

- Shizuku en modo ADB (sin root) no puede acceder a los datos internos de otras aplicaciones, por lo que no es posible editar las partidas en este modo. Es por eso que se cambio la ruta respecto al repositorio original para que sea más fácil para usuarios sin root.
- Antes de escribir los cambios, se crea automáticamente una copia de seguridad (`.bak`), pero utiliza la aplicación bajo tu propia responsabilidad.

## Licencia

- El código de este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para obtener más información.
- Para consultar la información sobre las licencias de los materiales de terceros incluidos en el proyecto, consulta `THIRD_PARTY_NOTICES.md`.
