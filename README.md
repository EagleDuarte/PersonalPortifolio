# PersonalPortifolio
Welcome to my personal portifolio projects. 
https://personal-portifolio-x7hq.vercel.app/

Design Updated.
![portifolioupdate](https://user-images.githubusercontent.com/107157839/194735906-625a4387-e913-40a4-b882-e2fcfdb7b94b.png)

https://finished-fullvibe-site-main.vercel.app/

https://reactcalcularjs.vercel.app/

http://github.com/EagleDuarte/GrowNotesTS

http://github.com/EagleDuarte/DoctorStrange


    <section class="portfolio" id="confecçoes">
      <div class="main-text">
        <h2 style="color: rgb(137, 26, 170);">Portfolio</h2>
        <h4>Some of My Main Recent Projects</h4>
        <br>
        <hr>
      </div>
    
      <div class="portfolio-content">
        <div class="slideshow-container">
          <div class="mySlides">
            <img src="img/superarshirt.jpg" />
          </div>
      
          <div class="mySlides">
            <img src="img/digitalizalayout.png" />
          </div>
      
          <div class="mySlides">
            <img src="img/batismolayout.png" />
          </div>
      
          <div class="mySlides">
            <img src="img/batismo2.jpg" />
          </div>
      
          <div class="mySlides">
            <img src="img/moletomlarankalay.png" />
          </div>
      
          <div class="mySlides">
            <img src="img/conffecoes.jpg" />
          </div>
        </div>
      
        <div class="image-container">
          <a class="prev" onclick="plusSlides(-1)" role="button" aria-label="Slide anterior">&#10094;</a>
          <img src="img/superarshirt.jpg" class="thumbnail" onclick="currentSlide(1)" role="button" aria-label="Foto 1" />
          <img src="img/digitalizalayout.png" class="thumbnail" onclick="currentSlide(2)" role="button" aria-label="Foto 2" />
          <img src="img/batismolayout.png" class="thumbnail" onclick="currentSlide(3)" role="button" aria-label="Foto 3" />
          <img src="img/batismo2.jpg" class="thumbnail" onclick="currentSlide(4)" role="button" aria-label="Foto 4" />
          <img src="img/moletomlarankalay.png" class="thumbnail" onclick="currentSlide(5)" role="button" aria-label="Foto 5" />
          <img src="img/conffecoes.jpg" class="thumbnail" onclick="currentSlide(6)" role="button" aria-label="Foto 6" />
          <a class="next" onclick="plusSlides(1)" role="button" aria-label="Próximo slide">&#10095;</a>
        </div>
      </div>
    </section>
    
    <script>
      var slideIndex = 1;
      var timer;
    
      showSlides(slideIndex);
      startAutoSlide();
    
      function plusSlides(n) {
        stopAutoSlide();
        showSlides((slideIndex += n));
      }
    
      function currentSlide(n) {
        stopAutoSlide();
        showSlides((slideIndex = n));
      }
    
      function showSlides(n) {
        var i;
        var slides = document.getElementsByClassName("mySlides");
        var thumbnails = document.getElementsByClassName("thumbnail");
        if (n > slides.length) {
          slideIndex = 1;
        }
        if (n < 1) {
          slideIndex = slides.length;
        }
        for (i = 0; i < slides.length; i++) {
          slides[i].style.display = "none";
        }
        for (i = 0; i < thumbnails.length; i++) {
          thumbnails[i].className = thumbnails[i].className.replace(" active", "");
        }
        slides[slideIndex - 1].style.display = "block";
        thumbnails[slideIndex - 1].className += " active";
        startAutoSlide();
      }
    
      function startAutoSlide() {
        timer = setTimeout(function() {
          plusSlides(1);
        }, 3000);
      }
    
      function stopAutoSlide() {
        clearTimeout(timer);
      }
    </script>
    
    <style>
      .portfolio-content {
        display: flex;
        flex-direction: column;
        align-items: center;
        position: relative;
      }
    
      .slideshow-container {
        width: 100%;
        max-width: 800px;
        position: relative;
        margin: auto;
        overflow: hidden;
      }
    
      .mySlides {
       display: none;
       text-align: center;
       height: 500px; /* Defina a altura desejada */
       overflow: hidden; /* Adicione esta linha para ocultar qualquer parte da imagem que exceda a altura */
     }
    
      .mySlides img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    
      .image-container {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 20px;
      }
    
      .thumbnail {
        width: 60px;
        height: 60px;
        object-fit: cover;
        margin: 0 10px;
        cursor: pointer;
        border: 2px solid transparent;
        transition: border-color 0.3s ease;
      }
    
      .thumbnail:hover {
        border-color: #363636;
      }
    
      .thumbnail.active {
        border-color: #363636;
      }
    
      .prev,
      .next {
        width: 50px;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background-color: rgba(0, 0, 0, 0.8);
        color: white;
        font-size: 24px;
        border-radius: 50%;
        cursor: pointer;
        transition: background-color 0.3s ease;
        z-index: 1;
        touch-action: manipulation; /* Adicionado para melhorar a resposta ao toque em dispositivos touchscreen */
  
      }
    
      .prev:hover,
      .next:hover {
        background-color: rgba(0, 0, 0, 1);
      }
    
      .prev {
        left: 10px;
      }
    
      .next {
        right: 10px;
      }
    
      /* Adicionando o tamanho padrão de 1200x675 para as imagens */
      img {
        width: 1200px;
        height: 675px;
      }
    
      @media screen and (max-width: 767px) {
        .slideshow-container {
          max-width: 100%;
        }
    
        .thumbnail {
          width: 40px;
          height: 40px;
        }
    
        .prev,
        .next {
          font-size: 20px;
          width: 40px;
          height: 40px;
        }
      }
    </style>