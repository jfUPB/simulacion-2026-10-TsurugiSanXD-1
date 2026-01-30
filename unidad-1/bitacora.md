# Unidad 1

## Bitácora de proceso de aprendizaje

## ***Actividad 1.***

*Aleatoriedad en el arte genartivo:*
La aletoriedad le da un factor de cratividad sorpresa al arte generativo.


## ***Actividad 2.***
**¿Que espero que suceda?**
R\: Con las modificaciones que hice espero que cambie de color a un azul, que en la pantalla se muestre una elipse en vez de un punto y que la elipse suba más de lo que.
<br>
<br>
<br>
***¿Que paso realmente?*** 
R\: Cuando ejecute el codigo casi todo lo que plantee funciono. En vez de un punto tenia una elipse, la elipse si era de color azul, pero lo que me fallo fue el movimiento, dado que la elipse se quedo quieta en el centro. Fue facil de solucinar porque en realidas solo habia pasado que en uno de los condicionales escribí "choise" en vez de "choice", pero cuando corregi la sintaxis ya funciono como yo esperaba.

## ***Codigo***

```java
let walker;

function setup() {
  createCanvas(640, 240);
  walker = new Walker();
  background(255);
}

function draw() {
  walker.step();
  walker.show();
}

class Walker {
  constructor() {
    this.x = width / 2;
    this.y = height / 2;
  }

  show() {
    stroke(100, 150, 255);
    ellipse(this.x, this.y, 4, 4);
  }

  step() {
    const choice = floor(random(5));
    if (choice == 0) {
      this.x++;
    } else if (choice == 1) {
      this.x--;
    } else if (choice == 2) {
      this.y++;
    } else if (choice == 3){
      this.y--;
    } else {
      this.y--;
    }
  }
}
```

## ***Actividad 3.***

1)R:\ La diferencia entre la distribución uniforme y la no uniforme consiste en, que ladistrobucipon uniforme podemos tomarla por así decirlo como igualitaria, dado que todas las variables tendran la misma probabilidad de "creecer" por así decirlo. En cambio la ditribución uniforme no actua igual para todas las variables, habra unas que creceran más rapido que otras, dado que las probabilidades no seran iguales y el mayor crecimiento se vera en en la media de las variables.

## ***Codigo: Modificación traditional random walker donde se favorezca ir a la derecha***

```java
let walker;

function setup() {
  createCanvas(640, 240);
  walker = new Walker();
  background(255);
}

function draw() {
  walker.step();
  walker.show();
}

class Walker {
  constructor() {
    this.x = width / 2;
    this.y = height / 2;
  }

  show() {
    stroke(255, 150, 255);
    ellipse(this.x, this.y, 4, 4);
    fill(100, 150, 255, 255);
  }

  step() {
    const choice = floor(random(5));
    if (choice == 0) {
      this.x++;
    } else if (choice == 1) {
      this.x++;
    } else if (choice == 2) {
      this.y++;
    } else if (choice == 3){
      this.x++;
    } else {
      this.y--;
    }
  }
}
```

## **Actividad 4.**
**Codigo**
```java
let bins = [];
let numBins = 40;

function setup() {
  createCanvas(640, 240);
  background(255);

  // inicializamos el histograma
  for (let i = 0; i < numBins; i++) {
    bins[i] = 0;
  }
}

function draw() {
  background(255);

  // generar un valor con distribución normal
  let x = randomGaussian(width / 2, 60);

  // convertir el valor a un índice del histograma
  let index = floor(map(x, 0, width, 0, numBins));

  if (index >= 0 && index < numBins) {
    bins[index]++;
  }

  // dibujar las barras
  let w = width / numBins;

  for (let i = 0; i < numBins; i++) {
    let h = bins[i];
    fill(120, 150, 255);
    noStroke();
    rect(i * w, height - h, w - 1, h);
  }
}

```
<br>
<br>
<br>
**Link al codigo en p5:** https://editor.p5js.org/luisafer1845/sketches/iffAJJKJs
<br>
<br>
<br>
**Captura de pantalla**
<img width="1919" height="868" alt="image" src="https://github.com/user-attachments/assets/17a45cd0-1e7d-43db-ad28-65b68c775794" />

## **Actividad 7.**

1)R:\ **¿Ques una obra generativa?**
Una obra generativa es basicamente una creación artistica basada en la alatoriedad y el tiempo para producir resultados variables (que no son fijos). En las obras genarativas el artistas en vez de hacer algo fijo, que tenga la misma apariencia crea una serie de instrucciones/normas que seguir para que la obra cambie por si misma, lo cual, hace que la obra nunca sea la misma. Ya que la obra depende de la aleatoriedad esta siempre sera diferente dependiende la acción que el usuario ejecute con ella, la cual la convierte en una experiencia unica siempre. 
<br>
<br>
<br>
2)R:\ **Link al codigo en p5:** https://editor.p5js.org/luisafer1845/sketches/YaxjOJLqG
<br>
<br>
<br>
3)R:\ **Captura de pantalla:**

<img width="1919" height="868" alt="image" src="https://github.com/user-attachments/assets/c4cc5e7b-85ba-4ad0-b73c-87ec4541713c" />
<br>
<br>
<br>
## Bitácora de aplicación 



## Bitácora de reflexión





















