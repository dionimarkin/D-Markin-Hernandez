# Changelog: planta de emulsión asfáltica

## v000

- Quemador para calentar el asfalto AC-30, en su versión mínima funcional.
- Se enciende por debajo de 130 °C y se apaga al superar 140 °C.

## v001

- Reencendido con un contacto Y004 con autorretención.
- Corrección: se eliminó la memoria M1 para lograr la histéresis real. Ahora solo reenciende al bajar de 130 °C.

## v002

- Las salidas físicas innecesarias se sustituyeron por memorias M.
- Los contactos NO de M0 (START) pasaron a las luces.
- STOP va como contacto NO, porque en físico es NC.
- Se añadió el contacto de STOP en la rama de temperatura.

## v003

- Aumento lento de la temperatura en frío con T0 y T1 (pulsos de quemador encendido y apagado).

## v004

- Emergencia por sobretemperatura (M4) con el termostato X006 (más de 150 °C).
- Luz H3, que se mantiene hasta pulsar RESET (X007).
- Contactos X001, X006 y X003 invertidos para simular (temporal).

## v005

- Memoria M5 para la falla del quemador (X002), con la luz H4 y RESET.

## v006

- Seta X012. Su memoria M6 no tiene RESET: al soltarla el sistema no reinicia, porque M0 queda apagada.
- Relé térmico del quemador X013 (memoria M7, con RESET).
- Manual cableado con el selector X010. X011 solo informa y enciende H6.
- M4 a M7 se unieron en M3 (permiso general: ON = sin emergencia).

## v007

- Bomba que trae el asfalto al depósito (KM2, pulsador CARGA X016, con autorretención).
- Lógica de nivel en el depósito: el nivel mínimo (X014) detiene el sistema y no arranca solo al recuperarse; el nivel máximo (X015) detiene la bomba.
- Protección de la bomba con relé térmico (X017, memoria M9, con RESET). Detiene solo la bomba.
- Luces de nivel mínimo (H9), cargando (H10), falla de la bomba (H11) y nivel máximo (H12).
- Se corrigieron errores en las luces: H10 seguía al pulsador CARGA en lugar de la bomba, y H11 seguía al contacto del relé en lugar de M9. También se corrigió un error en la luz del quemador (verificar la redacción).

## v008
- Se eliminaron las multiples luces de emergencia y se puso una general que parpadea.
- Se agrega una pantalla que lee la memoria que activo emergencia y muestra cual es el fallo.

## v009
- Se cambiaron las memorias de emergencia por memorias retensivas para que si se corta la luz guarden el estado de mergencia

## Convención temporal

- Contactos invertidos para simular: X001, X002, X003, X006, X010, X012, X013, X014, X015 y X017.
- Se revierten al cierre del proyecto.

## Pendientes de cierre

- [ ] Devolver la polaridad física a los contactos invertidos.
- [ ] Cambiar K30 y K60 por K100 y K200.
