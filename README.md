# MCOC2020_P2_G0_Entrega5

# Informe

### 1. ¿Cuál fue su diseño inicial? ¿Cuánto pesaba? ¿Cómo eran los factores de utilización y las deformaciones?

En primera instancia, debido a la condición que limita el largo de las barras en el vano del puente a solo 6 metros, se decidió crear barras de de `5 [m]` de longitud. Al ser el primer diseño, se utilizó una estructura similar a la de la entrega 4, pero esta no considero las barras diagonales en la base de la estructura.
El largo de todas las barras se consideró igual, por lo que la altura del puente en primera instancia fue de `H= 4,33 [m]` (*Calculado con el teorema de Pitágoras*). El espesor de las barras y el radio se fijó igual para todas y tuvo un valor inicial de  `t= 5 [mm]` y `R= 8 [cm]`.
A continuación se presenta la estructura del diseño 1, la cual tuvo un peso de `P= 283.837,4099 [N]`.

![Gráfica_1_Estructura](https://user-images.githubusercontent.com/43649125/96386665-fb993d80-1172-11eb-80f8-c6391159d7c5.PNG)

Posteriormente se calcularon las tensiones correspondientes para cada combinación y se graficaron las deformaciones de la estructura. Junto a lo anterior se revisó la viabilidad del diseño con la función `chequear_diseño`. El requisito para aprobar el diseño propuesto debía cumplir:


![CodeCogsEqn](https://user-images.githubusercontent.com/43649125/96386731-72363b00-1173-11eb-94fe-dce5133550ff.gif)

A continuación se presentan los resultados del diseño número 1: 

* 
![Gráfica_1_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96386670-ffc55b00-1172-11eb-92d4-44ba34eae0b5.PNG) 


* 
![Gráfica_1_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96386669-ffc55b00-1172-11eb-901b-e82b571c391b.PNG)

Se observa que el primer diseño realizado no cumple con los requisitos mínimos de diseño. Este, al no ser un diseño viable, generó valores de Factor de Utilización muy superiores a 1 por lo que descartado. El criterio para revisar si efectivamente el diseño iba por buen camino, fue revisar el cumplimiento de las cominaciones de carga y el valor de la deformación.
En un intento por corregir esto, se generó distintos casos en los que se varió uno o mas parametros de la estructura original. Para poder analizar los cambios que generaban en ella.
 
A continuación se presenta una tabla con la variacion de parametros en cada caso:

| Caso | Radio `[cm]`: | Espesor `[mm]` | Altura `[m]` | Largo `[m]` |
|--|--|--|--|--|
| 1 | 8 | 5 | 4,33 | 5 |
| 2 | 15 | 25 | 4,33 | 5 |
| 3 | 15 | 25 | 10 | 5 |
| 4 | 20 | 40 | 20 | 5 |
| 5 | 20 | 40 | 20 | 5,972 |


### Caso 2
Para este caso se aumentó el radio de la barra  a `15 [cm]` y su espesor a `25 [mm]`.

*
![Gráfica_2_Estructura](https://user-images.githubusercontent.com/43649125/96387003-94c95380-1175-11eb-82df-8d859a3645b9.PNG)


*
![Gráfica_2_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96387002-9430bd00-1175-11eb-93de-93ad1e124711.PNG)


* 
![Gráfica_2_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96387001-93982680-1175-11eb-8a51-b60c0875d3ab.PNG)


### Caso 3
Para este caso se aumentó la altura de la estructura a `10 [m]`.

* 
![Gráfica_3_Estructura](https://user-images.githubusercontent.com/43649125/96387058-d823c200-1175-11eb-9255-b3168aaff6f5.PNG)


* 
![Gráfica_3_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96387057-d823c200-1175-11eb-9324-53879f80e430.PNG)


* 
![Gráfica_3_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96387054-d78b2b80-1175-11eb-8a3b-a84ad41c9735.PNG)


### Caso 4
Para este caso se aumentó el radio de la barra  a `20 [cm]`, su espesor a `40 [mm]` y su altura a `20 [m]`.

* 
![Gráfica_4_Estructura](https://user-images.githubusercontent.com/43649125/96387060-e40f8400-1175-11eb-8cd6-145901c7874f.PNG)


* 
![Gráfica_4_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96387062-e540b100-1175-11eb-96f4-8f086f02a4a3.PNG)


* 
![Gráfica_4_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96387061-e4a81a80-1175-11eb-9b75-7f18e9f19e94.PNG)

#### Caso 5
Para este caso se mantuvieron los parámetros iguales que para el caso 4. Sin embargo, el largo de la barra se re calculo dividiendo el largo del puente por 36 (número de barras). El resultado a pesar de ser decimal (*y por ende, no realista con las medidas existentes en el mercado*) no cumplio con los requisitos. Por lo que no hubo que ajustar su valor a las solicitudes de la industria. 

* 
![Gráfica_5_Estructura](https://user-images.githubusercontent.com/43649125/96387288-50d74e00-1177-11eb-8700-1e73d930bd1d.PNG)


* 
![Gráfica_5_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96387290-52087b00-1177-11eb-8a89-251b23377653.PNG)


* 
![Gráfica_5_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96387289-52087b00-1177-11eb-90ab-65a575f8bab5.PNG)




### 2. Para cada cambio informe qué cambios hizo y porqué, y cómo cambia el peso y los factores de utilización. 

Dada la incompetencia del diseño de reticulado, es que se pensó en un diseño completamente distinto. Se creó un puente con arco de altura `H= 33 [m]`. El arco fue construido con un reticulado triangular y de él se originaron “cables” que sostuvieron el vano del puente.

A continuación se presenta el diseño en `autocad` del puente:

![Diseño puente](https://user-images.githubusercontent.com/43649125/96654119-f5d95e80-1310-11eb-8a59-de34d13c171e.png)

Se observa el arco de reticulado de color blanco, los cables que sostendrían cada nodo del vano de color amarillo y los nodos del arco representados en verde.

El diseño original considero todas las barras de igual radio y espesor, de la misma forma que para los cables. Es decir, las barras de la calle, arco y cables se les asignó las mismas medidas. La estructura en su totalidad terminó siendo formada por barras de radio `R= 10 [cm]` y espesor `t= 20 [mm]`. Al correr el primer diseño se obtuvieron los siguientes resultados:

### Caso 6

*
![Gráfica_6_Estructura](https://user-images.githubusercontent.com/43649125/96653787-4d2aff00-1310-11eb-9331-a3ed209d552e.PNG)


*
![Gráfica_6_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653791-50be8600-1310-11eb-89f3-3b7470ca92bc.PNG)


*
![Gráfica_6_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96653796-52884980-1310-11eb-8253-ed374aa76f0f.PNG)


*
![Gráfica_6_FU_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653803-57e59400-1310-11eb-92be-832976639faa.PNG)


*
![Gráfica_6_FU_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96653808-5a47ee00-1310-11eb-9793-597d39c96d92.PNG)


Se puede observar que el diseño no cumplió las combinaciones de carga. Debido a esto los valores de FU no fueron entregados, debido a que en diversas barras este valor superaba el valor limite igual a 1. Es importante recalcar que debido a la cantidad de barras, visualizar el factor se torna engorroso, razon por la que se omitirá su visualizacion hasta cumplir el requisito de los valores menores a 1.

Para el diseño 2 se decidió cambiar las medidas de las barras utilizadas para los cables. Se planteó un radio `R= 2 [cm]` y espesor `t= 20 [mm]`. Los resultados se presentan a continuación.

### Caso 7

*
![Gráfica_7_Estructura](https://user-images.githubusercontent.com/43649125/96653850-6cc22780-1310-11eb-827e-0bce05b845a4.PNG)


*
![Gráfica_7_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653859-6f248180-1310-11eb-9f75-827fd6bffbec.PNG)


*
![Gráfica_7_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96653864-7186db80-1310-11eb-9a0f-a1bbb8e2a73d.PNG)


*
![Gráfica_7_FU_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653871-7481cc00-1310-11eb-8444-6d6a14c4825f.PNG)


*

![Gráfica_7_FU_caso_1 2D+1 6L (1)](https://user-images.githubusercontent.com/43649125/96660821-fa0d7800-1320-11eb-83f4-ab24e76a95b0.PNG)



Se observa que el diseño 2 fue nuevamente insuficiente al momento de cumplir con las condiciones de carga. Los valores de FU tampoco fueron entregados al estar incorrectos.

Buscando optimizar tanto la estructura como las iteraciones para lograr esto, se utilizó la función chequear diseño, y se le agregó un código con la finalidad de que el programa nos entregase un detalle de las barras (en específico el conjunto de nodos que forman una barra) que estaban fallando en cumplir con las combinaciones de carga 1 y 2. 

Gracias a esto se pudo observar que los triángulos del reticulado de ambos bordes del puente estaban siendo muy exigidos al ser las “bases” del arco en el suelo. Se procedió a  rediseñar las barras de ese sector las cuales se dejaron con un radio radio `R= 25 [cm]` y espesor `t= 20 [mm]`.

De la misma forma que en la base del reticulado, se observó que las barras que estaban pensadas como “cables” no estaban siendo de utilidad para sostener el vano del puente, sobre todo al evaluarse la carga viva. Para solucionar esto se decidió abordar la utilidad de los cables y reemplazarlos por barras más concisas. Esto aumentó el peso del puente en comparación con las ideas originales, pero sirvió para cumplir con las condiciones de carga existentes. Observando las barras que no cumplian los requisitos, se observó que los cables diagonales y centrales podían dimensionarse de manera distinta entre sí. 
De acuerdo a lo anterior se rediseñaron los cables y se les asignó un radio de `R= 18 [cm]` y espesor `t= 18 [mm]`para los cables diagonales, y un radio de `R= 20 [cm]` y espesor `t= 20 [mm]`para los cables centrales.

Finalmente estos cambios lograron que el diseño del puente cumpliera con los requisitos, logrando un diseño optimizado. Los resultados se muestran a continuación.

### Caso 8

*
![Gráfica_8_Estructura](https://user-images.githubusercontent.com/43649125/96653973-9ed38980-1310-11eb-825b-6364529bbd29.PNG)


*
![Gráfica_8_Tensiones_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653981-a135e380-1310-11eb-8240-51e527c7a870.PNG)


*
![Gráfica_8_Tensiones_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96653986-a430d400-1310-11eb-86d7-2145375509df.PNG)


*
![Gráfica_8_FU_caso_1 4D](https://user-images.githubusercontent.com/43649125/96653990-a6932e00-1310-11eb-99c7-9eb46d05f07b.PNG)


*
![Gráfica_8_FU_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96653994-a8f58800-1310-11eb-8f49-6e7f2edca862.PNG)


Se adjuntan los valores de FU que cumplen en su totalidad la exigencia de valor limite igual a 1.

*
![Gráfica_8_FU_valores_caso_1 4D](https://user-images.githubusercontent.com/43649125/96654025-b579e080-1310-11eb-8735-9bb73e1750a8.PNG)


*
![Gráfica_8_FU_valores_caso_1 2D+1 6L](https://user-images.githubusercontent.com/43649125/96654027-b874d100-1310-11eb-9724-25009eeef09e.PNG)



