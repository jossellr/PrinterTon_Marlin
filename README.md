# PrinterTon Marlin

Este proyecto recoge el código Marlin personalizado para mi Ender 3 pro modificada. La versión de Marlin es la 2.0.4, y los cambios en la Ender original
son los siguientes:

 1. **Placa**: MKS Gen L v2.0.
 2. **Drivers**: TMC2208 v2.0 (modo UART) para los motores de los ejes X, Y, Z y extrusor.
 3. **Ventiladores**: noctua de 12V para el hotend y dos ventiladores de 24V para la electrónica. 
 4. **Extrusor**: el extrusor que utilizo es el BMG clonado de Trianglelab.

Puntos a tener en cuenta de cara a actualizar el firmware de la electrónica a través del IDE de Arduino: 

 1. **Placa**: Arduino/Genuino Mega or Mega 2560.
 2. **Procesador**: ATmega 256.
 3. **Biblioteca necesaria para la LCD**: U8glib.
 4. **Biblioteca necesaria para configurar los drivers mediante Marlin (UART mode)**: TMCSteppers.
 5. **Error avr-gcc o avr-g++**: en Windows es posible que surjan problemas al compilar el proyecto. Si este error te sucede, elimina 
 todas las carpetas alojadas en el directorio PrinterTon_Marlin\src\HAL, a excepción de las carpetas HAL_AVR y shared.

Configuración de Marlin de ejemplo para la Ender 3 con las siguientes modificaciones:

 1. **Drivers**: TMC2208.
 2. **Placa**:  BOARD_MKS_GEN_L_V2.
 3. **Cambio de filamento**: ADVANCED_PAUSE_FEATURE (también requiere habilitar PARK_HEAD_ON_PAUSE y NOZZLE_PARK_FEATURE).
 4. **Cambio de filamento por LCD**: FILAMENT_LOAD_UNLOAD_GCODES (requiere el anterior punto).
 5. **Activación del ventilador automático del extrusor a partir de 50 grados**: 7 (E0_AUTO_FAN_PIN).
 6. **Pasos de los motores**: {80, 80, 400, 415}.

Configuración de Marlin para el modo UART de los drivers:
 1. **Driver's para los motores X, Y y Z**: corriente de 700 mA y 16 micropasos.
 2. **Driver del extrusor**: corriente de 300 mA y 16 micropasos.

# Perfiles de cura

En la carpeta [cura profiles](cura%20profiles) iré dejando perfiles de CURA. Por ahora los perfiles que hay son:
 1. **PLA**: enlace del archivo [aquí](cura%20profiles/PLA_profile.curaprofile).
