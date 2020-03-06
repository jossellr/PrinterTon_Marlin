# PrinterTon Marlin

Este proyecto recoge mi código de Marlin personalizado. La versión de Marlin es la 2.0.4.

Puntos a tener en cuenta de cara a actualizar la electrónica:

 1. **Placa**: Arduino/Genuino Mega or Mega 2560.
 2. **Procesador**: ATmega 256.
 3. **Biblioteca necesaria para la LCD**: U8glib.

Configuración de Marlin de ejemplo para la Ender 3 con las siguientes modificaciones:

 1. **Drivers**: TMC2208_STANDALONE.
 2. **Placa**:  BOARD_MKS_GEN_L_V2.
 3. **Cambio de filamento**: ADVANCED_PAUSE_FEATURE (También requiere habilitar PARK_HEAD_ON_PAUSE y NOZZLE_PARK_FEATURE).
 4. **Cambio de filamento por LCD**: FILAMENT_LOAD_UNLOAD_GCODES (requiere el anterior punto).
 5. **Activación del ventilador automático del extrusor**: 7 (E0_AUTO_FAN_PIN).