<html>
    <head>
        <title>Academia</title>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="css/estilo.css">
        <script src="js/menu.js" defer></script>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.2/css/all.min.css" integrity="sha512-1sCRPdkRXhBV2PBLUdRb4tMg1w2YPf37qatUFeS7zlBy7jJI8Lf4VHwWfZZfpXtYSLy85pkm9GaYVYMfw5BC1A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    </head>

    <body>
      
        <header id="header">
            <div id="logo"> <img src="img/logo.png"> </div>

            <nav id="navbar">

                <button id="btt_mobile">
                    Menu
                    <span id="icone"></span>
                </button>

                <ul id="menu">
                    <li> <a href=""> Seja um franqueado </a> </li>
                    <li> <a href=""> Academias </a> </li>
                    <li> <a href=""> Espaço do cliente </a> </li>
                </ul>
            </nav>
        </header>

        <div class="carrossel">

            <!-- Slides do carrossel -->
            <div class="slide">
                <div class="pag"> 1 / 3 </div>
                <img src="img/academia.jpg">  
                <div class="desc"> Academia </div>
            </div>

            <div class="slide">
                <div class="pag"> 2 / 3 </div>
                <img src="img/alimento.jpg">
                <div class="desc"> Dicas de alimentação </div>
            </div>

            <div class="slide">
                <div class="pag"> 3 / 3 </div>
                <img src="img/whey.png">
                <div class="desc"> Produtos </div>
            </div>

            <!-- Botões do carrossel -->
            <a href="#" class="prev" onclick="next_slide(-1);"> &#10094; </a>
            <a href="#" class="next" onclick="next_slide(1);"> &#10095; </a>

            <!-- Indicador de posição no carrossel -->
            <div class="dots_box">
                <span class="dot" onclick="current_slide(1);"></span>
                <span class="dot" onclick="current_slide(2);"></span>
                <span class="dot" onclick="current_slide(3);"></span>
            </div>

        </div>

        <div class="texto">
            <h1>Planos</h1>
        </div>
       
            <img src="img/tabela.png">
        
        <div class="caixa">
            <div class="texto"><h1>Comentários</h1></div>
            <img src="img/depoimento1.png">
            <img src="img/depoimento2.png">
        </div>
            <span>
                <input type="submit" value="Comece agora!" id="btt"/><br>
            </span>

        <div class="rodape">
            <img src="img/logo.png">
            <h2> Siga a nossa Academia </h2>
            <p>Contato: academia@gmail.com</p>
            <p>Telefone: XXXX-XXXX</p>
            <p>Academia - 2022</p>
        </div>
    </body>
</html>

//css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap');

:root{
    --bg_navbar: rgb(163, 163, 163);
    --c_font_light: #f2f2f2;
    --c_hover: rgb(190, 190, 190);
    --rodape: #dfdddd;
    --c_hover_cont: rgb(121, 121, 121);
    --bg_btt: black;
    --bg_pag: rgba(0, 0, 0, 0.336);
    --c_font_white: white;
    --bg_btt_hover: rgb(212, 63, 63);
    --bg_dot: grey;
}

body{
    font-family: 'Roboto', sans-serif;
    margin: 0px;
    padding: 0px;
    background-color: #fdfcfc;
}

ul{
    padding: 0px;
    margin: 0px;
    list-style: none;
}

a{
    text-decoration: none;
    color: var(--c_font);
}

a:hover{
    background: var(--c_hover);
}

#logo{
    font-size: 1.5rem;
    font-weight: bold;
}

#header{
    /* mantem a altura em pixels */
    box-sizing: border-box;
    height: 60px;
    padding: 1rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--bg_navbar);
}

#menu{
    display: flex;
    gap: 0.5rem;
}

#menu a{
    display: block;
    padding: 0.5rem;
}

#btt_mobile{
    display: none;
}

@media (max-width: 600px){

    #menu{
        display: block;
        position: absolute;
        width: 100%;
        top: 60px;
        right: 0px;
        background-color: var(--bg_navbar);
        height: 0px;
        transition: 0.6s;
        z-index: 1000;
        visibility: hidden;
        overflow-y: hidden;
    }

    #menu a{
        text-align: center;
        padding: 1rem;
        margin: 1rem;
        border-bottom: 2px solid var(--c_border);
    }

    #navbar.active #menu{
        height: calc(100vh - 60px);
        visibility: visible;
        overflow-y: auto;
    }

    #btt_mobile{
        display: flex;
        padding: 0.5rem 1rem;
        font-size: 1rem;
        border: none;
        background: none;
        cursor: pointer;
        gap: 0.5rem;
    }

    #icone{
        width: 20px;
        border-top: 2px solid;
    }

    #icone::after, #icone::before{
        content: '';
        display: block;
        width: 20px;
        height: 2px;
        background-color: currentColor;
        margin-top: 5px;
        transition: 0.3s;
        position: relative;
    }

    #navbar.active #icone{
        border-top-color: transparent;
    }

    #navbar.active #icone::after{
        transform: rotate(-135deg);
        top: -7px;
    }

    #navbar.active #icone::before{
        transform: rotate(135deg);
    }

    .carrossel{
        position: relative;
        width: 500px;
        margin: auto;
        padding-top: 10px;
    }

    #btt{
        height: 40px;
        width: 100px;
    }
}

#logo img{
    width: 250px;
    height: 98px;
}

    .carrossel{
        position: relative;
        width: 700px;
        margin: auto;
        padding-top: 10px;
    }

img{
    width: 100%;
}

.prev, .next{
    color: var(--c_font_white);
    position: absolute;
    top: 50%;
    width: auto;
    padding: 10px;
    /* margin-top: -22px; */
    transform: translate(0, -50%);
    font-size: 25px;
    font-weight: bold;
    background-color: var(--bg_btt);
    text-decoration: none;
    transition: 0.3s;
}

.next{
    right: 0;
}

.prev:hover, .next:hover{
    transition: 0.3s;
    background-color: var(--bg_btt_hover);
}

.pag, .desc{
    color: var(--c_font_white);
    background-color: var(--bg_pag);
    font-size: 18px;
}

.pag{
    padding: 8px 14px;
    position: absolute;
    top: 0;
}

.desc{
    /* padding: 5px; */
    position: absolute;
    bottom: 30px;
    width: 100%;
    text-align: center;
}

.dots_box{
    text-align: center;
    margin-top: 10px;
}

.dot{
    cursor: pointer;
    width: 15px;
    height: 15px;
    margin: 0px 2px;
    background-color: var(--bg_dot);
    border-radius: 50%;
    display: inline-block;
}

.rodape{
    text-align: center;
    background-color:  var(--rodape);
}

.rodape img{
    width: 230px;
    height: 90px;
}

.rodape p{
    font-size: 18px;
}

.texto{
    margin-top: 10px;
    color: var(--bg_btt_hover);
    text-align: center;
    background-color: var(--bg_pag);
    border-radius: 10px;
}

#btt{
    height: 40px;
    width: 400px;
    margin-top: 20px;
    margin-bottom: 18px;
    background-color: var(--bg_btt);
    border: none;
    color: var(--c_font_light);
    font-weight: bolder;
    text-transform: uppercase;
    cursor: pointer;
    transition: 0.5s ease-out;
    border-radius: 10px;
    margin-left: 36%;
}

#btt:hover {
    background-color: var(--bg_btt_hover);
    color: var(--c_font_light);
    transition: 0.5s ease-in;
}

.caixa img{
    width: 450px;
    height: 450px;
    margin-left: 12%;
    align-items: center;
}

//javascript

const btt_mobile = document.getElementById("btt_mobile");

function toggle_menu(event){

    if(event.type == 'touchstart') event.preventDefault();

    const navbar = document.getElementById("navbar");
    navbar.classList.toggle("active");

}

btt_mobile.addEventListener('click', toggle_menu);
btt_mobile.addEventListener('touchstart', toggle_menu);

let slide_index = 1;

show_slide(slide_index);

function next_slide(n){
    show_slide(slide_index += n);
}

function current_slide(n){
    show_slide(slide_index = n);
}

function show_slide(n){

    let i;
    let slides = document.getElementsByClassName('slide');
    let dots = document.getElementsByClassName('dot');

    if(n > slides.length) slide_index = 1;
    if(n < 1) slide_index = slides.length;

    for(i = 0; i < slides.length; i++){
        slides[i].style.display = "none";
    }

    for(i = 0; i < dots.length; i++){
        dots[i].className = dots[i].className.replace(" active", "");
    }

    slides[slide_index - 1].style.display = "block";
    dots[slide_index - 1].className += " active";

}
