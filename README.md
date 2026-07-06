style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');
  
  body { 
    background-color: #001f3f; /* Azul Marino como base */
    color: #333; 
    display: flex; justify-content: center; align-items: center; 
    height: 100vh; margin: 0; text-align: center; 
    font-family: 'Montserrat', sans-serif; 
  }
  
  .contenedor { 
    padding: 40px; max-width: 80%; 
    border-radius: 30px;
    background: #fdfdfd; /* Fondo limpio y claro */
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  }
  
  h1 { font-size: 28px; margin-bottom: 30px; color: #ff9aa2; } /* Rosa Pastel */
  
  button { 
    padding: 20px; margin: 15px 0; font-size: 20px; cursor: pointer; 
    border-radius: 15px; border: none; 
    background: #c7ceea; /* Verde/Azul Pastel */
    color: #444; 
    display: block; width: 100%; transition: 0.3s;
    font-weight: 600;
  }
  
  button:hover { background: #b5ead7; color: #222; }
</style>

<div class="contenedor" id="pantalla">
  <h1 id="texto">Test de Personalidad: ¿Qué tan compatible eres conmigo?, osea yo, paulina jaja</h1>
  <div id="areaBotones">
    <button onclick="siguiente(1)">Empezar Test</button>
  </div>
</div>

<script>
  function siguiente(paso) {
    const texto = document.getElementById('texto');
    const area = document.getElementById('areaBotones');
    
    if (paso === 1) {
      texto.innerText = " Si yo fuera un zorro y tu un conejo,sabiendo que puedo devorarte,correrias el riesgo de acercarte conmigo ?";
      area.innerHTML = `<button onclick="siguiente(2)">no se w</button><button onclick="siguiente(2)">quiero que me comas 🕴️</button>`;
    } else if (paso === 2) {
      texto.innerText = "ME ODIAS Y ME QUIERES MUERTA VERDAD NAYLEEEENNN???";
      area.innerHTML = `<button onclick="siguiente(3)">Te amo </button><button onclick="siguiente(3)">xq me dices naylen, y no amorr???????🥀</button>`;
    } else if (paso === 3) {
      texto.innerText = "solo quiero que sepas que TE AMO con toda el alma naylen🩷💕💞";
      area.innerHTML = `<button onclick="siguiente(4)">Te amo tonota</button><button onclick="siguiente(4)">deja de decirme nay ☠️</button>`;
    } else if (paso === 4) {
      texto.innerText = "pizza con piña o avatar?☠️ solo quiero saber jajaja no tiene nada q ver conmigo";
      area.innerHTML = `<button onclick="siguiente(5)">avatar y pizza con piña y vtalv w xd</button><button onclick="siguiente(5)">pizza con piña</button>`;
    } else if (paso === 5) {
      texto.innerText = "bueno ahora tu resultado del test, si no eres compatible conmigo, ps alv, no importa, te hare mi esposa y el amor si quieres ps";
      area.innerHTML = `<button onclick="siguiente(6)">Okei🥀🥀🥀</button>`;
    } else if (paso === 6) {
      texto.innerText = "¿Quieres ser mi novia?";
      area.innerHTML = `
        <button onclick="alert('Ahora somos pololas, te amo conejita preciosa')">SÍ, QUIEROoOoOo</button>
        <button id="btnNo" onmouseover="moverBoton()">NO</button>
      `;