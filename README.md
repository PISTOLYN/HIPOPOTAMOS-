# Hipopotamos Comiendo Bolitas

Juego arcade para dos jugadores, empaquetado como aplicación de Windows con Electron.

## Instaladores

GitHub Actions crea dos instaladores NSIS:
- **x64:** Windows 10 de 64 bits y Windows 11 de 64 bits.
- **ia32:** Windows de 32 bits. También puede ejecutarse en Windows de 64 bits, aunque se recomienda x64.

Cada vez que se actualice la rama `main`, se ejecuta el flujo **Crear instaladores de Windows**.

## Descargar los instaladores

1. Abre la pestaña **Actions** del repositorio.
2. Entra al último flujo **Crear instaladores de Windows** que terminó correctamente (marca verde).
3. En **Artifacts**, descarga `Hipopotamos-Windows-x64` o `Hipopotamos-Windows-ia32`.
4. Descomprime el ZIP del artefacto y ejecuta el archivo `.exe`.

## Probar localmente

Requiere Node.js 22:
- `npm install`
- `npm start`

Para compilar:
- `npm run build:win64`
- `npm run build:win32`

## Nota de compatibilidad

La compilación de 32 bits utiliza Electron 43. Electron anunció que la serie 43 será la última con binarios Windows de 32 bits; el soporte de esa serie termina en enero de 2027. La compilación x64 también usa Electron 43 para mantener versiones de motor coherentes. Actualizar a Electron 44 o posterior requiere retirar el instalador de 32 bits.
