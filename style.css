const URL_API =
"https://script.google.com/macros/s/AKfycbxWck4ukpJXSVt0q1yWlxji9lU54q7xhn3-58Qr130Dou2u3PVrZm-IhECLe2xinM8S/exec";

const codigo =
document.getElementById(
"codigo"
);

const nombre =
document.getElementById(
"nombre"
);

const resultado =
document.getElementById(
"resultado"
);

const estado =
document.getElementById(
"estado"
);

let timer;

codigo.addEventListener(
"keydown",
(e)=>{

if(
e.key==="Enter"
||
e.key==="Go"
||
e.key==="Search"
){

e.preventDefault();

nombre.value="";

buscarCodigo();

}

}
);

codigo.addEventListener(
"change",
()=>{

if(
codigo.value.trim()
){

buscarCodigo();

}

}
);

nombre.addEventListener(
"keydown",
(e)=>{

if(
e.key==="Enter"
||
e.key==="Go"
||
e.key==="Search"
){

e.preventDefault();

codigo.value="";

buscarNombre();

}

}
);

nombre.addEventListener(
"change",
()=>{

if(
nombre.value.trim()
){

buscarNombre();

}

}
);

async function buscarCodigo(){

const q=
codigo.value.trim();

if(!q){

resultado.innerHTML="";
estado.innerHTML="";

return;

}

buscar(
"codigo",
q
);

}

async function buscarNombre(){

const q=
nombre.value.trim();

if(!q){

resultado.innerHTML="";
estado.innerHTML="";

return;

}

buscar(
"nombre",
q
);

}

async function buscar(
tipo,
q
){

estado.innerHTML=
"Buscando...";

try{

const r=
await fetch(
`${URL_API}?tipo=${tipo}&q=${encodeURIComponent(q)}`
);

const datos=
await r.json();

mostrar(
datos
);

estado.innerHTML=
`${datos.length} resultado(s)`;

}

catch{

estado.innerHTML=
"Error conectando";

}

}

function mostrar(
lista
){

resultado.innerHTML="";

if(
lista.length===0
){

resultado.innerHTML=
"<div class='card'>Sin resultados</div>";

return;

}

lista.forEach(
p=>{

resultado.innerHTML+=`

<div class="card">

<div class="detalle">

${p.detalle}

</div>

<div class="info">

Código:
${p.codigo}

</div>

${
p.codigo !== p.coddun14
?

`

<div class="info">

Barra:
${p.coddun14}

</div>

`

:

""
}

<div class="info">

${p.tipo_mater}

</div>

<div class="precio">

$ ${Number(
p.precio
).toLocaleString()}

</div>

</div>

`;

}

);

}
