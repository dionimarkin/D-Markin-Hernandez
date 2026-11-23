# Changelog - Planta de emulsión

## v000
- Quemador para calentar AC30, versión mínima funcional
- El quemador se enciende si la temperatura esta por debajo de los 130 grados y se apaga al subir de 140

## v001
- El quemador se vuelve a encender cuando baje de 140 mientras no se presione STOP.Para lograr esto se agrego un contacto Y4 con autoretencion 

## v002
- Salidas físicas innecesarias cambiadas por memorias M. 
- Contactos NO de M0 (START) en luces. 
- STOP como NO por ser NC en físico.
- Contacto añadido en rama de temperatura.

## v003
- Aumento lento de temperatura con t0 y t1.

## v004 
- Estado de emergencia por sobretemperatura con un contacto de termometro (temperatura sobre los 150 grados)
-
- Invirtio los contactos x001 (STOP), x006 (>150), x003 (<130) para facilitar la simulacion 

## v005
- Se agrego una memoria diferente M5 para un estado de emergencia por fallo del quemador y la luz H4 que lo indica

## v006
- Se agrego un boton seta como paro de emergencia.
- Se le agrego un rele termico al contactor del quemador
- Se implemento un cambio para modo manual con el contancto X010.
- El quemador se enciende manual con X011.
- Se unieron M4,M5,M6 y M7 en una linea M3, asi se juntan todas las emergencias y facilita los cambios y lectura del codigo.