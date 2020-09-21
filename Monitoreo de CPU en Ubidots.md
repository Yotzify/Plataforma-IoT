<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Monitoreo de CPU en Ubidots</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="monitoreo-de-cpu-en-ubidots">Monitoreo de CPU en Ubidots</h1>
<h4 id="dicultad-media.">Dicultad: Media.</h4>
<h2 id="tiempo-estimado-1-hora.">Tiempo estimado: 1 hora.</h2>
<h2 id="objetivo">Objetivo:</h2>
<p>Desarrollar un sistema de monitoreo en Node-RED que indique el porcentaje de uso del procesador, para posteriormente ser visualizado en Ubidots mediante la creación de widgets.</p>
<h2 id="requerimientos">Requerimientos:</h2>
<ul>
<li>Computadora con sistema operativo Windows o macOS.</li>
<li>Cuenta Ubidots.</li>
<li>Node.js.</li>
<li>Node-RED.</li>
</ul>
<h2 id="contenido">Contenido:</h2>
<ul>
<li>
<p><a href="#instalaci%C3%B3n-de-node-red-para-windows"> Instalación de Node-RED para Windows.</a></p>
</li>
<li>
<p><a href="#instalaci%C3%B3n-de-node-red-para-mac">Instalación de Node-RED para MAC.</a></p>
</li>
<li>
<p><a href="#utilizando-node-red">Utilizando Node-RED.</a></p>
</li>
<li>
<p><a href="#configuraci%C3%B3n-de-ubidots-y-node-red">Configuración de Ubidots y Node-RED.</a></p>
</li>
<li>
<p><a href="#configuraci%C3%B3n-de-widgets">Configuración de widgets.</a></p>
</li>
</ul>
<h2 id="desarrollo">Desarrollo:</h2>
<h3 id="instalación-de-node-red-para-windows">Instalación de Node-RED para Windows:</h3>
<ol>
<li>
<p>Descarga e instala <a href="https://nodejs.org/en/">Node.js</a>, utiliza la versión recomendada.</p>
</li>
<li>
<p>Verifica que la instalación sea correcta. Accede a la consola de comandos de Windows y ejecuta:</p>
<p><code>node --version &amp;&amp; npm --version</code></p>
</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/8w4-Qxg0gcASJ7PZcB9ZgZdqEudaCZzt8UVfTMS0lcw5A5yBz_dfGETpaGQHpDKgSai99Z_5jeMRZtf_P9SjceMHE3vLGGtWZ74PNUG5hMD8CSI3s56ZNv6Igp6V8DVdXa4SHW5q" alt=""></p>
<blockquote>
<p><strong>En una correcta instalación se mostrará la versión correspondiente de Node.js</strong></p>
</blockquote>
<p><img src="https://lh4.googleusercontent.com/s63owIyI3C7NJpXegpfHd_Y2zB74MS5FmsRuBwVBFqPcPwJVG4XBu5MZHVWP44ybgdR1563B8KI1o-7tI_c1PzIiOO6T1m0be1jc8cUsNR95JKXY5htUuLsRmEXl2144IZzAqZxp" alt=""></p>
<ol start="3">
<li>Ejecuta la siguiente línea de comando para instalar Node-RED:</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/tYh9jZyjdVuSwqENBnErLoUCDc5b4QdN_3QsXSg1zAJpZ91HZcdhejmM93x_GPdk2b1adM_9cCT_WrNHksv22RRu0IHbSZ-hVkNASmiEymJk4rx9AuW0tjDJ29sks3gzKhQCgzOT" alt=""></p>
<ol start="4">
<li>Ejecuta Node-RED con el siguiente comando en la consola:</li>
</ol>
<p><code>node-red</code></p>
<p><img src="https://lh3.googleusercontent.com/gQrgoCAKndlSIBXnZSqFTOYArKMUVUtZMvD1iu9rarHP2J6HM94uvNWS8Nod5wYodhpfoBlKUL-sRVFsbULyxAyez7GK0uNSs2jRUeM9Y3dUcuqRVebpXcj1MwdS6xLWQwAOZWHt" alt=""></p>
<blockquote>
<p><strong>Es importante mantener abierta la consola mientras se esté utilizando Node-RED.</strong></p>
</blockquote>
<ol start="5">
<li>Ingresa a la dirección del servidor en tu navegador.</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/RVQZ8Upl2l-J1HLUnQ-EuMs9Rnq4NAK0hhTkafMwcm2EFGXEfg8b9CsuyfstX4y2XryHWG43Fuc3Xjwz_CwfkofbnUmCkgPI6jNMzXrixcJwC7cxAi-xRyXryGVpQAYHBKgbd9mM" alt=""></p>
<blockquote>
<p><strong>Se debe mostrar la siguiente página:</strong></p>
</blockquote>
<p><img src="https://lh3.googleusercontent.com/N1urQ4t58LTe6RkgNxoHp7ZW9vaE0ga58YPnkjkiF0pKugWkYh2BcQX2kEdedi5UG4o05zihNheki_U6otb769UwqwHa1YWV_b-3_xvdbpHXdyvoAkPNp8DJ2udEG-pqGdWE6Ur5" alt=""></p>
<h3 id="instalación-de-node-red-para-mac">Instalación de Node-RED para MAC:</h3>
<ol>
<li>Descarga <a href="https://nodejs.org/en/download/">Node.js</a>, utiliza la versión recomendada.</li>
</ol>
<p><strong><img src="https://lh6.googleusercontent.com/xEzyrFNQC53MNpIT-dH22jcOvhxTPw856jVT_MZrAryJvaDdgp3yeOs4dEQys6NMuSvidemV53xDgzAneyAT96v_WaLHcn4zLXDkF3zLGwtKzXoOAULUXukbLKIpVuiv_LsKEwM9" alt=""></strong></p>
<ol start="2">
<li>Instala el programa.</li>
</ol>
<p><img src="https://lh6.googleusercontent.com/crUyxNVEew7K-js2E-3dHiVolb60w1-oRBOU-tdo6aw5Wvsj4aPxzWPslYPQGP0yuHtg-4Bgae5_Fh_MYhBZsLQiVX3in731LmFv4iun1P4YAMvVOylwGWc3wFNySPlolEs480PI" alt=""></p>
<ol start="3">
<li>Accede a tu terminal.</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/sQS-uOQgfVFnXRp1Dl08WWdamsJOFU3vPQ6B0MLehrQMBZb83Uqua8HPvI9cTB74EJpSX-63C-nI5Ev_VidMkvvcjnpAoElLek0uwtCC7agRvmUOKRqj0y5j2VJssK-kSgnzUHoB" alt=""></p>
<ol start="4">
<li>Ejecuta la siguiente línea de comando para instalar Node-RED:</li>
</ol>
<p><code>sudo npm install -g --unsafe-perm node-red</code></p>
<p><img src="https://lh5.googleusercontent.com/KpH062UKdIOBD_PSej3cAVlTh9nXnnzcXEgFR7Qowo2zTUO7-Ev3iMP3sL8X0CanmjbmyP2hjLEriiXyGK90IkHXdE12AXsGL6MJq16IfNSkyCwb1QhEwbPOEjJBf3pMGBRizV2s" alt=""></p>
<blockquote>
<p>En caso de que aparezca la siguiente información, introduzca su contraseña (Al momento de escribir no se mostrarán los caracteres escritos, aún así, teclee la contraseña) y dar enter.</p>
</blockquote>
<p><img src="https://lh6.googleusercontent.com/t9N-wN8yoXR7IHFVYfm2ToVvtgNtZUt3De2OnBSmxBktZj2O5rCVDKWdi_wcuGQl2km7Z3oGwXTu1o10m1di7why4ZwqUJ89iYLm-m-Id3kOMHfkec4odeB7gIilvQrJ84ivRooo" alt=""></p>
<blockquote>
<p>Se empezará a instalar Node-RED</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/xTChBatBVnzKRIvSuvm0nMlr5c8BgOFrIbS5h1B0v7YZka7xkgiMRHDFiJQEsy4B-P4EOM2HWDZUsO48PKHkY3tyMjsTWxc_qmZn9vYPVITvzY_K0cHw8xYMy41HYO0kjS6b72l5" alt=""></p>
<ol start="5">
<li>
<p>Ejecuta Node-RED con el siguiente comando en la consola:</p>
<p><code>node-red</code></p>
</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/mHqDzFlV5-1FCsnQWl2L8mfTIdaT8D-7IOANaaSOdw9bre32mPYxfH86T1Y-ydnjT-6FFWWHPJ8OsPh9PI-AbQH-hc3p7MsHuuh1GEpZcplKT8ysGv9kim0SpLmCwDLobdo6NET7" alt=""></p>
<blockquote>
<p>Es importante mantener abierta la terminal mientras se esté utilizando Node-RED.</p>
</blockquote>
<ol start="6">
<li>Ingresa a la dirección del servidor en tu navegador.</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/9xbfjl51W-PT9tn_5Hr28qJLkryS1nsSvR3NSD5__uNWQdp2cMWQWPwlDgddpQz7jps3x8LyhyQsjgxuBYYqh2ze-d8BBu7SDRwFyUZKj1HukSmYT7dYP9lnpTIJI1aH7XVqemwi" alt=""></p>
<blockquote>
<p>Se debe mostrar la siguiente página:</p>
</blockquote>
<p><img src="https://lh3.googleusercontent.com/N1urQ4t58LTe6RkgNxoHp7ZW9vaE0ga58YPnkjkiF0pKugWkYh2BcQX2kEdedi5UG4o05zihNheki_U6otb769UwqwHa1YWV_b-3_xvdbpHXdyvoAkPNp8DJ2udEG-pqGdWE6Ur5" alt=""></p>
<h3 id="utilizando-node-red">Utilizando Node-RED:</h3>
<blockquote>
<p>Por defecto, Node-RED no cuenta con los nodos necesarios para realizar la conexión a Ubidots, por lo cual, es necesario instalarlos de la siguiente manera:</p>
</blockquote>
<ol>
<li>Ingresar al menú y seleccionar Manage Palette, en la pestaña install buscar ubidots-nodered e instalarla.</li>
</ol>
<p><img src="https://lh6.googleusercontent.com/epwyvC6PC6eD2hSR44jqIaE-jJo8dW4ukwQ4uu3fD2CVtPXLh5szK6epARPswgvMrSSCnK86JQpTmDEKPPIalh3Cd6zdtdwKLwLYCOXpkkoO_NuHNN3OiuXPu_17E_cfJwRnOFSh" alt=""></p>
<blockquote>
<p>Se habrán añadido los siguientes elementos:</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/ueXlR92jHJsG41D5eilnJi_ljlUMqbTLSh8LXB1Hd_M0jeAdPk2j-wYKRx_S_fqybm8OF70DV3-9ADnk2tRQa_du7HkYAc0ocecaLEKdgUzJ2xF87b2xOdA9xQWbVA3OrJnqk6h2" alt=""></p>
<ol start="2">
<li>De la misma manera instalar: <code>node-red-contrib-cpu</code></li>
</ol>
<p><img src="https://lh3.googleusercontent.com/8p5KYYYN1lQCc3Y1dTGxvM8nv-iwJlLXnjpfSOsJGQ6aXbWQaXAoDrme5z2DF4RzwC_0aMrkLnZB9XvYI0yHRwMa0n5gZb9mDfKk717qC4y7wqrXCH6SqcVytbSGuaRJ5Pn6j4M8" alt=""></p>
<ol start="3">
<li>Insertar los siguientes nodos:</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/i1nVq0OFwIrkuv0TqnESDZi4dUw8oRJ9xOtUHVnWEMIw2-Z_KX8ABj3qcUzyNl9gVchfC-zxlu_XUhU7Jwzq1zeXiwYO5T9YP6IdF5BzBk3pX8x4QexCULobiS9u98MiD5PErZOP" alt=""><img src="https://lh3.googleusercontent.com/rSLZm-gnE7AHCH7ebbFijsUOZJGXUe_fNgUXq9z8N9P_UndPD345BTYw1J1j-ghRLt8YoeA2VKmxhVWXJYefIpt6yvairv2_oYKm6wnjPg9Z5gvKQUoNhYkm_dcI_4vBXSfRqTH3" alt=""><img src="https://lh3.googleusercontent.com/Zfbrt-35jCKCrItYOUHRkM9JlZk69SPXe0EC55d9N9oH51B5PbLS1xzmEBBZ164rczCCKAGsehC-4iB_lD0khRHBzd7FzoaKdpjg0dORbaas-LQvknrO1TRKFOa4gRSMP8aIFb75" alt=""></p>
<blockquote>
<p>Inject: Inserta un pulso cada vez que es presionado o cada determinado tiempo.</p>
<p>CPU: Recopila información sobre el uso del procesador.</p>
<p>Debug: Muestra la información del mensaje del nodo anterior.</p>
</blockquote>
<ol start="4">
<li>Conectalos de la siguiente manera:</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/NAC_06w23uwyCmawtVqPOz3OYfyBItcl1IBc0FG2DQdjswNpiLhu0JYziyt6fyXLGos9Myp1rmMgmRS7RpM4N-Le860gT37sSIzLyEf-TEEcYHxwFcRMzbc64XP48jjpBEceJDF-" alt=""></p>
<ol start="5">
<li>Accede al nodo de CPU usage y selecciona “Send a message for overall usage”</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/UDT3WW5M4SOlGtJ7ASqNp39K6EUS7eetRaMMq-8bsQIsZSWfdIaB4_GYY9U4mqPyBNZYux_BPpYaa6TXRI6FouTO6aDL9KQxROxJES851NBDLE5cBk2W9_V5xswIn4IqcX0gxW-j" alt=""></p>
<blockquote>
<p>Para poder observar los mensajes debug, se debe cambiar a la pestaña debug. Para guardar tu trabajo y ejecutar los nodos, selecciona el botón Deploy.</p>
</blockquote>
<p><img src="https://lh3.googleusercontent.com/0sEciW7BL7Jn2WyCRx_wyyS25ge-VOymHTGLWaIPGtr3WEDyLNuBC2NKAhmpxVwHtCfYsG4NvZu5mv3autr1-7w3FvfiE6V7pRLP96TdJPmLepXdzzwBBl3-x9q1eWSmsExHEkxo" alt=""></p>
<ol start="6">
<li>Presiona el botón en el nodo timestamp y se mostrará un mensaje con el uso del CPU.</li>
</ol>
<p><img src="https://lh4.googleusercontent.com/7S8mnKBPTmxek4cFVfxRGLHwjQw6UM8flcuIWRBrn45tF8KfE1omxyM-bKQGzVZl4ikhedss7TdipI-_LTkSET8SMJ3X0eM3MqUn9Z-_Yna52EhGIYhFe9uVrObhX3L48DNDCL3G" alt=""></p>
<p><img src="https://lh5.googleusercontent.com/k06rCM435r9Dq8aIl1BSxqJkkDJRJbw9MRWX6Ol3Xmf61OKSkS1_WhGwC22jkgbBbz_6upIr1VpI34jo6km75be1dCn5Dp4vi7tCx5Gu_vHAz5BbTTgfqsH0yfehrAAXO3lhx_8B" alt=""></p>
<h3 id="configuración-de-ubidots-y-node-red">Configuración de Ubidots y Node-RED:</h3>
<ol>
<li>
<p>Ingresa a <a href="https://ubidots.com/">Ubidots</a> y crea una cuenta educacional.</p>
</li>
<li>
<p>Selecciona el apartado de Devices y da click en el símbolo de +.</p>
</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/BczYK1x1PVbxkgZFBV1TmVbcHVztofiGqSKKAuD03c6VuG0uTWRsDoxHtv64jw_GAWUFG0dcJsLrGJOfRU8MGJgZXEXeGhtjfGWsMhgLzA4u4uW_hfZDg95GBeVVFX6EBziT0Ysy" alt=""></p>
<ol start="3">
<li>Selecciona Blank Device y asígnale un nombre.</li>
</ol>
<p><strong><img src="https://lh6.googleusercontent.com/0jKbCRAgxDqgecU9bCEk9qd91u4MU855I8d5UhYMa9DBNUu6VK3V7dfb1d0H2qRyqEF0RHLyOSMELZOCyTeOSftt-RkxA-khksGLGm0zTjQrZ4FGdN5hTPxOCJxZDZFESIWV_TTX" alt=""></strong><br>
<img src="https://lh5.googleusercontent.com/WSJmO0IJEOTJtpYmBNyi1dmcjNj5xI4NHJtd3OJUHHI-2_Zui6tsf8OmBxFg9KiT13DcGSrFiDwHg_qlSc5BhM_b_vhgedS5R7rdVUSMrNmFZqdAPRaUIPm7r6VCrASU3T_WbeP7" alt=""></p>
<ol start="4">
<li>Confirma la creación de tu dispositivo.</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/J-fzKrrSGEP5-HuiRvPBYQF3DHkKZ8RCNGJB3-vj-d-Q3JbCnn1pLz1TeSiCK-547Jr0xpPsUpj265eCN8YNvnfTHreHr8u1LSr5VxrHXKSkPdbIJJhAGkYu-pNoqnpbCcOspcKX" alt=""></p>
<ol start="5">
<li>Obtener token de acceso. Al hacer click en tu foto de perfil se desplegará el menú de opciones, seleccionar “Api Credentials” y anotar la información del token.</li>
</ol>
<p><img src="https://lh4.googleusercontent.com/_mtVvzgCouEHxXMXIcPPiiAs17sNRYfGbXAmturD1epiwqB5GTwlzI9gY4Mb_BxQsh5YCRYmmGl4kELlHO9pOhytjw5Yz0piyYyFl1zGR90w12DGHgC6_-uT27t2UgXSoc465lS1" alt=""></p>
<p><img src="https://lh6.googleusercontent.com/Rd8L9GwLIB3NEs_-eEfOkFpQi2Ms8-qOnxXTyepofqYyBbsjNxlWk769QI-2lvMMajwV1cVmzbgYvrHEq6pNsdbJ4m4WyvqUCnKjXFZaPFQG90-JEAZ7TtMKrdIke5kp5xpMyfRY" alt=""></p>
<ol start="6">
<li>Añade los nodos de function, ubidots-out, switch y conectalos de la siguiente manera:</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/pAGZCeEvyO_ni6dsBdwkmmBbRrB-2wJsJPyMTgcL8aBh83newowZMIfoKiGiGNFCAgbTKrjlfuXONRvltzmgPYMPm0U2dCWoGn5sVEjlFDOQMCdn-tJziEqP9UH0ybVFYRv5llmf" alt=""></p>
<blockquote>
<p>El nodo switch se conectará más adelante.</p>
<p>Function: Permite escribir una función JavaScript para modificar mensajes.</p>
<p>Switch: Envía la información por diferentes canales dependiendo las condiciones definidas.</p>
<p>Ubidots-Out: Se encarga de mandar la información al backend de  Ubidots.</p>
</blockquote>
<ol start="7">
<li>Accede al nodo Ubidots out y configurarlo con su información correspondiente.</li>
</ol>
<blockquote>
<p>Configurar los campos de la siguiente manera:</p>
</blockquote>
<p><img src="https://lh4.googleusercontent.com/m7YPq01NYBz7NGXdi1xkWUiLphWmfNEzcClO7HKzmV9t6j72EcYCCLLK0HeHGNGwKOtm7ZUbp5GsEmUZF3NJC8o3ZGiU3JDDNgJfjgnPe-GjojKT9Giz4O1QprFWFhO17r-qJkqx" alt=""></p>
<blockquote>
<p>Account Type: Ubidots for Education.</p>
<p>Name: Nombre del nodo, puede ser el que guste.</p>
<p>Token: Credencial de token previamente anotada.</p>
<p>Device Label: Nombre del dispositivo registrado en Ubidots.</p>
<p>Ubidots espera un mensaje con un formato específico, por lo que es necesario utilizar una función para modificar la información, la cual debe contar con esta forma:</p>
</blockquote>
<pre><code>{

"device_label": “Nombre de tu dispositivo”,

"payload": {"Nombre de tu variable": "Valor de tu variable"}

}
</code></pre>
<blockquote>
<p>Se deben modificar la sección nombre de dispositivo, nombre de variable y valor de tu variable, dependiendo de los nombres que les hayas asignado.</p>
</blockquote>
<ol start="8">
<li>Accede al primer nodo de función y escribe el siguiente código:</li>
</ol>
<p><img src="https://lh4.googleusercontent.com/b1q4g772aIszuysLiUjmM7EMU0Df5YAjAMpZnI2zrySyq9UJCYXSjSAkrbNJFYjlJ1pJIwQ5HPhMARyjGMpfvc9EiwvGxa8CDAXY_YtzaSkBlu2RLEr4yFY6qGgbaU2taAYPaxXj" alt=""></p>
<pre><code>msg ={

"device_label": "windows",

"payload": {"CPU LOAD": msg.payload}

}

return msg
</code></pre>
<ol start="9">
<li>Accede al segundo bloque de función y escribe el siguiente código:</li>
</ol>
<p><img src="https://lh6.googleusercontent.com/0jezMScFCzXii4CxnO5miKVMlN8LhLAXRg0VPYFVcTsDBNmM3_0ctq8BMmgt-mO7wW6lpWVbvMjQwACnLv2Y3pwkGdeVl8OHKuXfcDyFHluUL3kQXKBxidChhHVEo4AauOgffnmC" alt=""></p>
<pre><code>msg ={

"device_label": "windows",

"payload": {"ADVERTENCIA": 1}

}

return msg
</code></pre>
<ol start="10">
<li>Accede al tercer bloque de función y escribe el siguiente código:</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/JOkyyL4ic9HlQYvhA0wvdB8kgKB3RYzk6I-8Scm1f5XDiPwWTXrTDMbVEzMhPtYVjhXX_QJi1D4ifFtLmvSVLfjtfAP7t8keECx8sPuWBqmzIPwJ23IUhIrdrJuZjeOteOnlboED" alt=""></p>
<pre><code>msg ={

"device_label": "windows",

"payload": {"ADVERTENCIA": 0}

}

return msg
</code></pre>
<blockquote>
<p>La primera función se encarga de enviar la información del uso del procesador, mientras que las otras 2 sirven como advertencia para indicar una carga normal o alta (normal = 0, alta=1), por lo que es necesario tener un selector, para esto se utiliza el nodo de switch.</p>
</blockquote>
<ol start="11">
<li>Accede al nodo switch y configura los valores mínimos y máximos de carga del procesador, es importante conocer a qué porcentaje se encuentra trabajando tu procesador en este momento, así podrás establecer un rango correcto para esta prueba.</li>
</ol>
<blockquote>
<p>Utiliza el Administrador de Tareas para conocer el porcentaje de uso de tu procesador.</p>
</blockquote>
<p><img src="https://lh3.googleusercontent.com/LEbQiVD7WYlvLO4HeLCCbZ2rFtsDXNs2_Ytso6yhTRqJdaxIxKjoBK2KuAFEWsDS80bUMXBJeCS481SErDh-C9Jy70fJ4QXW4obskARD7ba420Hj3ooGZcMlmw0DQQNYpXb_Ooqe" alt=""></p>
<p><img src="https://lh6.googleusercontent.com/2cAuu3AeD8g6d5WhrdZp_JQqMt0Og6ju7d_AyEkAxAmKsntwdyL6CJafl5MtSvIOa0MFk5vubs0ErSVGg6In11pQBRiWzky2kLNG-putXXFZYP-P0HYiBriGJtBVy4EjOMtIggku" alt=""></p>
<blockquote>
<p>Para este caso en particular el procesador se encuentra variando entre 4% y 10%, por lo que para esta prueba cualquier porcentaje por debajo del 5% será considerado como normal y arriba de 6% como una sobrecarga.</p>
</blockquote>
<p><img src="https://lh6.googleusercontent.com/aLbOXM-sRiXitrUkOa6_B4nWpiz1kiKcO5PTv7naImndp22QYmWmknx39m3Pz0GF6pX5uyWNhDth1anVvjxUPHEH0fLTJ-DUkIrkdzHTzOu9Xbb3RdV7J2jPPmE1wswK-KRT3NFy" alt=""></p>
<blockquote>
<p>Esto causará que el nodo switch cuente con dos salidas, las cuales deben conectarse de la siguiente manera:</p>
</blockquote>
<p><img src="https://lh6.googleusercontent.com/NwiKPZpj97pwnNTiCBlvV7-JBg6qET6U-GyKnzAvnjm7DCvVjNRFvK30JKoCbqzVdfYrVZU1D6rRH7E7yBuKzdcIMJD1tflUktbPQVVSDqFS8ML-XbNiT04veFpk0SZJPWZ1MTJO" alt=""></p>
<ol start="12">
<li>Da click en el botón de Deploy.</li>
</ol>
<p><img src="https://lh3.googleusercontent.com/f8F_G-ne49RydErdTBD2zbdEP4__raLBqoRXd572TQdRh4psZket6B8Kg88BKI4SYVrkp67SzRYOTsgdTmQ29u0dorOP5ug6xoF5YM3CfEbwcUOaVul1Qc3U8XFsNKbSDFbNpFsV" alt=""></p>
<ol start="13">
<li>Da click en el botón de timestamp y accede a tu dispositivo en Ubidots, la información se habrá actualizado.</li>
</ol>
<p><img src="https://lh6.googleusercontent.com/_iXJRfTjnYDKy7zgaKZAwnYuv6kNq46bsVV351spl04Gqqu8YduF4FasI_4TIcNHWhdtwb6Twrj3QqanKCJu1Cv2oEC7h87uRbiVHvMfv65844o9wOgZc6WtQZEy21wP7goGCFlX" alt=""></p>
<h3 id="configuración-de-widgets">Configuración de widgets:</h3>
<ol>
<li>En la parte de Data, accede a la sección de Dashboards y da click en el símbolo de +, selecciona Gauge para crear un nuevo widget.</li>
</ol>
<p><img src="https://lh4.googleusercontent.com/bNVOAva6PT5HX_CqCGYcODzqItMH_broow_lgvcDnhMtKI90nbUmvZQCbSPqGKKCkgjszu7uqICplGM6hpFnSqF2j0ew5-hcSs2cxYU5YJd2Gx1pp1u-Bww7CmpK41-9-K__k__d" alt=""></p>
<p><img src="https://lh4.googleusercontent.com/P1jG895FFbWcRfrT0MjdVPdDx2MEyCOSgcg82pDwjUVr7oU284jI8ooALybKKDiRJBB3IKex03NRoLv73hDfZ8W7g6vhpp7oZt0cx7KyizRr-E4VLSPE53pV8OsygFtEds5SkPwS" alt=""></p>
<ol start="2">
<li>En la sección de Gauge, hacer click en “add variable”.</li>
</ol>
<p><img src="https://lh4.googleusercontent.com/Xcns-3eBco8YKp8aVGU0khn2BVG7_2FNpQ6B85mb60PgiiMYAQM1CwtODU_zxw_UVQdmGfPXSL-ibcJfKY3kuVi5qgXPv5xoPNqw6Uu7yNBJKO69lP9Ooa89-0OtFBx_kwT6azT5" alt=""></p>
<p>Selecciona tu dispositivo y la variable cpu-load, confirma la selección.</p>
<p><img src="https://lh5.googleusercontent.com/nXMGfBJOC69cAcu2hmpd9Iwf_qNtYOjst08sTgUS4gkgjA7lc2ChlZLPQj09wih_5fW83Xf65raTBVe5izxt9S82OFtLCPr4u3HfurllN930iLValien5npowsvOXq_qIoyfhuyM" alt=""></p>
<blockquote>
<p>Modifica su nombre y confirma su configuración.</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/SaHQGGOTLZtA_gWcpbTUWma2WnUwq-McevKYHFJst3B-OzWsqdUZC7RixsV6I5Ra_pOY1jxOkj_Dnri84dw10qXePAXPbTQEMy_ASzTzAElxX2ywgUSzXjZBHzhmHSSwulnsaZ3W" alt=""></p>
<blockquote>
<p>Se obtendrá el siguiente widget:</p>
</blockquote>
<p><strong><img src="https://lh5.googleusercontent.com/AbiZ3NW2APn_VdTePETgjfYmz8PX0MY3REEYXDdKJTdpMYkqHgD9ApG2eC22Zl-4Q3rnvuE-QBQl43C6hmCqpKuIqXL98Ael-UvFbKrsDHBplSE-Ibb6d0z1j1Ksexohz8qKFghE" alt=""></strong></p>
<ol start="3">
<li>Crea otro widget del tipo indicator y añade la variable de advertencia.</li>
</ol>
<p><img src="https://lh6.googleusercontent.com/A-58weT1tHNMrhQtZ8xM1erGgkpmUmUvMIEFukHdeRalRaFzGoeoI6jggimcKJc7PQH_G0S0x2SCALSdpEw_rAOQ7HWz054VgMiOplSDN5cODPoBnFIA949da09i_9TASc7o2TuI" alt=""></p>
<p><img src="https://lh5.googleusercontent.com/ugIrWnmWyoVcj0HI-Fp78WcoDMxf1_xplD8sl4__eTcdVzFaLNkhplKQdmmVmQvi4rIKlCMnqTDVNkmxMKnAEr--t5GYFaFOkbWRlrGy-PmTXzv_5eJizLQLkFhwKeznpSqIT_dE" alt=""></p>
<blockquote>
<p>Selecciona la opción de “Add color logic” y configurarlo de la<br>
siguiente manera:</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/YVaT9Uu2IpgMVq_hf0uC0p7S-7qGNTT5r7ZIKNCnilMfEf6PRt-BNqgzEqlZpRxBwPe26pLnp2sTasUHhAfhx1p3J59ayvGU8e-oRBQY7K1tHsAEklbgKFYAUeaxrdcwbNfdw27N" alt=""></p>
<blockquote>
<p>Ahora se cuenta con dos widgets, donde se puede ver la carga del procesador y una advertencia en caso de sobrecarga.</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/hEsuP2QnIAY6RllFiHqU9HIjJ9g-nTVHYkpRrwUrZlC-qYfMCqWtHJ8wYOse7y4BYLzjJlt5uJTq_UI-GCYGPpIA8x6mJLlE8eKSf6yja96LiTs5AIGWxch9nuwM3Yg3AFOrdUAg" alt=""></p>
<blockquote>
<p>Por último se configurará el nodo de timestamp para que cada 10 segundos se actualice la información.</p>
</blockquote>
<ol start="4">
<li>En node red accede al nodo timestamp y modifica su configuración de la siguiente manera:</li>
</ol>
<p><img src="https://lh5.googleusercontent.com/Z1m8nwasSav9YttZYkKpkOBN_dxOYlsfDjGiqK0lVOPg9dIkjkatJ5bHGSSvGav5PTBczoW8fLypvIcMzmCzh9D9Fd3q1CapQC2m1KllmZ0OsqjnIFsMyoAHY5nkfZmCZN41QqnV" alt=""></p>
<blockquote>
<p>Recuerda que puedes modificar los valores en los que quieras indicar una sobrecarga o carga normal, en el nodo switch.</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/EPAI7GYIN_r2dIVwkkbWAsVHj3D3GSFgWvoDRuzjoCsTGf-oQ-pf2tPvIOj1Q4tPJg_ZUGPR9a2bmgd-TvE-D347oG14K1EhSg41MfeqAhBS4SRCcOUYxa8gL4YH7YYpITwIjL-d" alt=""></p>
<blockquote>
<p>De la misma forma puedes acceder a tu dispositivo en Ubidots y seleccionar cualquier variable para inspeccionar su información.</p>
</blockquote>
<p><img src="https://lh5.googleusercontent.com/rN1QjyzWgv03J-VtehaTJL6EVFRvBnEyCoZrD-7HdaSTv1zI2gu1-tFMz4jwvTys3bhZHbvu0J1HvLjjd1iD8jWrEFU-P5hNALgpKS5MajviqOFGvkSOQ0cVU9JvDXgSf6qtsn3u" alt=""></p>
</div>
</body>

</html>
