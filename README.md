# triviadospuntouno 
Trivia
# HOLA✨🦄 bienvenidxs a la trivia dos punto uno!

Esta es una página básica HTML en conjunto con JavaScript y CSS que en conjunto se verán reflejados como un sitio web interactivo y con estilo para que el usuario pueda responder una trivia.

_Última actualización: 24 Ago 2023_

## De qué trata nuestro proyecto?

Trata del juego de una trivia. Se solicita el nombre del participante y enviamos un saludo invitándolo a jugar
Se le plantean tres preguntas referentes al significado palabras en tres diferentes países. El juagdor debe 
elegir una opción y presionar el botón para validar su respuesta, mostrando el sistema una pantalla en la que 
le informa si su opción fue correcta o no.

← `README.md`: Aquí es donde estás en estos momentos, explicamos de que trata nuestro proyecto y también adjuntamos el código de HTML, JavaScript y CSS.

← `index.html`: El HTML será la estructura y contenido de la página de Trivia2punto1 donde al juntar con JavaScript y CSS el usuario podrá interactuar para ingresar el nombre y luego ingresar al juego de la Trivia.

← `comenzar.html`: El HTML es la página de las preguntas interactivas

← `style.css`: Agregamos estilo a los elementos de nuestro HTML gracias al archivo CSS. 

← `script.js`: Java nos ayuda a agregar interacción y funcionalidad al sitio web. 


Aquí abajo agregamos nuestro código.

## Código - Nuestra página principal 🏗️ (index.html)

Página principal o de ingreso para jugar la trivia`index.html` ...

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" href="/style.css" />
    <script src="/script.js" defer></script>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    
     <title>¿Cómo me llamo?</title>
       <h2 class="encabezado" style="text-align:center">Trivia</h2>
 </head>
  
  <body>
      <br>
      <div class="wrapper">
      <div class="content" role="main">
        <h1 class="title" style="text-align:center"> ¿Cómo me llamo en tu país?</h1>
      </div> </div>
      <br>

            center><p>¡HOLA! ¿Cuál es tu nombre?</p>    
    
        <input type="text" class="txt-nombre">
        <input type="Submit" class="boton-Ir"> 
        <br><br></center>
    
    <div class="mostrar">

    <center><button id="comenzar">Comenzar trivia</button>
    </center>
    </div>
       
    <footer class="footer">
      <div class="links"></div>
      
    </footer>        
  </body>
</html>
```

## Código - Página secundaria o de preguntas de la trivia🏗️ (comenzar.html)

Página de preguntas y respuestas de la trivia donde el usuario va a interactuar `comenzar.html` ...
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="/style.css" />
    <script src="/script.js" defer></script>
    
       <title>¿Cómo me llamo?</title>
        <h2 class="encabezado" style="text-align:center">Trivia</h2>   
  </head>

  <body>
        
     <div class="wrapper">
        <div class="content" role="main">
        <h1 class="title" style="text-align:center"> ¿Cómo me llamo en tu país?</h1>
        </div>
  
      <fieldset>
      <legend>RETO 1</legend>
       <div>
       <h2 style="color:black;text-align:left;">1. ¿Cómo se llama este objeto en Chile?</h2> 
         
         <!--incorpora una imagen que va a alinear al centro-->
         <center><img         
          src="https://cdn.glitch.global/70cd08c7-a55d-4144-994b-e717f2a6c9fe/vecteezy_hair-clip_1202556.png?v=1692675466895"
          class="illustration"
          alt="Editor illustration"
          title="Click the image!"
         > <!cierra imagen-->
        </center>
        </div>
      
     <!-- estamos diciendo que los círculos se alineen a la izquierda -->
       <p style="text-align:left;">
          <input type="radio" name="GpoPinche" value="pinza"> <label>Pinza</label>
          <br>
          <input type="radio" name="GpoPinche" value="pinche"> <label>Pinche</label>
          <br>
          <input type="radio" name="GpoPinche" value="broche"> <label>Broche</label>
          <br>   
       </p>
          <button onclick="respuesta1();">Validar respuesta</button>
          <div class="instructions"></div>
       
      </fieldset>   
    
      <div class="wrapper">  
       <fieldset>
       <legend>RETO 2</legend>
        <div>
        <h2 style="color:black;text-align:left;">2. ¿En qué país le dice guagua a los bebés?</h2> 
  
         <center><img         
          src="https://cdn.glitch.global/70cd08c7-a55d-4144-994b-e717f2a6c9fe/guagua.png?v=1692805843385"
          class="illustration"
          alt="Editor illustration"
          title="Click the image!"
         > <!--cierra imagen-->
         </center>
     
        </div>
        <p style="text-align:left;">
        
          <input type="radio" name="GpoGuagua" value="méxico"> <label>México</label>
          <br>
          <input type="radio" name="GpoGuagua" value="panamá"> <label>Panamá</label>
          <br>
          <input type="radio" name="GpoGuagua" value="chile"> <label>Chile</label>
          <br>
         
        </p>
      
         <button id="respuesta2();">Enviar</button>
         <div class="instructions"></div>
        
      </fieldset>
    
      <fieldset>
      <legend>RETO 3</legend>
       
        <div>
        <h2 style="color:black;text-align:left;">3. ¿A qué se refiere el término "patas negras"?</h2>         
        </div>
      
          <p style="text-align:left;">
            <input type="radio" name="GpoPatas" value="uvas"> <label>A la persona que trabaja pisando las uvas.
</label>
            <br>
            <input type="radio" name="GpoPatas" value="amante"> <label>Persona que es infiel a su pareja actual.</label>
            <br>
            <input type="radio" name="GpoPatas" value="sucio"> <label>Persona que no se lava los pies.</label>
            <br>
         
          </p>
      
             <button id="respuesta3();">Enviar</button>
             <div class="instructions"></div>
        
          </fieldset>
    
      <footer class="footer">
      <div class="links"></div>
      <a
        class="btn--remix"
        target="_top"
        href="https://trivia2punto1.glitch.me/"
      >
        <img
          src="https://laboratoria.la"
          alt=""
        />
       Volver
      </a>    
      </footer>
      
  </body>
</html>
```

## Código - JavaScripta 🏗️ (script.js)

Funcionalidad para el diseño que hemos construido en html `script.js` ...

```
      function Bienvenida (){
      const nombre = document.querySelector(".txt-nombre").value;
          
      alert(`¡Hola ${nombre} vamos a jugar!` );
      document.getElementsByClassName('mostrar')[0].style.display="block";
      }
        
      const btn = document.querySelector(".boton-Ir");
      btn.addEventListener("click",Bienvenida);
 

      document.getElementById('comenzar').addEventListener('click', function() {
      window.location.href = 'comenzar.html';
      
      });
      
      function respuesta1(){
      let elementoActivo = document.querySelector('input[name="GpoPinche"]:checked');
      if(elementoActivo.value=='pinche') {
        alert('Respuesta Correcta');
      } else {
        alert('Respuesta Incorrecta');
      }};
      
      function respuesta2(){
      let elementoActivo2 = document.querySelector('input[name="GpoGuagua"]:checked');
      if(elementoActivo2.value=='chile') {
        alert('Respuesta Correcta');
      } else {
        alert('Respuesta Incorrecta');
      }};
      
      function respuesta3(){
      let elementoActivo3 = document.querySelector('input[name="GpoPatas"]:checked');
      if(elementoActivo3.value=='amante') {
        alert('Respuesta Correcta');
      } else {
        alert('Respuesta Incorrecta');
      }};

```

## Código - CSS 🏗️ (style.css)

Aquí es donde  dimos estilo y color para que nuestro sitio tenga la apariencia deseada `style.js` ...

```
:root {
  --color-bg: #69F7BE;
  --color-text-main: #000000;
  --color-primary: #FFFF00;
  --wrapper-height: 70vh;
  --image-max-width: 300px;
  --image-margin: 3rem;
  --font-family: "HK Grotesk";
  --font-family-header: "HK Grotesk";
}

* {
  box-sizing: border-box;
}
[hidden] {
  display: none !important;
}

@font-face {
  font-family: HK Grotesk;
  src: url("https://cdn.glitch.me/605e2a51-d45f-4d87-a285-9410ad350515%2FHKGrotesk-Regular.otf?v=1603136326027")
    format("opentype");
}
@font-face {
  font-family: HK Grotesk;
  font-weight: bold;
  src: url("https://cdn.glitch.me/605e2a51-d45f-4d87-a285-9410ad350515%2FHKGrotesk-Bold.otf?v=1603136323437")
    format("opentype");
}

.btn--remix {
  font-family: HK Grotesk;
  padding: 0.75rem 1rem;
  font-size: 1.1rem;
  line-height: 1rem;
  font-weight: 500;
  height: 2.75rem;
  align-items: center;
  cursor: pointer;
  background: #FFFFFF;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  text-decoration: none;
  color: #000;
  white-space: nowrap;
  margin-left: auto;
}
.btn--remix img {
  margin-right: 0.5rem;
}
.btn--remix:hover {
  background-color: #D0FFF1;
}

.footer {
  display: flex;
  justify-content: space-between;
  margin: 1rem auto 0;
  padding: 1rem 0 0.75rem 0;
  width: 100%;
  flex-wrap: wrap;
  border-top: 4px solid #fff;
}

.footer a:not(.btn--remix):link,
a:not(.btn--remix):visited {
  font-family: HK Grotesk;
  font-style: normal;
  font-weight: normal;
  font-size: 1.1rem;
  color: #000;
  text-decoration: none;
  border-style: none;
}
.footer a:hover {
  background: var(--color-primary);
}

.footer .links {
  padding: 0.5rem 1rem 1.5rem;
  white-space: nowrap;
}

.divider {
  padding: 0 1rem;
}

body {
  font-family: HK Grotesk;
  background-color: #afcdc9;
}

.wrapper {
  min-height: 50%;
  display: grid;
  place-items: center;
  margin: 0 1rem;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.title {
  color: white;
  font-family: ALGERIAN;
  font-style: normal;
  font-weight: bold;
  font-size: 50px;
  line-height: 105%;
  margin: 0;
}

.encabezado {
  color: YELLOW;
  font-family: ALGERIAN;
  font-style: normal;
  font-weight: bold;
  font-size: 70px;
  line-height: 105%;
  margin: 0;
}

.illustration {
  max-width: 25%;
  max-height: var(--image-max-width);
  margin-top: var(--image-margin);
  }

.instructions {
  margin: 1rem auto 0;
}

button,
input {
  font-family: inherit;
  font-size: 100%;
  background: #FFFFFF;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 6px;
  padding: 0.5rem 1rem;
  transition: 500ms;
}

h2 {
  color: #6a5acd;
}

.illustration:active {
  transform: translateY(20px);
}

.dipped {
  transform: translateY(20px);
}

.fileopener {
  cursor:pointer;
  font-weight:bold;
  border-bottom:3px solid var(--color-primary);
  color: var(--color-secondary);
}
.fileopener:hover {
  border-bottom:3px solid var(--color-secondary);  
}

.mostrar {
  display:none;  
  }

```
<link rel="trivia2punto1" href="https://trivia2punto1.glitch.me/" />
## Ha sido construido en Glitch!


<link rel="canonical" href="https://glitch-hello-website.glitch.me/" />
<meta name="description" content="A simple website, built with Glitch. Remix it to get your own."/>
<meta name="robots" content="index,follow" />
<meta property="og:title" content="Hello World!" />
<meta property="og:type" content="article" />
<meta property="og:url" content="https://glitch-hello-website.glitch.me/" />
<meta property="og:description" content="A simple website, built with Glitch. Remix it to get your own."/>
<meta property="og:image" content="https://cdn.glitch.com/605e2a51-d45f-4d87-a285-9410ad350515%2Fhello-website-social.png?v=1616712748147"/>
<meta name="twitter:card" content="summary" />
```

