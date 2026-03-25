# Ramos_Eternos
Página web de Lino's Art Ramos Eternos💖
 <!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lino's Art - Ramo Eterno</title>
<link href="https://fonts.googleapis.com/css2?family=Sensa+Brush&display=swap" rel="stylesheet">
<style>
  body { font-family: 'Sensa Brush', cursive; margin:0; padding:0; background:#ffe6f0; color:#000; }
  .container { width:8in; min-height:14in; margin:0 auto; padding:25px; border-radius:25px; background:#fff0f5; box-shadow:0 0 15px rgba(0,0,0,0.1);}
  header { text-align:center; margin-bottom:25px; }
  header h1 { font-size:50px; color:#ff69b4; margin-bottom:10px; }
  header h2 { font-size:36px; color:#000; }
  section { margin-bottom:20px; padding:15px; background:#fff0f5; border-radius:20px; box-shadow:0 0 8px rgba(0,0,0,0.05); }
  label { display:block; margin:10px 0; font-size:20px; }
  .flores { display:flex; flex-wrap:wrap; gap:10px; margin-bottom:10px; }
  .flor { padding:12px 20px; background:#ffb6c1; border-radius:25px; cursor:pointer; font-size:22px; transition: transform 0.2s, box-shadow 0.2s; }
  .flor.selected { box-shadow:0 0 0 5px #ff69b4; transform:scale(1.1); }
  .color-options { display:flex; flex-wrap:wrap; gap:12px; margin-bottom:10px; }
  .color-block { text-align:center; font-size:18px; }
  .color-option { width:40px; height:40px; border-radius:50%; border:2px solid #000; cursor:pointer; margin-bottom:5px; transition: transform 0.2s; }
  .color-option.selected { box-shadow:0 0 0 5px #ff69b4; transform:scale(1.2); }
  input[type="number"], input[type="text"], select { padding:10px; border-radius:15px; border:1px solid #ccc; margin-bottom:5px; width:100%; font-size:20px; box-sizing:border-box; }
  button { padding:15px 30px; font-size:26px; background:#ff69b4; color:#fff; border:none; border-radius:30px; cursor:pointer; transition: background 0.3s; }
  button:hover { background:#ff1493; }
  h2,h3 { font-size:28px; margin-top:15px; }
  .mensaje-foto { font-size:24px; color:#ff1493; font-weight:bold; text-align:center; padding:15px; background:#fff0f5; border-radius:20px; margin-bottom:20px; }
</style>
</head>
<body>
<div class="container">
  <header>
    <h1>✨ Lino's Art ✨</h1>
    <h2>Ramo Eterno</h2>
  </header>

  <!-- Selección de flores -->
  <section>
    <label>🌸 Selecciona la flor:</label>
    <div class="flores" id="galeriaFlores">
      <div class="flor" data-flor="Gardenia">Gardenia</div>
      <div class="flor" data-flor="Tulipán">Tulipán</div>
      <div class="flor" data-flor="Girasol pequeña">Girasol pequeña</div>
      <div class="flor" data-flor="Girasol grande">Girasol grande</div>
      <div class="flor" data-flor="Amapola">Amapola</div>
      <div class="flor" data-flor="Rosa">Rosa</div>
      <div class="flor" data-flor="Flor de lotus">Flor de lotus</div>
      <div class="flor" data-flor="Lirio">Lirio</div>
    </div>
  </section>

  <!-- Colores -->
  <section>
    <label>🎨 Colores de las flores (puedes seleccionar varios):</label>
    <div class="color-options" id="colorOptions">
      <div class="color-block"><div class="color-option" style="background:#ffb6c1;" data-color="Rosa"></div>Rosa</div>
      <div class="color-block"><div class="color-option" style="background:#00ffff;" data-color="Cian"></div>Cian</div>
      <div class="color-block"><div class="color-option" style="background:#ffffff; border:1px solid #000;" data-color="Blanco"></div>Blanco</div>
      <div class="color-block"><div class="color-option" style="background:#000000;" data-color="Negro"></div>Negro</div>
      <div class="color-block"><div class="color-option" style="background:#ff0000;" data-color="Rojo"></div>Rojo</div>
      <div class="color-block"><div class="color-option" style="background:#800020;" data-color="Burdeos"></div>Burdeos</div>
      <div class="color-block"><div class="color-option" style="background:#ffff00;" data-color="Amarillo"></div>Amarillo</div>
      <div class="color-block"><div class="color-option" style="background:#98fb98;" data-color="Verde claro"></div>Verde claro</div>
      <div class="color-block"><div class="color-option" style="background:#006400;" data-color="Verde oscuro"></div>Verde oscuro</div>
      <div class="color-block"><div class="color-option" style="background:#808000;" data-color="Verde oliva"></div>Verde oliva</div>
      <div class="color-block"><div class="color-option" style="background:#0000ff;" data-color="Azul"></div>Azul</div>
      <div class="color-block"><div class="color-option" style="background:#40e0d0;" data-color="Turquesa"></div>Turquesa</div>
      <div class="color-block"><div class="color-option" style="background:#87ceeb;" data-color="Azul cielo"></div>Azul cielo</div>
      <div class="color-block"><div class="color-option" style="background:#8a2be2;" data-color="Violeta"></div>Violeta</div>
      <div class="color-block"><div class="color-option" style="background:#e6e6fa;" data-color="Lavanda"></div>Lavanda</div>
      <div class="color-block"><div class="color-option" style="background:#c8a2c8;" data-color="Lila"></div>Lila</div>
      <div class="color-block"><div class="color-option" style="background:#654321;" data-color="Marrón oscuro"></div>Marrón oscuro</div>
      <div class="color-block"><div class="color-option" style="background:#a52a2a;" data-color="Marrón claro"></div>Marrón claro</div>
    </div>
  </section>

  <!-- Cantidad -->
  <section>
    <label>🔢 Cantidad:</label>
    <select id="cantidad-flor">
      <option value="1">1</option>
      <option value="3">3</option>
      <option value="7">7</option>
      <option value="10">10</option>
      <option value="15">15</option>
      <option value="25">25</option>
    </select>
  </section>

  <!-- Extras -->
  <section>
    <h3>✨ Extras ✨</h3>
    <label>🌹 Corona ($3): <input type="number" id="corona" min="0" value="0"> 
      <select id="coronaColor"><option>Oro</option><option>Plata</option></select>
    </label>
    <label>💡 Luces ($2): <input type="number" id="luces" min="0" value="0"></label>
    <label>🦋 Mariposas ($0.20 c/u): <input type="number" id="mariposas" min="0" value="0">
      <select id="mariposasColor"><option>Oro</option><option>Plata</option></select>
    </label>
    <label>✉️ Sobre con carta ($3): <input type="number" id="sobre" min="0" value="0"></label>
    <label>🎀 Cinta con frase ($2.5): <input type="text" id="cinta" maxlength="100"></label>
    <label>🍫 Ferreros ($1 c/u): <input type="number" id="ferreros" min="0" value="0"></label>
    <label>📦 Cambiar ramo por caja ($6): <input type="checkbox" id="caja"></label>
  </section>

  <!-- Mensaje sobre foto -->
  <div class="mensaje-foto">
    📸 Puedes incluir una foto de referencia si lo deseas.  
    💡 Recuerda guardarla en tu galería antes de enviarla por WhatsApp.
  </div>

  <button onclick="enviarWhatsApp()">💌 Enviar pedido por WhatsApp ✨😁</button>
  <h2 id="precio-total">💖 Precio total: $0 ✨</h2>
</div>

<script>
// Flores
let florSeleccionada = null;
document.querySelectorAll('.flor').forEach(f => {
  f.addEventListener('click', () => {
    document.querySelectorAll('.flor').forEach(fl=>fl.classList.remove('selected'));
    f.classList.add('selected');
    florSeleccionada = f.getAttribute('data-flor');
    calcularTotal();
  });
});

// Colores
document.querySelectorAll('.color-option').forEach(c=>{
  c.addEventListener('click', ()=>{c.classList.toggle('selected'); calcularTotal();});
});

function obtenerColoresSeleccionados(){
  return Array.from(document.querySelectorAll('.color-option'))
    .filter(c=>c.classList.contains('selected'))
    .map(c=>c.getAttribute('data-color'))
    .join(', ');
}

// Calcular precio
function calcularTotal(){
  let precio=0;
  const cantidad=parseInt(document.getElementById("cantidad-flor").value);
  const precios={
    "Rosa": {1:5,3:10,7:20,10:30,15:40,25:50},
    "Tulipán": {1:5,3:10,7:20,10:30,15:40,25:40},
    "Girasol pequeña": {1:9,3:18,7:26,10:36,15:46,25:56},
    "Girasol grande": {1:12},
    "Amapola": {1:5,3:10,7:20,10:30,15:40,25:50},
    "Gardenia": {1:12,3:18,7:26,10:36,15:46,25:56},
    "Flor de lotus": {1:15},
    "Lirio": {1:12}
  };
  if(florSeleccionada && precios[florSeleccionada] && precios[florSeleccionada][cantidad]) precio+=precios[florSeleccionada][cantidad];
  precio+=parseInt(document.getElementById("corona").value)*3;
  precio+=parseInt(document.getElementById("luces").value)*2;
  precio+=parseInt(document.getElementById("mariposas").value)*0.2;
  precio+=parseInt(document.getElementById("sobre").value)*3;
  if(document.getElementById("cinta").value) precio+=2.5;
  precio+=parseInt(document.getElementById("ferreros").value)*1;
  if(document.getElementById("caja").checked) precio+=6;
  document.getElementById("precio-total").innerText="💖 Precio total: $"+precio.toFixed(2)+" ✨";
  return precio.toFixed(2);
}

// Eventos inputs
['cantidad-flor','corona','luces','mariposas','sobre','cinta','ferreros','caja'].forEach(id=>{
  document.getElementById(id).addEventListener('input',calcularTotal);
  document.getElementById(id).addEventListener('change',calcularTotal);
});

// WhatsApp
function enviarWhatsApp(){
  const colores=obtenerColoresSeleccionados();
  const mensaje=`✨😁 ¡Hola! Quiero hacer un pedido de Ramo Eterno 💖:%0A`+
                `🌸 Tipo de flor: ${florSeleccionada || ""}%0A`+
                `🔢 Cantidad: ${document.getElementById("cantidad-flor").value}%0A`+
                `🎨 Colores: ${colores}%0A`+
                `✨ Extras:%0A`+
                `- 🌹 Corona: ${document.getElementById("corona").value} (${document.getElementById("coronaColor").value})%0A`+
                `- 💡 Luces: ${document.getElementById("luces").value}%0A`+
                `- 🦋 Mariposas: ${document.getElementById("mariposas").value} (${document.getElementById("mariposasColor").value})%0A`+
                `- ✉️ Sobre con carta: ${document.getElementById("sobre").value}%0A`+
                `- 🎀 Cinta con frase: ${document.getElementById("cinta").value}%0A`+
                `- 🍫 Ferreros: ${document.getElementById("ferreros").value}%0A`+
                `- 📦 Cambiar ramo por caja: ${document.getElementById("caja").checked ? "Sí" : "No"}%0A`+
                `💖 Precio total: $${calcularTotal()} ✨`;
  window.open(`https://wa.me/17879393404?text=${mensaje}`,'_blank');
}
</script>
</body>
</html>
