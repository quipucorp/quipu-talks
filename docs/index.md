---
marp: true
# import: style.css
theme: gaia
math: mathjax
_class: 
  - lead
  #- invert
paginate: true
backgroundColor: #fff
# backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!--
<link rel="icon" href="https://quipubank.com/wp-content/uploads/2022/10/logo-back.svg" sizes="32x32" />
<link rel="icon" href="https://quipubank.com/wp-content/uploads/2022/10/logo-back.svg" sizes="192x192" />
-->

<style>
@import url(https://fonts.googleapis.com/css?family=Google+Sans);
/*@import url(https://fonts.googleapis.com/css?family=Poppins);*/

:root {
    font-family: "Google Sans";
    /*font-family: "Poppins";*/
    --color-background: #ddd;
    --color-background-code: #ccc;
    --color-background-paginate: rgba(
        128, 128, 128, 0.05
    );
    --color-foreground: #345;
    --color-highlight: #99c;
    --color-highlight-hover: #aaf;
    --color-highlight-heading: #99c;
    --color-header: #bbb;
    --color-header-shadow: transparent;
    img[alt~="center"] {
        display: block;
        margin: 0 auto;
    }
}
section::after {
content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);
}
</style>

# Blockchain, Web3 y DeFi

<!--
![img](./imgs/bc-information.mp4)
![img](./imgs/bc-concensus.gif)
![img](./imgs/bc-validators.mp4)
![img](./imgs/Blockchain.gif)
-->

# QuipuBank

---
# Blockchain, Web3 y DeFi

- **Blockchain:** Conceptos, historia y Smart Contracts.
- **Web 3:** Blockchain + Web2, Interactuar con la Blockchain.
- **Finanzas Decentralizadas:** DeFi, AMM y Lending Pools, Quipu.

---
# Blockchain
- Conceptos Fundamentales y Técnicos
- Historia: de Bitcoin a Ethereum.
- Solidty/EVM Smart Contracts.

---
## Blockchain / Conceptos Fundamentales
- **Registro público distribuido y decentralizado**
- **Anónimo:** La participación en cada transacción es referenciada a **números de cuenta**.
- **Consultar es gratis.**
- **Se paga por escribir:** Esfuerzo computacional = _gas transaction_
- **Inmutable:** Habilita la trazabilidad de las transacciones.

---
### Blockchain / Conceptos técnicos / Hash
  Función criptográfica para codificar datos en una cadena de caracteres única.
  Ejemplo un hash de bloque: `0xb5a4bbd24022b35daf9c239755c69d8728abffaf90e859ef4fcb6846b34ceb58`.
  Asegurar autenticidad de datos, contraseñas, firmar documentos electrónicos.

---
### Blockchain / Conceptos técnicos / Bloque
Información agrupada en conjuntos, a los que se les añade
metadata relativa a otro bloque anterior en la cadena,
para hacer un seguimiento seguro a través de cálculos criptográficos.

---
### Blockchain / Conceptos Técnicos / Cadena de bloques
<style scoped>
img {
  margin:auto;
  text-align: center;
}
p {
  margin:auto;
  text-align: center;
}
</style>
![w:950 info](./imgs/blockchain.gif)

---
### Blockchain / Conceptos técnicos / Cadena de bloques decentralizada
Blockchain es un tipo de **libro de contabilidad decentralizado**.
Utiliza ordenadores independientes (**nodos**) para **registrar, compartir y sincronizar transacciones** en sus respectivos
libros digitales; **en lugar de mantener los datos centralizados**
como en un libro de finanzas tradicional.
Ejerce de **base de datos pública no relacional de un histórico irrefutable** de información.

---
<style scoped>
img {
  margin:auto;
  text-align: center;
}
p {
  margin:auto;
  text-align: center;
}
</style>
### Blockchain / Conceptos técnicos / Blockchain
![w:900 info](./imgs/bc-information.gif)


<!--
---
### Concenso 
![w:950 info](./imgs/bc-concensus.gif)
-->

---
<style scoped>
img {
  margin:auto;
  text-align: center;
}
p {
  margin:auto;
  text-align: center;
}
</style>
![blur:.5px opacity:.9 saturate:1.5 sepia:.9 w:930 contrast:120% history](./imgs/bc-history2.jpg)

---
<style scoped>
p{
  font-size: 28px;
}
</style>
![bg right:40% w:500](imgs/smart-contract.jpeg)
# Smart Contracts
Los contratos inteligentes son **programas informáticos que se alojan y ejecutan en la Blockchain**.
Consiste en código que especifica **condiciones** predeterminadas que, cuando se cumplen, **desencadenan resultados**.
Al ejecutarse en una cadena de bloques descentralizada, permiten que varias partes lleguen a un **resultado compartido de forma precisa, oportuna y a prueba de manipulaciones**. 

---
![bg left:66% w:1000](./imgs/helloWorld-sc.png)

# Hola Mundo! 
Ejemplo de un Smart Contract en Solidy, lenguaje de la  Máquina Virtual Ethereum (EVM), que actualiza una cadena de texto.

---
![bg left:50% w:1350](./imgs/web3.png)
# Web3
 - Blockchain + Web2
   - _on/off-chain data_
 - Interactuar con la Blockchain
   - Wallets
   - Emitir y escuchar eventos

---
![bg opacity:0.3 w:1350](./imgs/web3b.png)
## Web3 / Blockchain + Web2 = Web3
- Término creado por el cofundador de Ethereum, Gavin Wood, en su artículo _Insights Into a Modern world_.
- Leer y generar información en la Blockchain desde el navegador, a través de interfaces HTML o aplicaciones.
  **On-chain data:** Información que recide o es producida dentro de la Blockchain.
- Smart Contracts que consultan información del mundo real. Por Ej. condiciones climáticas, precios de bienes, APIs, etc.
  **Off-chain data:** Información fuera de la Blockchain.


---
![bg right:40% w:1350](./imgs/wallet.jpg)
## Web3 / Interactuar / Wallets de criptomonedas

- Son piezas clave para interactuar con la Blockchain.
- Experiencias tempranas de dApp (interfaces Web3).
- Como herramienta _add-on_ de navegador, la mas usada es _Metamask_ pero hay muchas otras.

---
## Web3 / Eventos  / Emitir 

```
// Declare an Event
event Deposit(address indexed _from, bytes32 indexed _id, uint _value);

// Emit an event
emit Deposit(msg.sender, _id, msg.value);
```
Método especial de los Smart Contract que exponen información a partir de determinadas condiciones cumplidas.


---
<style scoped>
h1,h2,h3, p{
color: #FFF;
}

</style>

![bg brightness:0.4](./imgs/tg.jpg)
## Web3 / Eventos  / Escuchar

Grupo de herramientas,
librerías, SDKs y servicios 
que pueden subscribirse
a un Smart Contract 
y registran eventos
emitidos por los mismos.


---

![bg left:50%](./imgs/defi.jpg)
# DeFi: Finanzas Decentralizadas

Principales arquetipos:
- Creadores Automáticos de Mercado (AMM / Liquidty Pools).
- Pools de Préstamos (Lending Pools) 

<!--
---
## DeFi / Tokens 
-->

---
![bg right:60% w:1050](./imgs/amm.png)
**DeFi / Automated Market Makers (AMM)**
Los AMM permiten a intercambiar unidades de diferentes tipos de criptoactivos, sin necesidad de encontrar una contraparte.

---
![bg left:50% w:1200](./imgs/lp.png)
**DeFi / Lending Pools**
Los pools de préstamos son apps descentralizadas que permiten a usuarios que no son de confianza mutua prestar y tomar prestados criptoactivos.



---
![bg w:1350](./imgs/quipulp.png)
### Quipu / Lending Pool
<!--
Acceder a lineas de credito sin establecer un elemento de valor como garantía es que el puede confiscar
al prestatario si éste no devuelve el préstamo según las condiciones acordadas.

Un ejemplo común es cuando se contrata una hipoteca.
Normalmente, el banco le
pedirá que aporte su casa como garantía. 
-->

---
![bg right:50%](./imgs/quipu1.svg)
## Quipu / Lending Pool / Protocolo de Smart Contracs 
Créditos que proviene de cualquier persona del mundo, en forma de criptomonedas, creando un nuevo fondo de liquidez en la que usuarios pueden extraer
de forma rápida y a tipos de interés asequibles.

<!---
1. Quipu planea que los
microcréditos provengan de cualquier persona del mundo,
creando un nuevo fondo de liquidez del que se puede extraer.
de forma rápida y a tipos de interés asequibles;

Y aquí es donde entran los tokens.
Los prestamistas compran un token, que está vinculado al peso colombiano para que los microempresarios
puedan obtener dinero real de forma rápida y a tipos de interés asequibles;
y a cambio los inversores reciben un token que genera intereses y
que aumenta su valor a medida que se devuelven los préstamos. 

2. Los préstamos se asignan desde el fondo común a los usuarios de Quipu incluidos en la lista blanca,
basándose en la puntuación crediticia de Quipu.
Quipu construye una puntuación crediticia de IA utilizando información del comportamiento digital de los usuarios en la app,
ventas, puntuación de los clientes, sociodemográfica, etc.

3. Los microempresarios son recompensados con tokens cuando devuelven sus préstamos a tiempo, traen más prestatarios a la comunida
 tienen un catálogo actualizado, etc. Con esos tokens
pueden comprar productos a otros comerciantes de la plataforma, devolver sus préstamos,
ahorrar o incluso realizar inversiones en otros emprendedores de la plataforma Quipu. 
l objetivo final es que estos poseedores de tokens se conviertan en
una herramienta de gobernanza descentralizada en el futuro.
Los emprendedores de Quipu que posean tokens de gobernanza ganarán poder de decisión sobre el protocolo de préstamos.

4. Los prestatarios recibirán su dinero en una tarjeta de prepago que podrán utilizar
para gastar en determinados negocios, mientras reciben tokens quipu como devolución de dinero.
No necesitarán cambiar cripto por moneda fiduciaria.
-->

---
<style scoped>
code {
  background: transparent;
  color: #000;
  font-weight: bold;
  min-width: 80%;
}
</style>

# ¡Muchas Gracias!

```
                        ________  ___  ___  ___  ________  ___  ___     
                       |\   __  \|\  \|\  \|\  \|\   __  \|\  \|\  \    
                       \ \  \|\  \ \  \\\  \ \  \ \  \|\  \ \  \\\  \   
                        \ \  \\\  \ \  \\\  \ \  \ \   ____\ \  \\\  \  
                         \ \  \\\  \ \  \\\  \ \  \ \  \___|\ \  \\\  \ 
                          \ \_____  \ \_______\ \__\ \__\    \ \_______\
                           \|___| \__\|_______|\|__|\|__|     \|_______|
                                 \|__|                                  
                        ________  ________  ________   ___  __       
                       |\   __  \|\   __  \|\   ___  \|\  \|\  \     
                       \ \  \|\ /\ \  \|\  \ \  \\ \  \ \  \/  /|_   
                        \ \   __  \ \   __  \ \  \\ \  \ \   ___  \  
                         \ \  \|\  \ \  \ \  \ \  \\ \  \ \  \\ \  \ 
                          \ \_______\ \__\ \__\ \__\\ \__\ \__\\ \__\
                           \|_______|\|__|\|__|\|__| \|__|\|__| \|__|
```
## ¿Preguntas?

---
# Referencias

http://Blockchain.mit.edu/how-Blockchain-works
https://www.cbsnews.com/news/web3-cryptocurrency-nft-tim-oreilly/
https://es.wikipedia.org/wiki/Cadena_de_bloques
https://chain.link/education/smart-contracts
https://www.coinbureau.com/review/the-graph-grt/
https://clarusway.com/what-is-a-web3-wallet
https://medium.com/coinmonks/the-current-state-of-undercollateralized-defi-lending-2021-1f84e14527b5


<!---
---
<style scoped>
code {
  font-size: 22px;
}
</style>

```solidty
/* Specifies the version of Solidity, using semantic versioning.
pragma solidity ^0.7.0;

/* Defines a contract named `HelloWorld`.
 * A contract is a collection of functions and data (its state).
 * Once deployed, a contract resides at a specific address on the Ethereum Blockchain.
 * Learn more: https://solidity.readthedocs.io/en/v0.5.10/structure-of-a-contract.html */
contract HelloWorld {

  /* Declares a state variable `message` of type `string`.
   * State variables are variables whose values are permanently stored in
   * contract storage. The keyword `public` makes variables accessible from
   * outside a contract and creates a function that other contracts or
   * clients can call to access the value. */
   string public message;

  /* Similar to many class-based object-oriented languages, a constructor
   * is a special function that is only executed upon contract creation. 
   * Constructors are used to initialize the contract's data. */
   constructor(string memory initMessage) {

      /* Accepts a string argument `initMessage` and sets the value into the
       * contract's `message` storage variable). */
      message = initMessage;
   }

   /* A public function that accepts a string argument and updates the `message` storage variable. */
   function update(string memory newMessage) public {
      message = newMessage;
   }
}
```
-*--

Los pools de préstamos son aplicaciones descentralizadas que permiten a usuarios que no son de confianza mutua prestar y tomar prestados criptoactivos.
En [7], formalizamos todas las interacciones entre los usuarios y las LPs, proporcionando así una especificación completa de la funcionalidad económica de las LPs.
Nuestro modelo permite formalizar y especificar las propiedades fundamentales de las LPs,
como por ejemplo la contabilidad correcta de los tokens acuñados y la preservación del suministro de tokens depositados,
que son cruciales para asegurar la consistencia en el intercambio y distribución de tokens habilitados por las LPs.
Además, nuestro modelo permite razonar sobre los agentes racionales, que están incentivados a liquidar los préstamos
a cambio de una garantía con descuento o a realizar depósitos inmediatamente antes del devengo de intereses.
También proporcionamos argumentos sólidos para el diseño de los incentivos de las LPs, por ejemplo demostrando formalmente que los depositantes pueden potencialmente canjear más fichas de las que depositaron, e identificando las condiciones bajo las cuales los canjes no son posibles. En este sentido, formalizamos las nociones de seguridad de utilización, que representa un compromiso de utilidad entre las acciones de préstamo y reembolso, moderado por un tipo de interés dinámico. En las LPs, los préstamos están asegurados por una garantía: sin embargo, existen estados de la LP en los que el prestatario ya no está incentivado a devolver el préstamo si la garantía del agente cae por debajo de un cierto umbral. Caracterizamos formalmente estos estados con garantía. Finalmente, explotamos ambas nociones de seguridad para ilustrar los ataques a la utilización y a la colateralización, destinados a socavar los mecanismos de incentivos de las LP.

Traducción realizada con la versión gratuita del traductor www.DeepL.com/Translator




-->
