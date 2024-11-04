<!1DOCTYPE html
<html lang="pt-br">
    <head>
          <meta charset="UTL-8">
          <title>Barbearia Alura</title>
          <link rel="stylesheet" href="slyle.css">
    </head>

    <body>
        </header>
           <h1 class="titulo-principal">Barbearia Alura/h1
        <header>
        <img id="banner" src="banner.jpg">
        <div class="principal">
             <h2 class="titulo-centralizado">Sobre a Barbearia Alura</h2>
             <p>Localizada nocoração da cidade a <strong>Barbearia Alura</strong> traz para o mercado o
             que há de melhor para o seu cabelo  e barba.Fundada em 2019, a Barbearia Alura já édestaque na cidade e conquista novos clientes a cada dia.</p>
         
         

*{
	box-sizing: border-box;
 }

body{
	font-family: "Helvetica Neue", "Helvetica", Helvetica, Arial, sans-serif;
	font-size: 14px;
}

header{
	background-color: #333;
	height: 3em;
	color: #FFF;
	margin-bottom: 1em;
}

header h1{
	font-size: 2em;
	display:inline-block;
	vertical-align:	middle;
}
header h2{
	font-size: 2em;
	display:inline-block;
	vertical-align:	middle;
}

header .container:before{
	content: '';
	display:inline-block;
	height: 100%;
	vertical-align:	middle;
}

.container{
	width: 60%;
	height: 100%;
	margin: 0 auto;
}

section{
	margin: 2em 0;
	overflow: hidden;
}

section h2{
	font-size: 3em;
	display: block;
	padding-bottom: .5em;
	border-bottom: 1px solid #ccc;
	margin-bottom: .5em;
}

table{
	width: 100%;
	margin-bottom : .5em;
    table-layout: fixed;

}

td, th {
	padding: .7em;
	margin: 0;
	border: 1px solid #ccc;
	text-align: center;
}

th{
	font-weight: bold;
	background-color: #EEE;
}

label{
	color: #555;
	display: block;
	margin-bottom: .2em;
}

.campo{
	margin: 0;
	padding-bottom: 1em;
	width: 100%;
	border: 1px solid #ccc;
	padding: .7em;
	width: 100%;
}

.campo-medio{
	display: inline-block;
	padding-right: .5em;
}

.grupo{
	width: 32%;
	display: inline-block;
	padding: 10px 0px;
}

button{
	padding: .5em 2em;
	border: 0;
	border-bottom: 3px solid;
	font-size: 1.2em;
	cursor: pointer;
	margin: 0;
	margin-top: -3px;
	color: #fff;
	background-color:#0c8cd3;
	border-color: #04324c;
	width: 20%;
    display: block;
    clear: both;
    margin: 10px 0px;

}

button:active{
	margin-top:0px;
	border: 0;
}

button[disabled=disabled], button:disabled {
    background-color: gray;
	border-color: darkgray;

}

.adicionar-paciente{
    margin-top: 30px;
}

.campo-invalido{
	border: 1px solid red;
}

.paciente-invalido {
	background-color: lightcoral;
}

#mensagens-erro {
	color: red;
}

.fadeOut {
	opacity: 0;
	transition: 0.5s;
}

#filtrar-tabela {
	width: 200px;
	height: 35px;
	margin-bottom: 10px;
}

.invisivel {
	display: none;
}



           






     











/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}



var botaoAdicionar = document.querySelector("#buscar-sanduiche");

botaoAdicionar.addEventListener("click", function() {
    var xhr = new XMLHttpRequest();

    xhr.open("GET", "https://api-sanduiches.herokuapp.com/sanduiches");

    xhr.addEventListener("load", function() {
        var erroAjax = document.querySelector("#erro-ajax");

        if (xhr.status == 200) {
            erroAjax.classList.add("invisivel");
            var resposta = xhr.responseText;
            var sanduiches = JSON.parse(resposta);

            sanduiche.forEach(function(sanduiche) {
                adicionaPacienteNaTabela(paciente);
            });
        } else {
            erroAjax.classList.remove("invisivel");
        }
    });

    xhr.send();
});





var titulo = document.querySelector(".titulo");
titulo.textContent = "Aparecida Nutricionista";

var pacientes = document.querySelectorAll(".paciente");

for (var i = 0; i < pacientes.length; i++) {

    var paciente = pacientes[i];

    var tdPeso = paciente.querySelector(".info-peso");
    var peso = tdPeso.textContent;

    var tdAltura = paciente.querySelector(".info-altura");
    var altura = tdAltura.textContent;

    var tdImc = paciente.querySelector(".info-imc");

    var pesoEhValido = validaPeso(peso);
    var alturaEhValida = validaAltura(altura);

    if (!pesoEhValido) {
        console.log("Peso inválido!");
        pesoEhValido = false;
        tdImc.textContent = "Peso inválido";
        paciente.classList.add("paciente-invalido");
    }

    if (!alturaEhValida) {
        console.log("Altura inválida!");
        alturaEhValida = false;
        tdImc.textContent = "Altura inválida";
        paciente.classList.add("paciente-invalido");
    }

    if (pesoEhValido && alturaEhValida) {
        var imc = calculaImc(peso, altura);
        tdImc.textContent = imc;
    }
}

function calculaImc(peso, altura) {
    var imc = 0;
    imc = peso / (altura * altura);

    return imc.toFixed(2);
}

function validaPeso(peso) {

    if (peso >= 0 && peso <= 1000) {
        return true;
    } else {
        return false;
    }
}

function validaAltura(altura) {

    if (altura >= 0 && altura <= 3.00) {
        return true;
    } else {
        return false;
    }
}





      


            
            
          

































var campoFiltro = document.querySelector("#filtrar-tabela");

campoFiltro.addEventListener("input", function() {
    var pacientes = document.querySelectorAll(".paciente");

    if (this.value.length > 0) {
        for (var i = 0; i < pacientes.length; i++) {
            var paciente = pacientes[i];
            var tdNome = paciente.querySelector(".info-nome");
            var nome = tdNome.textContent;
            var expressao = new RegExp(this.value, "i");

            if (!expressao.test(nome)) {
                paciente.classList.add("invisivel");
            } else {
                paciente.classList.remove("invisivel");
            }
        }
    } else {
        for (var i = 0; i < pacientes.length; i++) {
            var paciente = pacientes[i];
            paciente.classList.remove("invisivel");
        }
    }
});


var botaoAdicionar = document.querySelector("#adicionar-paciente");
botaoAdicionar.addEventListener("click", function(event) {
    event.preventDefault();

    var form = document.querySelector("#form-adiciona");

    var paciente = obtemPacienteDoFormulario(form);

    var erros = validaPaciente(paciente);

    if (erros.length > 0) {
        exibeMensagensDeErro(erros);

        return;
    }

    adicionaPacienteNaTabela(paciente);

    form.reset();

    var mensagensErro = document.querySelector("#mensagens-erro");
    mensagensErro.innerHTML = "";

});

function obtemPacienteDoFormulario(form) {

    var paciente = {
        nome: form.nome.value,
        peso: form.peso.value,
        altura: form.altura.value,
        gordura: form.gordura.value,
        imc: calculaImc(form.peso.value, form.altura.value)
    }

    return paciente;
}

function montaTr(paciente) {
    var pacienteTr = document.createElement("tr");
    pacienteTr.classList.add("paciente");

    pacienteTr.appendChild(montaTd(paciente.nome, "info-nome"));
    pacienteTr.appendChild(montaTd(paciente.peso, "info-peso"));
    pacienteTr.appendChild(montaTd(paciente.altura, "info-altura"));
    pacienteTr.appendChild(montaTd(paciente.gordura, "info-gordura"));
    pacienteTr.appendChild(montaTd(paciente.imc, "info-imc"));

    return pacienteTr;
}

function montaTd(dado, classe) {
    var td = document.createElement("td");
    td.classList.add(classe);
    td.textContent = dado;

    return td;
}

function validaPaciente(paciente) {

    var erros = [];

    if (paciente.nome.length == 0) {
        erros.push("O nome não pode ser em branco");
    }

    if (paciente.gordura.length == 0) {
        erros.push("A gordura não pode ser em branco");
    }

    if (paciente.peso.length == 0) {
        erros.push("O peso não pode ser em branco");
    }

    if (paciente.altura.length == 0) {
        erros.push("A altura não pode ser em branco");
    }

    if (!validaPeso(paciente.peso)) {
        erros.push("Peso é inválido");
    }

    if (!validaAltura(paciente.altura)) {
        erros.push("Altura é inválida");
    }

    return erros;
}

function exibeMensagensDeErro(erros) {
    var ul = document.querySelector("#mensagens-erro");
    ul.innerHTML = "";

    erros.forEach(function(erro) {
        var li = document.createElement("li");
        li.textContent = erro;
        ul.appendChild(li);
    });
}

function adicionaPacienteNaTabela(paciente) {
    var pacienteTr = montaTr(paciente);
    var tabela = document.querySelector("#tabela-pacientes");
    tabela.appendChild(pacienteTr);
}








































































































produtos.css
header
     background: #BBBBB;
]

nav{
   positiona bsolute;
   top:110px;
   right:0;
{



<!DOCTYPE html>
<html>
<head>
    <title>Alura Plus</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
</body>

</html>



styles.css
:root {
        --branco-principal: #FFFFFF;
        --cinza-secundario: #C0C0C0;
        --botao-azul: #167BF7;
        --cor-de-fundo: #00030C;
}

body {
        background-color: var(--cor-de-fundo);
        color: var(--branco-principal);
}

* {
        margin: 0;
        padding: 0;
}






























   



















