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
         
            <p id="missao"><em>Nossa missão é´:<strong>"Proporcionar auto-estima e qualidade de vida aos
             clientes"<strong>.</em></p>

           <p>Oferecemosprofissionais experientes e antenadosa ás mudançasno mundo da moda.O atendimento possui padrão de exelencia e agilidadee satisfação dos
           nossos clientes.</p>
           </div>
           <div class="benefícios">
             <h3 class=" titulo-centralizado"Beneficios</h3>

             <ul>
                <lí class="itens">Atentimento aos Clientes</li>
                <lí class= "itens">Espaço diferenciado</li>
                <lí class= "itens">Localização</li>
                <lí class= "itens">Profissionais Qualificados</li>
         
            </ul>

            <img> src="beneficios .jpg" class="imagembeneficios">
        </div>
   </body>

   
produtos.HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTL-8">
        <title>Produtos- Barbearia Alura</title>
        
        <linkr rel="stylesheet" href="reset.css">
        <link real="stylesheet" href="produtos.css">
     </head>
     <body>
        <header>
           <h1><img src="logo.png"></h1>

              <nav>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li><a href="produtos.html">Produtos</a></li>
                    <li><a href=" contato.html">Contatos</a></li>
                </ul>
                <nav>
            </header>

            <main>
               <ul>
                   <li>
                     <h2>Cabelo,/h2>
                     <img scr="cabelo.jgp">
                     <p>Na tesoura ou máquina, como o cliente preferir</p>
                     <p>R$ 25,00</p>
                 </li>
                 <li>
                    <h2>Barba</h2>
                    <img src="barba.jpg">
                    <p>Corte e desenho profissionalde barba</p>
                    <p>R$ 18,00</p>
                </li>
                <li>
                    <h2>Cabelo + Barba</h2>
                    <img src=" cabelo+barba.jpg">
                    <p>Pacote completo de cabelo e barba</p>
                    <p>r$ 35,00</p>
                </li>
              </ul>
        </main>
      </body>
 </html>

<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTL-8">
        <title>Produtos- Barbearia Alura</title>
        
        <linkr rel="stylesheet" href="reset.css">
        <link real="stylesheet" href="produtos.css">
     </head>
     <body>
        <header>
           <h1><img src="logo.png"></h1>

              <nav>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li><a href="produtos.html">Produtos</a></li>
                    <li><a href=" contato.html">Contatos</a></li>
                </ul>
                <nav>
            </header>

            <main>
               <ul>
                   <li>
                     <h2>Cabelo,/h2>
                     <img scr="cabelo.jgp">
                     <p>Na tesoura ou máquina, como o cliente preferir</p>
                     <p>R$ 25,00</p>
                 </l






      reset.css  
/*html://meyerweb.com/eric/tools/css/reset/
v2.0|20110126
license:none (public domain)
*/

html ,body, div, span, applet, object, iframe, 
h1, h2, h3, h4, h5, h6, p, blockquote, pre, 
a, abbr, acronym, address, big, cite, code, 
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var, 
b, u, i, center, 
dl, dt, dd, ol, ul, li, 
fieldset, form, label, legend, 
table, caption, tbody, tfoot, thead,th, td, 
article, figcaption, footer, header,hgroup, 
menu, nav, output, ruby, section, summary, 
time, mark, audio, video {
      margin: 0;
     padding: 0;
     border: 0;
     font-size:100%;
     font: inherit;
     vertical-align: baseline;
}

body {
    line-height:1;/*HTML5 display-role reset for older browsers */
article, aside,details, figcaption, figure,
footer, header, hgroup, menu, nav,section {
    display:block;
}
ol, ol {
    list-style: none;
}
blockquote, q {
    quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
    content:"";
    content: none;
}
table {
    border-collapse:collapse
    border-spacing: 0;
}

    
 produtos.css
 header{
    backgraund: #bbbbbb;
    padding: 20px 0;
} 

caixa {
  position: relative;
 margin: 0auto;
}

nav {
    position: absolute;
    top:110px;
    right: 0;
}

nav li {
    display:inline;
    margin: 0 0 0 15px;
}

nav a {
      text-transform: uppercase;
      color: #000000;
      front-weight: bold;
      front- size:22px;
      text-decoration: none;





PRODUTOS.CSS
header {
background: #BBBBBB;
padding: 20px 0;
}

.caixa {
position: relative;
width: 940px;
margin: 0 auto;
}

nav {
position: absolute;
top: 110px;
right: 0;
}

nav li {
display: inline;
margin: 0 0 0 15px;
}

nav a {
text-transform: uppercase;
color: #000000;
font-weight: bold;
font-size: 22px;
text-decoration: none;
}

nav a:hover {
color: #C78C19;
text-decoration: underline;
}

.produtos {
width: 940px;
margin: 0 auto;
padding: 50px 0;
}

.produtos li {



style.css
banner {
width:100%;
}

.principal{
background: #CCCCCC;
padding: 30px;
}

.titulo-principal {
padding-left: 20px;
}

.titulo-centralizado {
text-align: center
}

p {
text-align: center;
}

#missao {
font-size: 20px
}

em strong {
color: #FF0000;
}

.itens {
font-style: italic
}

profile

~/.profile: executed by the command interpreter for login shells.
# This file is not read by bash(1), if ~/.bash_profile or ~/.bash_login
# exists.
# see /usr/share/doc/bash/examples/startup-files for examples.
# the files are located in the bash-doc package.

# the default umask is set in /etc/profile; for setting the umask
# for ssh logins, install and configure the libpam-umask package.
#umask 022

# if running bash
if [ -n "$BASH_VERSION" ]; then
    # include .bashrc if it exists
    if [ -f "$HOME/.bashrc" ]; then
. "$HOME/.bashrc"
    fi
fi

# set PATH so it includes user's private bin if it exists
if [ -d "$HOME/bin" ] ; then
    PATH="$HOME/bin:$PATH"
fi

# set PATH so it includes user's private bin if it exists
if [ -d "$HOME/.local/bin" ] ; then
    PATH="$HOME/.local/bin:$PATH"
fi
export DIALOG_SLEEP=4

contato html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Contato - Barbearia Alura</title>

<link rel="stylesheet" href="reset.css">
<link rel="stylesheet" href="style.css">
</head>
<body>
<header>
<div class="caixa">
<h1><img src="logo.png"></h1>

<nav>
<ul>
<li><a href="index.html">Home</a></li>
<li><a href="produtos.html">Produtos</a></li>
<li><a href="contato.html">Contato</a></li>
</ul>
</nav>
</div>
</header>

<main>
<form>
<label for="nomesobrenome">Nome e sobrenome</label>
<input type="text" id="nomesobrenome">

<label for="email">Email</label>
<input type="text" id="email">

<label for="telefone">Telefone</label>
<input type="text" id="telefone">

<input type="submit" value="Enviar formulário

style.home.css
banner {
width:100%;
}

.principal{
background: #CCCCCC;
padding: 30px;
}

.titulo-principal {
padding-left: 20px;
}

.titulo-centralizado {
text-align: center
}

p {
text-align: center;
}

#missao {
font-size: 20px
}

em strong {
color: #FF0000;
}

.itens {
font-style: italic
}

.beneficios {
background: #FFFFFF;
padding: 20px;
}

ul {
display: inline-block;
vertical-align: top;
width: 20%;
margin-right: 15%;
}

.imagembeneficios {
width: 50%;
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
   



















