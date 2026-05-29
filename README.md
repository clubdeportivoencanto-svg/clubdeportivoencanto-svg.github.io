<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Canchas Encanto Campestre</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f4f7f4;
      color: #222;
    }

    header {
      background: #064d2c;
      color: white;
      padding: 35px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 42px;
    }

    header p {
      font-size: 20px;
      color: #ffe600;
    }

    .container {
      max-width: 1100px;
      margin: 30px auto;
      padding: 20px;
    }

    .card {
      background: white;
      border-radius: 18px;
      padding: 25px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.12);
      margin-bottom: 25px;
    }

    h2 {
      color: #064d2c;
    }

    label {
      font-weight: bold;
      display: block;
      margin-top: 15px;
    }

    input, select {
      width: 100%;
      padding: 13px;
      margin-top: 6px;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    button {
      margin-top: 20px;
      width: 100%;
      padding: 15px;
      background: #ffdd00;
      border: none;
      border-radius: 12px;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
    }

    button:hover {
      background: #e6c900;
    }

    .resumen {
      background: #eef8f1;
      border-left: 6px solid #064d2c;
      padding: 20px;
      border-radius: 12px;
      margin-top: 20px;
    }

    .precio {
      font-size: 28px;
      color: #064d2c;
      font-weight: bold;
    }

    .tag {
      display: inline-block;
      background: #ffdd00;
      padding: 6px 12px;
      border-radius: 20px;
      font-weight: bold;
      margin-top: 10px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }

    th {
      background: #064d2c;
      color: white;
    }

    th, td {
      padding: 12px;
      border: 1px solid #ddd;
      text-align: center;
    }

    .whatsapp {
      background: #25d366;
      color: white;
    }
  </style>
</head>
<body>

<header>
  <h1>Canchas Encanto Campestre</h1>
  <p>Reserva tu espacio deportivo en segundos</p>
</header>

<div class="container">

  <div class="card">
    <h2>Reservar cancha</h2>

    <label>Nombre completo</label>
    <input type="text" id="nombre" placeholder="Nombre del cliente">

    <label>WhatsApp</label>
    <input type="text" id="whatsapp" placeholder="Ej: 3001234567">

    <label>Cancha</label>
    <select id="cancha" onchange="mostrarPersonas()">
      <option value="sintetica1">Cancha Sintética No. 1</option>
      <option value="sintetica2">Cancha Sintética No. 2</option>
      <option value="voley1">Voley Playa No. 1</option>
      <option value="voley2">Voley Playa No. 2</option>
    </select>

    <label>Fecha</label>
    <input type="date" id="fecha">

    <label>Hora de inicio</label>
    <select id="hora">
      <option value="6">6:00 a.m.</option>
      <option value="7">7:00 a.m.</option>
      <option value="8">8:00 a.m.</option>
      <option value="9">9:00 a.m.</option>
      <option value="10">10:00 a.m.</option>
      <option value="11">11:00 a.m.</option>
      <option value="12">12:00 p.m.</option>
      <option value="13">1:00 p.m.</option>
      <option value="14">2:00 p.m.</option>
      <option value="15">3:00 p.m.</option>
      <option value="16">4:00 p.m.</option>
      <option value="17">5:00 p.m.</option>
      <option value="18">6:00 p.m.</option>
      <option value="19">7:00 p.m.</option>
      <option value="20">8:00 p.m.</option>
      <option value="21">9:00 p.m.</option>
      <option value="22">10:00 p.m.</option>
    </select>

    <label>Cantidad de horas</label>
    <input type="number" id="horas" value="1" min="1">

    <div id="personasBox" style="display:none;">
      <label>Cantidad de personas</label>
      <input type="number" id="personas" value="6" min="1">
    </div>

    <button onclick="calcularReserva()">Calcular reserva</button>

    <div id="resultado"></div>

    <button class="whatsapp" onclick="enviarWhatsApp()">Confirmar por WhatsApp</button>
  </div>

  <div class="card">
    <h2>Tarifas</h2>
    <table>
      <tr>
        <th>Cancha</th>
        <th>Día</th>
        <th>Noche</th>
        <th>Hora Valle</th>
      </tr>
      <tr>
        <td>Sintética No. 1</td>
        <td>$60.000</td>
        <td>$80.000</td>
        <td>$40.000</td>
      </tr>
      <tr>
        <td>Sintética No. 2</td>
        <td>$40.000</td>
        <td>$50.000</td>
        <td>$20.000</td>
      </tr>
      <tr>
        <td>Voley Playa</td>
        <td>$30.000 / $40.000</td>
        <td>$40.000 / $50.000</td>
        <td>$20.000</td>
      </tr>
    </table>
  </div>

</div>

<script>
  let resumenTexto = "";

  function mostrarPersonas() {
    const cancha = document.getElementById("cancha").value;
    const personasBox = document.getElementById("personasBox");

    if (cancha === "voley1" || cancha === "voley2") {
      personasBox.style.display = "block";
    } else {
      personasBox.style.display = "none";
    }
  }

  function calcularReserva() {
    const nombre = document.getElementById("nombre").value;
    const whatsapp = document.getElementById("whatsapp").value;
    const cancha = document.getElementById("cancha").value;
    const fecha = document.getElementById("fecha").value;
    const hora = parseInt(document.getElementById("hora").value);
    const horas = parseInt(document.getElementById("horas").value);
    const personas = parseInt(document.getElementById("personas").value || 0);

    if (!nombre || !whatsapp || !fecha) {
      alert("Por favor completa nombre, WhatsApp y fecha.");
      return;
    }

    const fechaObj = new Date(fecha + "T00:00:00");
    const diaSemana = fechaObj.getDay();
    const esLunesViernes = diaSemana >= 1 && diaSemana <= 5;
    const esHoraValle = esLunesViernes && hora >= 11 && hora < 15;

    let valorHora = 0;
    let tarifa = "";

    if (cancha === "sintetica1") {
      if (esHoraValle) {
        valorHora = 40000;
        tarifa = "Hora Valle";
      } else if (hora < 18) {
        valorHora = 60000;
        tarifa = "Diurna";
      } else {
        valorHora = 80000;
        tarifa = "Nocturna";
      }
    }

    if (cancha === "sintetica2") {
      if (esHoraValle) {
        valorHora = 20000;
        tarifa = "Hora Valle";
      } else if (hora < 18) {
        valorHora = 40000;
        tarifa = "Diurna";
      } else {
        valorHora = 50000;
        tarifa = "Nocturna";
      }
    }

    if (cancha === "voley1" || cancha === "voley2") {
      if (esHoraValle) {
        valorHora = 20000;
        tarifa = "Hora Valle";
      } else if (hora < 18) {
        valorHora = personas <= 6 ? 30000 : 40000;
        tarifa = personas <= 6 ? "Diurna hasta 6 personas" : "Diurna más de 6 personas";
      } else {
        valorHora = personas <= 6 ? 40000 : 50000;
        tarifa = personas <= 6 ? "Nocturna hasta 6 personas" : "Nocturna más de 6 personas";
      }
    }

    const total = valorHora * horas;
    const horaFinal = hora + horas;

    const nombreCancha = {
      sintetica1: "Cancha Sintética No. 1",
      sintetica2: "Cancha Sintética No. 2",
      voley1: "Voley Playa No. 1",
      voley2: "Voley Playa No. 2"
    }[cancha];

    resumenTexto =
      `Hola ${nombre}, tu reserva en Canchas Encanto Campestre ha sido registrada.%0A%0A` +
      `Cancha: ${nombreCancha}%0A` +
      `Fecha: ${fecha}%0A` +
      `Hora: ${hora}:00%0A` +
      `Horas reservadas: ${horas}%0A` +
      `Tarifa: ${tarifa}%0A` +
      `Valor por hora: $${valorHora.toLocaleString("es-CO")}%0A` +
      `Total a pagar: $${total.toLocaleString("es-CO")}`;

    document.getElementById("resultado").innerHTML = `
      <div class="resumen">
        <h3>Resumen de reserva</h3>
        <p><strong>Cliente:</strong> ${nombre}</p>
        <p><strong>WhatsApp:</strong> ${whatsapp}</p>
        <p><strong>Cancha:</strong> ${nombreCancha}</p>
        <p><strong>Fecha:</strong> ${fecha}</p>
        <p><strong>Hora inicio:</strong> ${hora}:00</p>
        <p><strong>Hora final:</strong> ${horaFinal}:00</p>
        <p><strong>Horas:</strong> ${horas}</p>
        ${(cancha === "voley1" || cancha === "voley2") ? `<p><strong>Personas:</strong> ${personas}</p>` : ""}
        <p><strong>Tarifa aplicada:</strong> <span class="tag">${tarifa}</span></p>
        <p><strong>Valor por hora:</strong> $${valorHora.toLocaleString("es-CO")}</p>
        <p class="precio">Total: $${total.toLocaleString("es-CO")}</p>
      </div>
    `;
  }

  function enviarWhatsApp() {
    const whatsapp = document.getElementById("whatsapp").value;

    if (!resumenTexto) {
      alert("Primero calcula la reserva.");
      return;
    }

    const url = `https://wa.me/57${whatsapp}?text=${resumenTexto}`;
    window.open(url, "_blank");
  }
</script>

</body>
</html>
