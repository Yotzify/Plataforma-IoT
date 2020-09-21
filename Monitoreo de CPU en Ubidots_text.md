# Monitoreo de CPU en Ubidots
#### Dicultad: Media.

## Tiempo estimado: 1 hora.


## Objetivo: 

Desarrollar un sistema de monitoreo en Node-RED que indique el porcentaje de uso del procesador, para posteriormente ser visualizado en Ubidots mediante la creación de widgets.

## Requerimientos:

- Computadora con sistema operativo Windows o macOS.
- Cuenta Ubidots.
- Node.js.
- Node-RED.

## Contenido:

-  [ Instalación de Node-RED para Windows.](#instalación-de-node-red-para-windows)
    
-   [Instalación de Node-RED para MAC.](#instalación-de-node-red-para-mac)
    
-   [Utilizando Node-RED.](#utilizando-node-red)
    
-   [Configuración de Ubidots y Node-RED.](#configuración-de-ubidots-y-node-red)
    
-   [Configuración de widgets.](#configuración-de-widgets)

## Desarrollo:

### Instalación de Node-RED para Windows: 

1.  Descarga e instala [Node.js](https://nodejs.org/en/), utiliza la versión recomendada.
    
2.  Verifica que la instalación sea correcta. Accede a la consola de comandos de Windows y ejecuta:

    `node --version && npm --version`
   
   ![](https://lh3.googleusercontent.com/8w4-Qxg0gcASJ7PZcB9ZgZdqEudaCZzt8UVfTMS0lcw5A5yBz_dfGETpaGQHpDKgSai99Z_5jeMRZtf_P9SjceMHE3vLGGtWZ74PNUG5hMD8CSI3s56ZNv6Igp6V8DVdXa4SHW5q)
> **En una correcta instalación se mostrará la versión correspondiente de Node.js**

![](https://lh4.googleusercontent.com/s63owIyI3C7NJpXegpfHd_Y2zB74MS5FmsRuBwVBFqPcPwJVG4XBu5MZHVWP44ybgdR1563B8KI1o-7tI_c1PzIiOO6T1m0be1jc8cUsNR95JKXY5htUuLsRmEXl2144IZzAqZxp)


3. Ejecuta la siguiente línea de comando para instalar Node-RED:

![](https://lh3.googleusercontent.com/tYh9jZyjdVuSwqENBnErLoUCDc5b4QdN_3QsXSg1zAJpZ91HZcdhejmM93x_GPdk2b1adM_9cCT_WrNHksv22RRu0IHbSZ-hVkNASmiEymJk4rx9AuW0tjDJ29sks3gzKhQCgzOT)

4.  Ejecuta Node-RED con el siguiente comando en la consola:

`node-red`

![](https://lh3.googleusercontent.com/gQrgoCAKndlSIBXnZSqFTOYArKMUVUtZMvD1iu9rarHP2J6HM94uvNWS8Nod5wYodhpfoBlKUL-sRVFsbULyxAyez7GK0uNSs2jRUeM9Y3dUcuqRVebpXcj1MwdS6xLWQwAOZWHt)

> **Es importante mantener abierta la consola mientras se esté utilizando Node-RED.**

5.  Ingresa a la dirección del servidor en tu navegador.
    

![](https://lh5.googleusercontent.com/RVQZ8Upl2l-J1HLUnQ-EuMs9Rnq4NAK0hhTkafMwcm2EFGXEfg8b9CsuyfstX4y2XryHWG43Fuc3Xjwz_CwfkofbnUmCkgPI6jNMzXrixcJwC7cxAi-xRyXryGVpQAYHBKgbd9mM)

>**Se debe mostrar la siguiente página:**

![](https://lh3.googleusercontent.com/N1urQ4t58LTe6RkgNxoHp7ZW9vaE0ga58YPnkjkiF0pKugWkYh2BcQX2kEdedi5UG4o05zihNheki_U6otb769UwqwHa1YWV_b-3_xvdbpHXdyvoAkPNp8DJ2udEG-pqGdWE6Ur5)

### Instalación de Node-RED para MAC:

1.  Descarga [Node.js](https://nodejs.org/en/download/), utiliza la versión recomendada.
    

**![](https://lh6.googleusercontent.com/xEzyrFNQC53MNpIT-dH22jcOvhxTPw856jVT_MZrAryJvaDdgp3yeOs4dEQys6NMuSvidemV53xDgzAneyAT96v_WaLHcn4zLXDkF3zLGwtKzXoOAULUXukbLKIpVuiv_LsKEwM9)**

2.  Instala el programa.
    

![](https://lh6.googleusercontent.com/crUyxNVEew7K-js2E-3dHiVolb60w1-oRBOU-tdo6aw5Wvsj4aPxzWPslYPQGP0yuHtg-4Bgae5_Fh_MYhBZsLQiVX3in731LmFv4iun1P4YAMvVOylwGWc3wFNySPlolEs480PI)

3.  Accede a tu terminal.
    

![](https://lh5.googleusercontent.com/sQS-uOQgfVFnXRp1Dl08WWdamsJOFU3vPQ6B0MLehrQMBZb83Uqua8HPvI9cTB74EJpSX-63C-nI5Ev_VidMkvvcjnpAoElLek0uwtCC7agRvmUOKRqj0y5j2VJssK-kSgnzUHoB)

4.  Ejecuta la siguiente línea de comando para instalar Node-RED:
    

`sudo npm install -g --unsafe-perm node-red`

  

![](https://lh5.googleusercontent.com/KpH062UKdIOBD_PSej3cAVlTh9nXnnzcXEgFR7Qowo2zTUO7-Ev3iMP3sL8X0CanmjbmyP2hjLEriiXyGK90IkHXdE12AXsGL6MJq16IfNSkyCwb1QhEwbPOEjJBf3pMGBRizV2s)

> En caso de que aparezca la siguiente información, introduzca su contraseña (Al momento de escribir no se mostrarán los caracteres escritos, aún así, teclee la contraseña) y dar enter.

![](https://lh6.googleusercontent.com/t9N-wN8yoXR7IHFVYfm2ToVvtgNtZUt3De2OnBSmxBktZj2O5rCVDKWdi_wcuGQl2km7Z3oGwXTu1o10m1di7why4ZwqUJ89iYLm-m-Id3kOMHfkec4odeB7gIilvQrJ84ivRooo)

 
> Se empezará a instalar Node-RED


![](https://lh5.googleusercontent.com/xTChBatBVnzKRIvSuvm0nMlr5c8BgOFrIbS5h1B0v7YZka7xkgiMRHDFiJQEsy4B-P4EOM2HWDZUsO48PKHkY3tyMjsTWxc_qmZn9vYPVITvzY_K0cHw8xYMy41HYO0kjS6b72l5)

5.  Ejecuta Node-RED con el siguiente comando en la consola:
    
    `node-red`

![](https://lh5.googleusercontent.com/mHqDzFlV5-1FCsnQWl2L8mfTIdaT8D-7IOANaaSOdw9bre32mPYxfH86T1Y-ydnjT-6FFWWHPJ8OsPh9PI-AbQH-hc3p7MsHuuh1GEpZcplKT8ysGv9kim0SpLmCwDLobdo6NET7)

  

> Es importante mantener abierta la terminal mientras se esté utilizando Node-RED.

  

6.  Ingresa a la dirección del servidor en tu navegador.
    

![](https://lh5.googleusercontent.com/9xbfjl51W-PT9tn_5Hr28qJLkryS1nsSvR3NSD5__uNWQdp2cMWQWPwlDgddpQz7jps3x8LyhyQsjgxuBYYqh2ze-d8BBu7SDRwFyUZKj1HukSmYT7dYP9lnpTIJI1aH7XVqemwi)

> Se debe mostrar la siguiente página:

![](https://lh3.googleusercontent.com/N1urQ4t58LTe6RkgNxoHp7ZW9vaE0ga58YPnkjkiF0pKugWkYh2BcQX2kEdedi5UG4o05zihNheki_U6otb769UwqwHa1YWV_b-3_xvdbpHXdyvoAkPNp8DJ2udEG-pqGdWE6Ur5)

### Utilizando Node-RED:

> Por defecto, Node-RED no cuenta con los nodos necesarios para realizar la conexión a Ubidots, por lo cual, es necesario instalarlos de la siguiente manera:


1.  Ingresar al menú y seleccionar Manage Palette, en la pestaña install buscar ubidots-nodered e instalarla.
    

![](https://lh6.googleusercontent.com/epwyvC6PC6eD2hSR44jqIaE-jJo8dW4ukwQ4uu3fD2CVtPXLh5szK6epARPswgvMrSSCnK86JQpTmDEKPPIalh3Cd6zdtdwKLwLYCOXpkkoO_NuHNN3OiuXPu_17E_cfJwRnOFSh)

> Se habrán añadido los siguientes elementos:

  
![](https://lh5.googleusercontent.com/ueXlR92jHJsG41D5eilnJi_ljlUMqbTLSh8LXB1Hd_M0jeAdPk2j-wYKRx_S_fqybm8OF70DV3-9ADnk2tRQa_du7HkYAc0ocecaLEKdgUzJ2xF87b2xOdA9xQWbVA3OrJnqk6h2)

  
2.  De la misma manera instalar: `node-red-contrib-cpu`

  

![](https://lh3.googleusercontent.com/8p5KYYYN1lQCc3Y1dTGxvM8nv-iwJlLXnjpfSOsJGQ6aXbWQaXAoDrme5z2DF4RzwC_0aMrkLnZB9XvYI0yHRwMa0n5gZb9mDfKk717qC4y7wqrXCH6SqcVytbSGuaRJ5Pn6j4M8)

  

3.  Insertar los siguientes nodos:
    

  

![](https://lh3.googleusercontent.com/i1nVq0OFwIrkuv0TqnESDZi4dUw8oRJ9xOtUHVnWEMIw2-Z_KX8ABj3qcUzyNl9gVchfC-zxlu_XUhU7Jwzq1zeXiwYO5T9YP6IdF5BzBk3pX8x4QexCULobiS9u98MiD5PErZOP)![](https://lh3.googleusercontent.com/rSLZm-gnE7AHCH7ebbFijsUOZJGXUe_fNgUXq9z8N9P_UndPD345BTYw1J1j-ghRLt8YoeA2VKmxhVWXJYefIpt6yvairv2_oYKm6wnjPg9Z5gvKQUoNhYkm_dcI_4vBXSfRqTH3)![](https://lh3.googleusercontent.com/Zfbrt-35jCKCrItYOUHRkM9JlZk69SPXe0EC55d9N9oH51B5PbLS1xzmEBBZ164rczCCKAGsehC-4iB_lD0khRHBzd7FzoaKdpjg0dORbaas-LQvknrO1TRKFOa4gRSMP8aIFb75)


> Inject: Inserta un pulso cada vez que es presionado o cada determinado tiempo.
> 
>   
> 
> CPU: Recopila información sobre el uso del procesador.
> 
>   
> 
> Debug: Muestra la información del mensaje del nodo anterior.

  

4.  Conectalos de la siguiente manera:
    

  

![](https://lh3.googleusercontent.com/NAC_06w23uwyCmawtVqPOz3OYfyBItcl1IBc0FG2DQdjswNpiLhu0JYziyt6fyXLGos9Myp1rmMgmRS7RpM4N-Le860gT37sSIzLyEf-TEEcYHxwFcRMzbc64XP48jjpBEceJDF-)

5.  Accede al nodo de CPU usage y selecciona “Send a message for overall usage”
    

![](https://lh3.googleusercontent.com/UDT3WW5M4SOlGtJ7ASqNp39K6EUS7eetRaMMq-8bsQIsZSWfdIaB4_GYY9U4mqPyBNZYux_BPpYaa6TXRI6FouTO6aDL9KQxROxJES851NBDLE5cBk2W9_V5xswIn4IqcX0gxW-j)

> Para poder observar los mensajes debug, se debe cambiar a la pestaña debug. Para guardar tu trabajo y ejecutar los nodos, selecciona el botón Deploy.

  

![](https://lh3.googleusercontent.com/0sEciW7BL7Jn2WyCRx_wyyS25ge-VOymHTGLWaIPGtr3WEDyLNuBC2NKAhmpxVwHtCfYsG4NvZu5mv3autr1-7w3FvfiE6V7pRLP96TdJPmLepXdzzwBBl3-x9q1eWSmsExHEkxo)

  

6.  Presiona el botón en el nodo timestamp y se mostrará un mensaje con el uso del CPU.
    

  

![](https://lh4.googleusercontent.com/7S8mnKBPTmxek4cFVfxRGLHwjQw6UM8flcuIWRBrn45tF8KfE1omxyM-bKQGzVZl4ikhedss7TdipI-_LTkSET8SMJ3X0eM3MqUn9Z-_Yna52EhGIYhFe9uVrObhX3L48DNDCL3G)

  

![](https://lh5.googleusercontent.com/k06rCM435r9Dq8aIl1BSxqJkkDJRJbw9MRWX6Ol3Xmf61OKSkS1_WhGwC22jkgbBbz_6upIr1VpI34jo6km75be1dCn5Dp4vi7tCx5Gu_vHAz5BbTTgfqsH0yfehrAAXO3lhx_8B)

### Configuración de Ubidots y Node-RED:

1.  Ingresa a [Ubidots](https://ubidots.com/) y crea una cuenta educacional.
    
2.  Selecciona el apartado de Devices y da click en el símbolo de +.
    

  

![](https://lh3.googleusercontent.com/BczYK1x1PVbxkgZFBV1TmVbcHVztofiGqSKKAuD03c6VuG0uTWRsDoxHtv64jw_GAWUFG0dcJsLrGJOfRU8MGJgZXEXeGhtjfGWsMhgLzA4u4uW_hfZDg95GBeVVFX6EBziT0Ysy)

3.  Selecciona Blank Device y asígnale un nombre.
    
**![](https://lh6.googleusercontent.com/0jKbCRAgxDqgecU9bCEk9qd91u4MU855I8d5UhYMa9DBNUu6VK3V7dfb1d0H2qRyqEF0RHLyOSMELZOCyTeOSftt-RkxA-khksGLGm0zTjQrZ4FGdN5hTPxOCJxZDZFESIWV_TTX)**
![](https://lh5.googleusercontent.com/WSJmO0IJEOTJtpYmBNyi1dmcjNj5xI4NHJtd3OJUHHI-2_Zui6tsf8OmBxFg9KiT13DcGSrFiDwHg_qlSc5BhM_b_vhgedS5R7rdVUSMrNmFZqdAPRaUIPm7r6VCrASU3T_WbeP7)

4.  Confirma la creación de tu dispositivo.
    

  

![](https://lh3.googleusercontent.com/J-fzKrrSGEP5-HuiRvPBYQF3DHkKZ8RCNGJB3-vj-d-Q3JbCnn1pLz1TeSiCK-547Jr0xpPsUpj265eCN8YNvnfTHreHr8u1LSr5VxrHXKSkPdbIJJhAGkYu-pNoqnpbCcOspcKX)

  

5.  Obtener token de acceso. Al hacer click en tu foto de perfil se desplegará el menú de opciones, seleccionar “Api Credentials” y anotar la información del token.
    

  

![](https://lh4.googleusercontent.com/_mtVvzgCouEHxXMXIcPPiiAs17sNRYfGbXAmturD1epiwqB5GTwlzI9gY4Mb_BxQsh5YCRYmmGl4kELlHO9pOhytjw5Yz0piyYyFl1zGR90w12DGHgC6_-uT27t2UgXSoc465lS1)

![](https://lh6.googleusercontent.com/Rd8L9GwLIB3NEs_-eEfOkFpQi2Ms8-qOnxXTyepofqYyBbsjNxlWk769QI-2lvMMajwV1cVmzbgYvrHEq6pNsdbJ4m4WyvqUCnKjXFZaPFQG90-JEAZ7TtMKrdIke5kp5xpMyfRY)

  

6.  Añade los nodos de function, ubidots-out, switch y conectalos de la siguiente manera:
    

![](https://lh3.googleusercontent.com/pAGZCeEvyO_ni6dsBdwkmmBbRrB-2wJsJPyMTgcL8aBh83newowZMIfoKiGiGNFCAgbTKrjlfuXONRvltzmgPYMPm0U2dCWoGn5sVEjlFDOQMCdn-tJziEqP9UH0ybVFYRv5llmf)

  

> El nodo switch se conectará más adelante.
> 
>   
> 
> Function: Permite escribir una función JavaScript para modificar mensajes.
> 
>   
> 
> Switch: Envía la información por diferentes canales dependiendo las condiciones definidas.
> 
>   
> 
> Ubidots-Out: Se encarga de mandar la información al backend de  Ubidots.

  

7.  Accede al nodo Ubidots out y configurarlo con su información correspondiente.
    

  

> Configurar los campos de la siguiente manera:

![](https://lh4.googleusercontent.com/m7YPq01NYBz7NGXdi1xkWUiLphWmfNEzcClO7HKzmV9t6j72EcYCCLLK0HeHGNGwKOtm7ZUbp5GsEmUZF3NJC8o3ZGiU3JDDNgJfjgnPe-GjojKT9Giz4O1QprFWFhO17r-qJkqx)

> Account Type: Ubidots for Education.
> 
>   
> 
> Name: Nombre del nodo, puede ser el que guste.
> 
>   
> 
> Token: Credencial de token previamente anotada.
> 
>   
> 
> Device Label: Nombre del dispositivo registrado en Ubidots.
> 
>   
> 
> Ubidots espera un mensaje con un formato específico, por lo que es necesario utilizar una función para modificar la información, la cual debe contar con esta forma:

 

    {
    
    "device_label": “Nombre de tu dispositivo”,
    
    "payload": {"Nombre de tu variable": "Valor de tu variable"}
    
    }

> Se deben modificar la sección nombre de dispositivo, nombre de variable y valor de tu variable, dependiendo de los nombres que les hayas asignado.

8.  Accede al primer nodo de función y escribe el siguiente código:
    

  

![](https://lh4.googleusercontent.com/b1q4g772aIszuysLiUjmM7EMU0Df5YAjAMpZnI2zrySyq9UJCYXSjSAkrbNJFYjlJ1pJIwQ5HPhMARyjGMpfvc9EiwvGxa8CDAXY_YtzaSkBlu2RLEr4yFY6qGgbaU2taAYPaxXj)

    msg ={
    
    "device_label": "windows",
    
    "payload": {"CPU LOAD": msg.payload}
    
    }
    
    return msg

  
  
  
  
  

9.  Accede al segundo bloque de función y escribe el siguiente código:
    

![](https://lh6.googleusercontent.com/0jezMScFCzXii4CxnO5miKVMlN8LhLAXRg0VPYFVcTsDBNmM3_0ctq8BMmgt-mO7wW6lpWVbvMjQwACnLv2Y3pwkGdeVl8OHKuXfcDyFHluUL3kQXKBxidChhHVEo4AauOgffnmC)

    msg ={
    
    "device_label": "windows",
    
    "payload": {"ADVERTENCIA": 1}
    
    }
    
    return msg

  

10.  Accede al tercer bloque de función y escribe el siguiente código:
    

![](https://lh5.googleusercontent.com/JOkyyL4ic9HlQYvhA0wvdB8kgKB3RYzk6I-8Scm1f5XDiPwWTXrTDMbVEzMhPtYVjhXX_QJi1D4ifFtLmvSVLfjtfAP7t8keECx8sPuWBqmzIPwJ23IUhIrdrJuZjeOteOnlboED)

    msg ={
    
    "device_label": "windows",
    
    "payload": {"ADVERTENCIA": 0}
    
    }
    
    return msg

  

> La primera función se encarga de enviar la información del uso del procesador, mientras que las otras 2 sirven como advertencia para indicar una carga normal o alta (normal = 0, alta=1), por lo que es necesario tener un selector, para esto se utiliza el nodo de switch.

  

11.  Accede al nodo switch y configura los valores mínimos y máximos de carga del procesador, es importante conocer a qué porcentaje se encuentra trabajando tu procesador en este momento, así podrás establecer un rango correcto para esta prueba.
    

> Utiliza el Administrador de Tareas para conocer el porcentaje de uso de tu procesador.

![](https://lh3.googleusercontent.com/LEbQiVD7WYlvLO4HeLCCbZ2rFtsDXNs2_Ytso6yhTRqJdaxIxKjoBK2KuAFEWsDS80bUMXBJeCS481SErDh-C9Jy70fJ4QXW4obskARD7ba420Hj3ooGZcMlmw0DQQNYpXb_Ooqe)


![](https://lh6.googleusercontent.com/2cAuu3AeD8g6d5WhrdZp_JQqMt0Og6ju7d_AyEkAxAmKsntwdyL6CJafl5MtSvIOa0MFk5vubs0ErSVGg6In11pQBRiWzky2kLNG-putXXFZYP-P0HYiBriGJtBVy4EjOMtIggku)

> Para este caso en particular el procesador se encuentra variando entre 4% y 10%, por lo que para esta prueba cualquier porcentaje por debajo del 5% será considerado como normal y arriba de 6% como una sobrecarga.

![](https://lh6.googleusercontent.com/aLbOXM-sRiXitrUkOa6_B4nWpiz1kiKcO5PTv7naImndp22QYmWmknx39m3Pz0GF6pX5uyWNhDth1anVvjxUPHEH0fLTJ-DUkIrkdzHTzOu9Xbb3RdV7J2jPPmE1wswK-KRT3NFy)

  

> Esto causará que el nodo switch cuente con dos salidas, las cuales deben conectarse de la siguiente manera:

  

![](https://lh6.googleusercontent.com/NwiKPZpj97pwnNTiCBlvV7-JBg6qET6U-GyKnzAvnjm7DCvVjNRFvK30JKoCbqzVdfYrVZU1D6rRH7E7yBuKzdcIMJD1tflUktbPQVVSDqFS8ML-XbNiT04veFpk0SZJPWZ1MTJO)

  

12.  Da click en el botón de Deploy.
    

![](https://lh3.googleusercontent.com/f8F_G-ne49RydErdTBD2zbdEP4__raLBqoRXd572TQdRh4psZket6B8Kg88BKI4SYVrkp67SzRYOTsgdTmQ29u0dorOP5ug6xoF5YM3CfEbwcUOaVul1Qc3U8XFsNKbSDFbNpFsV)

13.  Da click en el botón de timestamp y accede a tu dispositivo en Ubidots, la información se habrá actualizado.
    

![](https://lh6.googleusercontent.com/_iXJRfTjnYDKy7zgaKZAwnYuv6kNq46bsVV351spl04Gqqu8YduF4FasI_4TIcNHWhdtwb6Twrj3QqanKCJu1Cv2oEC7h87uRbiVHvMfv65844o9wOgZc6WtQZEy21wP7goGCFlX)

### Configuración de widgets:

  

1.  En la parte de Data, accede a la sección de Dashboards y da click en el símbolo de +, selecciona Gauge para crear un nuevo widget.
    

  

![](https://lh4.googleusercontent.com/bNVOAva6PT5HX_CqCGYcODzqItMH_broow_lgvcDnhMtKI90nbUmvZQCbSPqGKKCkgjszu7uqICplGM6hpFnSqF2j0ew5-hcSs2cxYU5YJd2Gx1pp1u-Bww7CmpK41-9-K__k__d)

  

![](https://lh4.googleusercontent.com/P1jG895FFbWcRfrT0MjdVPdDx2MEyCOSgcg82pDwjUVr7oU284jI8ooALybKKDiRJBB3IKex03NRoLv73hDfZ8W7g6vhpp7oZt0cx7KyizRr-E4VLSPE53pV8OsygFtEds5SkPwS)

2.  En la sección de Gauge, hacer click en “add variable”.
    

![](https://lh4.googleusercontent.com/Xcns-3eBco8YKp8aVGU0khn2BVG7_2FNpQ6B85mb60PgiiMYAQM1CwtODU_zxw_UVQdmGfPXSL-ibcJfKY3kuVi5qgXPv5xoPNqw6Uu7yNBJKO69lP9Ooa89-0OtFBx_kwT6azT5)

Selecciona tu dispositivo y la variable cpu-load, confirma la selección.

  

![](https://lh5.googleusercontent.com/nXMGfBJOC69cAcu2hmpd9Iwf_qNtYOjst08sTgUS4gkgjA7lc2ChlZLPQj09wih_5fW83Xf65raTBVe5izxt9S82OFtLCPr4u3HfurllN930iLValien5npowsvOXq_qIoyfhuyM)

> Modifica su nombre y confirma su configuración.

  

![](https://lh5.googleusercontent.com/SaHQGGOTLZtA_gWcpbTUWma2WnUwq-McevKYHFJst3B-OzWsqdUZC7RixsV6I5Ra_pOY1jxOkj_Dnri84dw10qXePAXPbTQEMy_ASzTzAElxX2ywgUSzXjZBHzhmHSSwulnsaZ3W)

  

> Se obtendrá el siguiente widget:

**![](https://lh5.googleusercontent.com/AbiZ3NW2APn_VdTePETgjfYmz8PX0MY3REEYXDdKJTdpMYkqHgD9ApG2eC22Zl-4Q3rnvuE-QBQl43C6hmCqpKuIqXL98Ael-UvFbKrsDHBplSE-Ibb6d0z1j1Ksexohz8qKFghE)**

3.  Crea otro widget del tipo indicator y añade la variable de advertencia.
    

![](https://lh6.googleusercontent.com/A-58weT1tHNMrhQtZ8xM1erGgkpmUmUvMIEFukHdeRalRaFzGoeoI6jggimcKJc7PQH_G0S0x2SCALSdpEw_rAOQ7HWz054VgMiOplSDN5cODPoBnFIA949da09i_9TASc7o2TuI)

![](https://lh5.googleusercontent.com/ugIrWnmWyoVcj0HI-Fp78WcoDMxf1_xplD8sl4__eTcdVzFaLNkhplKQdmmVmQvi4rIKlCMnqTDVNkmxMKnAEr--t5GYFaFOkbWRlrGy-PmTXzv_5eJizLQLkFhwKeznpSqIT_dE)

  
  
  
  
  

> Selecciona la opción de “Add color logic” y configurarlo de la
> siguiente manera:

  

![](https://lh5.googleusercontent.com/YVaT9Uu2IpgMVq_hf0uC0p7S-7qGNTT5r7ZIKNCnilMfEf6PRt-BNqgzEqlZpRxBwPe26pLnp2sTasUHhAfhx1p3J59ayvGU8e-oRBQY7K1tHsAEklbgKFYAUeaxrdcwbNfdw27N)

> Ahora se cuenta con dos widgets, donde se puede ver la carga del procesador y una advertencia en caso de sobrecarga.

  

![](https://lh5.googleusercontent.com/hEsuP2QnIAY6RllFiHqU9HIjJ9g-nTVHYkpRrwUrZlC-qYfMCqWtHJ8wYOse7y4BYLzjJlt5uJTq_UI-GCYGPpIA8x6mJLlE8eKSf6yja96LiTs5AIGWxch9nuwM3Yg3AFOrdUAg)

  

> Por último se configurará el nodo de timestamp para que cada 10 segundos se actualice la información.

  

4.  En node red accede al nodo timestamp y modifica su configuración de la siguiente manera:
    

![](https://lh5.googleusercontent.com/Z1m8nwasSav9YttZYkKpkOBN_dxOYlsfDjGiqK0lVOPg9dIkjkatJ5bHGSSvGav5PTBczoW8fLypvIcMzmCzh9D9Fd3q1CapQC2m1KllmZ0OsqjnIFsMyoAHY5nkfZmCZN41QqnV)

> Recuerda que puedes modificar los valores en los que quieras indicar una sobrecarga o carga normal, en el nodo switch.

![](https://lh5.googleusercontent.com/EPAI7GYIN_r2dIVwkkbWAsVHj3D3GSFgWvoDRuzjoCsTGf-oQ-pf2tPvIOj1Q4tPJg_ZUGPR9a2bmgd-TvE-D347oG14K1EhSg41MfeqAhBS4SRCcOUYxa8gL4YH7YYpITwIjL-d)

  

> De la misma forma puedes acceder a tu dispositivo en Ubidots y seleccionar cualquier variable para inspeccionar su información.

  

![](https://lh5.googleusercontent.com/rN1QjyzWgv03J-VtehaTJL6EVFRvBnEyCoZrD-7HdaSTv1zI2gu1-tFMz4jwvTys3bhZHbvu0J1HvLjjd1iD8jWrEFU-P5hNALgpKS5MajviqOFGvkSOQ0cVU9JvDXgSf6qtsn3u)
