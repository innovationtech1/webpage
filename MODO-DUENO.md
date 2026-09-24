# Modo dueño del generador

El generador cobra $39 USD por descargar la página. Tú, como dueño, puedes descargar gratis activando el **modo dueño**.

## Cómo activarlo

1. Abre esta dirección, cambiando `TU-CLAVE` por tu clave secreta:

   `https://innovationtech1.github.io/webpage/generador.html#dueno=TU-CLAVE`

2. Verás el aviso **"Modo dueño activado 🔓"** y la clave desaparece sola de la barra de direcciones.
3. Ese navegador queda recordado: la próxima vez entra normal a `generador.html` y seguirá desbloqueado.

Tienes que hacerlo una vez en cada navegador o dispositivo (computadora, celular, etc.).

## Cómo desactivarlo

Abre `generador.html#salir`. Útil si usaste una computadora prestada.

## Cómo cambiar la clave

La clave **no** está escrita en el código; solo está su "huella" (SHA-256) en la variable `OWNER_HASH` de `generador.html`.

1. Abre `generador.html` en tu navegador.
2. Presiona `F12` (o clic derecho → Inspeccionar) y ve a la pestaña **Console**.
3. Pega esto, cambiando `mi-clave-nueva`, y presiona Enter:

   ```js
   crypto.subtle.digest("SHA-256", new TextEncoder().encode("mi-clave-nueva")).then(b => console.log([...new Uint8Array(b)].map(x => x.toString(16).padStart(2,"0")).join("")))
   ```

4. Copia el texto largo que aparece y ponlo en `OWNER_HASH` dentro de `generador.html`.

Usa una clave larga (3 palabras y un número, por ejemplo). Nunca la escribas en el repositorio.

## Límite importante

Esto es una protección en el navegador: evita el truco fácil de `?owner=1`, pero alguien con conocimientos técnicos siempre puede modificar el código de una página estática. Lo mismo pasa con `?pago=ok`, que desbloquea sin verificar el pago con Stripe. La protección real requiere un pequeño servidor que confirme el pago con Stripe antes de entregar el archivo.
