# Google Sheets Argento
Scripts de Apps Script que añaden a tu Google Sheet funciones tipicas para el dia a dia de un Argentino de bien.

## Funciones

### Cotizaciones del dolar
Devuelve la cotización de los distintos tipos de dólar en Argentina.

```
=dolar("tipo"; "operación")
```

### Información de CEDEARs
Devuelve información sobre los CEDEARs (Certificados de Depósito Argentinos) que cotizan en Argentina.

```
=cedear("symbol"; "valor")
```

### Información de Acciones Argentinas
Devuelve información sobre las acciones que cotizan en el mercado argentino.

```
=acciones("symbol"; "valor")
```

### Información de Bonos Argentinos
Devuelve información sobre los bonos que cotizan en el mercado argentino.

```
=bonos("symbol"; "valor")
```

### Índices de Inflación
Devuelve el índice de inflación mensual de Argentina.

```
=inflacion(fecha)
```

### Precios de Criptomonedas
Devuelve el precio actual de criptomonedas desde Coinbase.

```
=crypto("symbol"; "moneda")
```

### Índices UVA
Devuelve el valor del índice UVA (Unidad de Valor Adquisitivo) de Argentina.

```
=uva(fecha)
```

### Riesgo País
Devuelve el valor del riesgo país de Argentina.

```
=riesgopais(fecha)
```

### Comparador de Precios de Criptomonedas (CriptoYa)
Devuelve y compara precios de criptomonedas en diferentes exchanges argentinos e internacionales.

```
=criptoya("coin"; "fiat"; volumen; "exchange"; "operacion")
```

## 📦 Estructura del repositorio
- dolar.js – Código fuente de Apps Script para cotizaciones de dólar
- cedear.js – Código fuente de Apps Script para información de CEDEARs
- acciones.js – Código fuente de Apps Script para información de acciones argentinas
- bonos.js – Código fuente de Apps Script para información de bonos argentinos
- inflacion.js – Código fuente de Apps Script para índices de inflación
- crypto.js – Código fuente de Apps Script para precios de criptomonedas
- uva.js – Código fuente de Apps Script para índices UVA
- riesgopais.js – Código fuente de Apps Script para valores del riesgo país
- criptoya.js – Código fuente de Apps Script para comparador de precios de criptomonedas
- README.md – Esta documentación

## 🔧 Instalación
1. Abrí tu Google Sheet.
2. Andá a Extensiones → Apps Script.
3. Borra cualquier código existente y pega el contenido de dolar.js, cedear.js, acciones.js, bonos.js, inflacion.js, crypto.js, uva.js, riesgopais.js y/o criptoya.js
4. Guarda el proyecto (por ejemplo, "ArgentinaFinance").
5. Volvé a la hoja y espera unos segundos para que se registren las funciones.

## 🚀 Uso

### Función Dólar
En cualquier celda de la hoja, escribe:

```
=dolar("tipo"; "operación")
```

#### Parámetros

**tipo (string):**
- "oficial"
- "blue"
- "bolsa"
- "contadoconliqui"
- "mayorista"
- "cripto"
- "tarjeta"

**operación (string):**
- "compra"
- "venta"
- "promedio"

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=dolar("blue"; "venta")` | Precio de venta del dólar Blue |
| `=dolar("mayorista"; "compra")` | Precio de compra del dólar Mayorista |
| `=dolar("oficial"; "promedio")` | Promedio entre compra y venta oficial |

### Función CEDEAR
En cualquier celda de la hoja, escribe:

```
=cedear("symbol"; "valor")
```

#### Parámetros

**symbol (string):**
- Símbolo del CEDEAR (ej: "AAPL", "MSFT", "GOOGL")

**valor (string):**
- "c" - Precio actual
- "v" - Volumen de operaciones
- "q_bid" - Cantidad en oferta de compra
- "px_bid" - Precio de oferta de compra
- "px_ask" - Precio de oferta de venta
- "q_ask" - Cantidad en oferta de venta
- "q_op" - Operaciones diarias
- "pct_change" - Variación porcentual diaria

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=cedear("AAPL"; "c")` | Precio actual del CEDEAR de Apple |
| `=cedear("MSFT"; "px_ask")` | Precio de oferta de venta del CEDEAR de Microsoft |
| `=cedear("GOOGL"; "pct_change")` | Variación porcentual diaria del CEDEAR de Google |

### Función Acciones
En cualquier celda de la hoja, escribe:

```
=acciones("symbol"; "valor")
```

#### Parámetros

**symbol (string):**
- Símbolo de la acción argentina (ej: "YPFD", "ALUA", "PAMP")

**valor (string):**
- "c" - Precio actual
- "v" - Volumen de operaciones
- "q_bid" - Cantidad en oferta de compra
- "px_bid" - Precio de oferta de compra
- "px_ask" - Precio de oferta de venta
- "q_ask" - Cantidad en oferta de venta
- "q_op" - Operaciones diarias
- "pct_change" - Variación porcentual diaria

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=acciones("YPFD"; "c")` | Precio actual de la acción de YPF |
| `=acciones("ALUA"; "px_ask")` | Precio de oferta de venta de Aluar |
| `=acciones("PAMP"; "pct_change")` | Variación porcentual diaria de Pampa Energía |

### Función Bonos
En cualquier celda de la hoja, escribe:

```
=bonos("symbol"; "valor")
```

#### Parámetros

**symbol (string):**
- Símbolo del bono argentino (ej: "AL30", "GD30", "AE38")

**valor (string):**
- "c" - Precio actual
- "v" - Volumen de operaciones
- "q_bid" - Cantidad en oferta de compra
- "px_bid" - Precio de oferta de compra
- "px_ask" - Precio de oferta de venta
- "q_ask" - Cantidad en oferta de venta
- "q_op" - Operaciones diarias
- "pct_change" - Variación porcentual diaria

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=bonos("AL30"; "c")` | Precio actual del bono AL30 |
| `=bonos("GD30"; "px_ask")` | Precio de oferta de venta del bono GD30 |
| `=bonos("AE38"; "pct_change")` | Variación porcentual diaria del bono AE38 |

### Función Inflación
En cualquier celda de la hoja, escribe:

```
=inflacion(fecha)
```

#### Parámetros

**fecha (string o Date):** [Opcional]
- Fecha para la cual se quiere obtener el índice de inflación
- Formato aceptado: "YYYY-MM-DD" o "MM/DD/YYYY"
- Si se omite, devuelve el valor más reciente disponible

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=inflacion()` | Índice de inflación más reciente |
| `=inflacion("2023-03-31")` | Índice de inflación para marzo de 2023 |
| `=inflacion("03/31/2023")` | Mismo resultado que el anterior |
| `=inflacion(A1)` | Índice de inflación para la fecha en la celda A1 |

### Función Crypto
En cualquier celda de la hoja, escribe:

```
=crypto("symbol"; "moneda")
```

#### Parámetros

**symbol (string):**
- Símbolo de la criptomoneda (ej: "BTC", "ETH", "SOL")

**moneda (string):** [Opcional]
- Moneda en la que se quiere obtener el precio (ej: "USD", "EUR")
- Por defecto: "USD"

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=crypto("BTC")` | Precio actual de Bitcoin en USD |
| `=crypto("ETH"; "EUR")` | Precio actual de Ethereum en euros |
| `=crypto("SOL"; "USD")` | Precio actual de Solana en USD |
| `=crypto("MATIC"; "ARS")` | Precio actual de Polygon en pesos argentinos |

### Función UVA
En cualquier celda de la hoja, escribe:

```
=uva(fecha)
```

#### Parámetros

**fecha (string o Date):** [Opcional]
- Fecha para la cual se quiere obtener el valor del índice UVA
- Formato aceptado: "YYYY-MM-DD" o "MM/DD/YYYY"
- Si se omite, devuelve el valor más reciente disponible

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=uva()` | Valor del UVA más reciente |
| `=uva("2023-03-31")` | Valor del UVA para el 31 de marzo de 2023 |
| `=uva("03/31/2023")` | Mismo resultado que el anterior |
| `=uva(A1)` | Valor del UVA para la fecha en la celda A1 |

### Función Riesgo País
En cualquier celda de la hoja, escribe:

```
=riesgopais(fecha)
```

#### Parámetros

**fecha (string o Date):** [Opcional]
- Fecha para la cual se quiere obtener el valor del riesgo país
- Formato aceptado: "YYYY-MM-DD" o "MM/DD/YYYY"
- Si se omite, devuelve el valor más reciente disponible

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=riesgopais()` | Valor del riesgo país más reciente |
| `=riesgopais("2023-03-31")` | Valor del riesgo país para el 31 de marzo de 2023 |
| `=riesgopais("03/31/2023")` | Mismo resultado que el anterior |
| `=riesgopais(A1)` | Valor del riesgo país para la fecha en la celda A1 |

### Función CriptoYa
En cualquier celda de la hoja, escribe:

```
=criptoya("coin"; "fiat"; volumen; "exchange"; "operacion")
```

#### Parámetros

**coin (string):**
- Criptomoneda a consultar (ej: "BTC", "ETH", "DAI", "USDT")
- [Lista completa](https://criptoya.com/api) incluye: BTC, ETH, USDT, USDC, DAI, UXD, USDP, WLD, BNB, SOL, XRP, ADA, AVAX, DOGE, etc.

**fiat (string):**
- Moneda contra la que se opera (ej: "ARS", "USD", "EUR")
- [Lista completa](https://criptoya.com/api) incluye: ARS, USD, EUR, BRL, CLP, COP, MXN, PEN, VES, etc.

**volumen (number):** [Opcional]
- Volumen a operar (utiliza el punto como separador decimal)
- Por defecto: 1

**exchange (string):** [Opcional]
- Exchange específico a consultar (ej: "binance", "ripio", "letsbit")
- Si se omite, devuelve el mejor precio entre todos los exchanges

**operacion (string):** [Opcional]
- Tipo de operación a consultar:
  - "compra" - Precio de compra sin comisiones (campo "ask")
  - "totalCompra" - Precio de compra con comisiones (campo "totalAsk")
  - "venta" - Precio de venta sin comisiones (campo "bid")
  - "totalVenta" - Precio de venta con comisiones (campo "totalBid")
- Por defecto: "totalCompra"

#### Ejemplos

| Fórmula | Descripción |
|---------|-------------|
| `=criptoya("BTC"; "ARS")` | Mejor precio de compra de Bitcoin en pesos argentinos |
| `=criptoya("ETH"; "USD"; 0.5; "binance"; "venta")` | Precio de venta de 0.5 ETH en USD en Binance |
| `=criptoya("DAI"; "ARS"; 100; ; "totalVenta")` | Mejor precio de venta (con comisiones) de 100 DAI en pesos |
| `=criptoya("USDT"; "ARS"; 1000; "ripio")` | Precio de compra de 1000 USDT en pesos en Ripio |

## 🔄 Actualización automática
Google Sheets recalcula las fórmulas al:

- Abrir la hoja
- Editar cualquier celda

Forzar recálculo:
- Ctrl + R (Windows) o ⌘ + R (Mac)
- Archivo → Configuración de hoja de cálculo → Cálculo → "Al cambiar" o "Cada minuto"

## ⚠️ Errores comunes

### Errores de la función Dólar

**Tipo inválido**  
"Tipo inválido: 'xyz'. Tipos disponibles: oficial, blue, bolsa, contadoconliqui, mayorista, cripto, tarjeta."

**Operación inválida**  
"Operación inválida: 'xyz'. Usa 'compra', 'venta' o 'promedio'."

### Errores de la función CEDEAR

**Símbolo inválido**  
"Símbolo inválido: 'xyz'. No se encontró en la lista de CEDEARs disponibles."

**Atributo inválido**  
"Atributo inválido: 'xyz'. Atributos disponibles: c, v, q_bid, px_bid, px_ask, q_ask, q_op, pct_change."

### Errores de la función Acciones

**Símbolo inválido**  
"Símbolo inválido: 'xyz'. No se encontró en la lista de acciones disponibles."

**Atributo inválido**  
"Atributo inválido: 'xyz'. Atributos disponibles: c, v, q_bid, px_bid, px_ask, q_ask, q_op, pct_change."

### Errores de la función Bonos

**Símbolo inválido**  
"Símbolo inválido: 'xyz'. No se encontró en la lista de bonos disponibles."

**Atributo inválido**  
"Atributo inválido: 'xyz'. Atributos disponibles: c, v, q_bid, px_bid, px_ask, q_ask, q_op, pct_change."

### Errores de la función Inflación

**Fecha inválida**  
"Fecha inválida: 'xyz'. Usar formato 'YYYY-MM-DD' o 'MM/DD/YYYY'."

### Errores de la función Crypto

**Par de trading no encontrado**  
"Par de trading no encontrado: 'XYZ-USD'. Verifica que el símbolo y la moneda sean correctos."

**Error de conexión**  
"Error al consultar el precio de XYZ: [mensaje de error detallado]"

### Errores de la función UVA

**Fecha inválida**  
"Fecha inválida: 'xyz'. Usar formato 'YYYY-MM-DD' o 'MM/DD/YYYY'."

### Errores de la función Riesgo País

**Fecha inválida**  
"Fecha inválida: 'xyz'. Usar formato 'YYYY-MM-DD' o 'MM/DD/YYYY'."

### Errores de la función CriptoYa

**Par de trading no encontrado**  
"Par BTC/XYZ no encontrado. Verifica que la cripto y la moneda sean correctas."

**Exchange no disponible**  
"Exchange 'xyz' no disponible. Exchanges disponibles: binance, ripio, letsbit, ..."

**Operación inválida**  
"Operación inválida: 'xyz'. Operaciones disponibles: compra, totalCompra, venta, totalVenta."

## 👏 Agradecimientos

- A [Argentina Datos](https://argentinadatos.com/) y su creador [Enzo Notario](https://github.com/enzonotario/) por las APIs de inflación y UVA.
- A [@JohnGalt_is_www](https://x.com/JohnGalt_is_www) por sus APIs de bonos, CEDEARs y acciones.
- A [@http://criptoya.com/](http://criptoya.com/) por su API de comparación de precios de criptomonedas.





