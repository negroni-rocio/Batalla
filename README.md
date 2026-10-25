# Batalla Naval 4×4 online

Juego web multijugador por equipos, con 3 barcos, turnos, impactos/agua, un capitán por equipo y flotas privadas.

## Importante
- El servidor es quien conserva las flotas y valida turnos/disparos. El navegador solo recibe la flota de su propio equipo; la flota rival nunca se emite a sus sockets.
- Un solo capitán por equipo puede ubicar barcos y disparar. Los observadores solo reciben el estado de juego.
- Esta versión guarda las partidas en memoria: si el servidor se reinicia o duerme, se pierde la partida. Es adecuada para una partida de clase; no es una base de datos permanente.
- El código de acceso de capitán es secreto. Compartí el código `...BCAP` solo con el capitán B y el código de capitán A queda en el navegador de quien crea la partida. Los códigos `...AVIEW` y `...BVIEW` son solo de lectura.

## Probar en tu computadora
Necesitás Node.js 18 o posterior.

```bash
npm install
npm start
```

Abrí `http://localhost:3000`.

## Publicarlo gratis en Render
1. Subí esta carpeta a un repositorio de GitHub.
2. En Render, creá un **New Web Service** y conectá ese repositorio.
3. Elegí `Node` como entorno, `npm install` como Build Command y `npm start` como Start Command.
4. Cuando termine el despliegue, Render te dará una URL pública `https://...onrender.com`. Compartí esa URL con tus compañeros.
5. Creá la partida desde esa URL y enviá a cada persona el código de su equipo.

Render puede poner servicios gratuitos en reposo cuando no se usan; la primera conexión puede tardar. Reiniciar el servidor borra las partidas activas.
