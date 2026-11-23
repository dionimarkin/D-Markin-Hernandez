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

- Bomba de carga KM2 con X016 y autorretención.
- Nivel mínimo X014 y nivel máximo X015.
- Relé térmico X017 con M9, que detiene solo la bomba.
- Luces H9 a H12.
- Se corrigieron errores en H10, H11 y la luz del quemador.

## Convención temporal

- Contactos invertidos para simular: X001, X002, X003, X006, X010, X012, X013, X014, X015 y X017.
- Se revierten al cierre del proyecto.

## Pendientes de cierre

- [ ] Devolver la polaridad física a los contactos invertidos.
- [ ] Cambiar K30 y K60 por K100 y K200.
- [ ] Repetir la tabla completa de todas las versiones.