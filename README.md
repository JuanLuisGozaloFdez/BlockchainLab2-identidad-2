# UNIR Curso Experto Desarrollo Aplicaciones Blockchain

## Práctica de Identidad Digital

En esta práctica se usará un modelo ERC-725 y ERC-735 para practicar y afianzar los conceptos de Identidad Digital en Blockchain.

## Actividad

El alumno debe modificar las funciones indicadas en las llamadas del fichero index.html de la carpeta web para hacer las correspondientes llamadas a las funciones públicas de los Smart Contracts factilitados.

El resultado de las llamadas se puede ver a través del navegador.

## Requerimientos previos

- REMIX IDE : <https://remix.ethereum.org/> accesible por navegador
- Node.js : <https://nodejs.org/>
- npm
- remixd. Disponible como paquete npm 
- Ganache (para tener una red de prueba y cuentas) : <https://trufflesuite.com/ganache/>. Descargar versión según Sistema Operativo.
- python3
- Un editor de texto para modificar el index.html (Visual Studio Code, notepad, etc...)

## Cómo empezar

En un directorio nuevo, ejecutar

`` 
$> git clone ESTE-REPOSITORIO
$> npm init
$> npm install -g @remix-project/remixd
``

Arrancar Ganache (en modo gráfico o consola), ejecutar (ejemplo, según version)

``
$> ./ganache-*.AppImage
``

Se mostrará en la pantalla, la dirección donde se está ejecutando, el puerto y el número de la red, así como las cuentas con ETH asignadas en prueba.

Arrancar remixd desde la línea de comandos del Sistema operativo para

``
$> remixd -s directorio-del-código/BlockchainLab2-identidad-2 --remix-ide http://remix.ethereum.org
``

Conectar REMIX IDE con remixd para acceder a los ficheros locales. Desde dentro de la pantalla de RemixIDE, opción "Connect to Localhost". Si es todo correcto, se mostrarán los ficheros del directorio en la página de RemixIDE.

Editar el fichero index.html para poner la URL donde se está ejecutando Ganache y el puerto correspondiente.

Compilar los contratos "ClaimHolder.sol" y "ClaimVerifier.sol".

Desplegar los contratos eligiendo un "Environment"="Web3 Provider" que será nuestro servidor Ganache. Asegurar que ponemos el puerto correcto de Ganache.

Para desplegar los contratos, se debe ir eligiendo una cuenta diferente para cada elemento de la práctica (Alumno, Universidad, Empresa) y se debe asociar cada uno a su contrato correspondiente según corresponda:

- el Alumno es ¿ClaimHolder o ClaimVerifier?
- la Universidad es ¿ClaimHolder o ClaimVerifier?
- la Empresa es ¿ClaimHolder o ClaimVerifier?

Cada vez que se despliega un contrato en RemixIDE va asignando un address que debemos copiar dentro del index.html en el apartado correspondiente a cada actor.

En el caso del ClaimVerifier, al desplegar el contrato, se necesita un parámetro (el verificador confiable). Hay que seleccionar la address del contrato desplegado correspondiente ¿es el del Alumno o el de la Universidad o el de la Empresa?

Por último, se lanzará la web. Para ello, en una ventana de Consola del Terminal, que quedará cautiva, ejecutaremos

``
$> python3 -m http.server
``

Ahora, ya podremos lanzar el navegador y acceder a la página <https://localhost:8000> para ver el index.html e iniciar la práctica

## Acciones posteriores a desarrollar por el alumno

En el código Web3 de index.html sólo se facilita la función inicial y deben completarse las funciones restantes:

- Emisión de credencial
- Acceptación de credencial
- Verificación de credencial




