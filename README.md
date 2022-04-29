## Preloader em HTML, Javascript, Jquery e CSS.
Cria um efeito de carregamento de cada página no seu site.
No seu site, depois de:

	<head>
    <title>Meu título</title>
	<meta charset="utf-8" />
  
Adicione o seguinte:

    <script type="text/javascript" src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    
    <div id="preloader">
        <div class="loader">Carregando..</div>
    </div>
    
    <style>
        #preloader {
            align-items: center;
            display: flex;
            height: 100vh;
            justify-content: center;
            left: 0;
            position: fixed;
            top: 0;
            transition: opacity 0.2s linear;
            width: 100%;
            z-index: 9999;
            opacity: 1;
            transform: opacity 1s linear;
            overflow: hidden;
            background-color: #4696e5;
        }
    
        .loader,
        .loader:before,
        .loader:after {
            background: #ffffff;
            -webkit-animation: load1 1s infinite ease-in-out;
            animation: load1 1s infinite ease-in-out;
            width: 1em;
            height: 4em;
        }
    
        .loader {
            color: #ffffff;
            text-indent: -9999em;
            margin: 88px auto;
            position: relative;
            font-size: 11px;
            -webkit-transform: translateZ(0);
            -ms-transform: translateZ(0);
            transform: translateZ(0);
            -webkit-animation-delay: -0.16s;
            animation-delay: -0.16s;
        }
    
        .loader:before,
        .loader:after {
            position: absolute;
            top: 0;
            content: '';
        }
    
        .loader:before {
            left: -1.5em;
            -webkit-animation-delay: -0.32s;
            animation-delay: -0.32s;
        }
    
        .loader:after {
            left: 1.5em;
        }
    
        @-webkit-keyframes load1 {
    
            0%,
            80%,
            100% {
                box-shadow: 0 0;
                height: 4em;
            }
    
            40% {
                box-shadow: 0 -2em;
                height: 5em;
            }
        }
    
        @keyframes load1 {
    
            0%,
            80%,
            100% {
                box-shadow: 0 0;
                height: 4em;
            }
    
            40% {
                box-shadow: 0 -2em;
                height: 5em;
            }
        }
    </style>
    
    <script>
        $(document).ready(function () {
            $('#preloader').fadeOut(2000);
        });
    </script>

No código acima, procure e edite as cores, a primeira é a cor do loader, a segunda o fundo geral:

    background: #ffffff;
    background-color: #4696e5;

Salve. Pronto, sua página já possui uma tela de carregamento. Indico colocar no header do website.
