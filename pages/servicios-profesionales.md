---
layout: page
title: Servicios
permalink: /servicios/
weight: 3
---

<p align="center">
<img src="/images/logo_armonizadogs_titulo_t.png">
</p>


# **Servicios profesionales**

<br><br>

<div class="carousel">
  <!-- Slide items -->
    <div class="slides">
        <div class="slide active" id="service-a">
            <h2>Educación canina</h2>
                <br><br>
                <h3>Motivación</h3>
                <br>
                <p>                
Entenderás a tu perro, su naturaleza y necesidades, cómo percibe el mundo y cómo piensa, cómo manifiesta sus emociones... 
                </p>
                <p>
¡No es una persona! 
                </p>
                <p>
Descubre el mundo de tu compañero/a aprendiendo comunicación canina efectiva. Ocupémonos del problemita antes de que se convierta en problemón.
                </p>
                <br>
                <h3>Descripción</h3>
                <br>
                <p>
Formación teórico-práctica a domicilio, es como un curso estructurado de educación canina pero a nivel particular, en tu casa y con tu perro. 
                </p>
                <p>
Aprenderás las bases de la naturaleza canina (físicas, instintivas, cognitivas, emocionales y sociales), a construir vínculo, motivación, concentración y comunicación con tu perro, gestionar correctamente el paseo, el juego, la sociabilización, etc. 
                </p>
                <p>
De esta manera nuestro objetivo es que consigas formar un gran equipo con tu fiel compañero y adquieras los conocimientos y habilidades para guiarle a descubrir lo maravilloso que es vivir y relacionarse en equilibrio y armonía con el entorno y los individuos que conviven en él.             
                </p>                
        </div>
    <div class="slide" id="service-b">        
        <h2>Cachorros</h2>
                <br><br>
                <h3>Motivación</h3>
                <br>
                <p>                
Es la etapa más importante de aprendizaje estructural, sentemos unas buenas bases, gánate su confianza, motívale y oriéntale en su descubrimiento del mundo. 
                </p>
                <p>
¡No cometas el gran error de esperar a que se haga adulto! Actúa.
                </p>
                <br>
                <h3>Descripción</h3>
                <br>
                <p>
Formación teórica básica (y rápida) sobre los cachorros y las características y necesidades de cada una de las etapas hasta que alcanza la adultez.
                </p>
                <p>
Por otro lado desarrollaremos el estudio, entrenamiento, orientación y seguimiento del cachorro para la formación de unas estructuras cognitivas y emocionales sólidas y
equilibradas.
                </p>
                <p>
Pondremos el mayor énfasis en la construcción del vínculo, la motivación, la comunicación y lo emocional (experiencias positivas). 
                </p>
                <p>
Aprenderás a guiarle en una correcta socialización/sociabilización y en los procesos de aprendizaje cognitivo.
                </p>                
    </div>
    <div class="slide" id="service-c">
        <h2>Modificación de conductas</h2>
                <br><br>
                <h3>Motivación</h3>
                <br>
                <p>                
Entenderás las causas reales de los comportamientos no deseados, identificaremos los estados psico-emocionales, los condicionamientos y los aprendizajes diarios que propician las conductas.
Armonízate con tu perro, construye vínculo y forma equipo, sé un buen guía.
                </p>
                <br>
                <h3>Descripción</h3>
                <br>
                <p>
Este es un servicio más delicado, es necesario un trabajo minucioso e hilar muy fino ya que
existen conductas no deseadas (en ocasiones problemas muy serios) y un diagnóstico erróneo o una mala aplicación de la terapia puede tener consecuencias nefastas. Igual de
importante e imprescindible es la voluntad y el compromiso de la persona o personas tutores del perro (familia). De hecho, en Armonizadogs, son los tutores los verdaderos
protagonistas de la terapia y el manejo del perro.
Sin estos dos ingredientes la rehabilitación real y completa es imposible.                
                </p>
                <br>
                <br>
<p style="text-align: left;">
Dicho esto, este servicio se compone de 4 fases:
<br>
- Entrevista inicial (gratuita): primera toma de contacto, cambio de impresiones, presentación de la
metodología y presentación del caso.
<br>
- Diagnóstico: proceso de recogida de información, análisis y elaboración del diagnóstico
<br>
- Reunión de compromiso familiar con la terapia y planificación conjunta: presentación de la
planificación de la terapia, reparto de roles, cambio de impresiones, modificaciones, y compromiso final.
<br>
- Terapia: aplicación y desarrollo de la terapia para la modificación de las conductas no deseadas.
                </p>                
    </div>
  </div>

<!-- Carousel HTML -->
<div class="carousel">
  <div class="slides">
    <div class="label"></div>    
  </div>

  <!-- Slide indicators -->
  <div class="indicators">
    <span class="indicator" onclick="showSlide(0)"></span>
    <span class="indicator" onclick="showSlide(1)"></span>
    <span class="indicator" onclick="showSlide(2)"></span>
  </div>

  <!-- Navigation buttons -->
  <button class="prev" onclick="changeSlide(-1)">&#10094;</button>
  <button class="next" onclick="changeSlide(1)">&#10095;</button>
</div>

<!-- Carousel JavaScript -->
<script>
let currentSlide = 0;
const slidesContainer = document.querySelector('.slides');
const slides = document.querySelectorAll('.slide');
const indicators = document.querySelectorAll('.indicator');
let startX = 0;
let currentTranslate = 0;
let prevTranslate = 0;
const slideTexts = [
  'Educación canina', 
  'Cachorros', 
  'Modificación de conductas'
  ];  // Label for each slide

function updateSlidePosition() {
  slidesContainer.style.transform = `translateX(-${currentSlide * 100}%)`;
  slidesContainer.style.transition = 'transform 0.5s ease-in-out';
  indicators.forEach((indicator, index) => {
    indicator.classList.toggle('active', index === currentSlide);
    console.log("indicator: " + indicator);
    console.log("index: " + index);
  });

  console.log("currentSlide: " + currentSlide);
  
  // Dynamically update the text content based on the current slide index  
  let activeSlideHeader = document.querySelector('div.label');
  let activeSlide = document.querySelector('div.label');
  activeSlide.textContent = slideTexts[currentSlide];  
}

function showSlide(n) {
  currentSlide = n;
  updateSlidePosition();
}

function changeSlide(direction) {
  currentSlide += direction;
  if (currentSlide >= slides.length) currentSlide = 0;
  if (currentSlide < 0) currentSlide = slides.length - 1;
  updateSlidePosition();
}

// Touch events for swiping
slidesContainer.addEventListener('touchstart', (e) => {
  startX = e.touches[0].clientX;
  slidesContainer.style.transition = 'none';
});

slidesContainer.addEventListener('touchmove', (e) => {
  const currentX = e.touches[0].clientX;
  currentTranslate = prevTranslate + currentX - startX;
  slidesContainer.style.transform = `translateX(${currentTranslate}px)`;
});

slidesContainer.addEventListener('touchend', () => {
  const movedBy = currentTranslate - prevTranslate;
  if (movedBy < -50) changeSlide(1);
  else if (movedBy > 50) changeSlide(-1);
  else updateSlidePosition();
  prevTranslate = -currentSlide * slides[0].offsetWidth;
});

// Initialize the first slide
updateSlidePosition();

</script>