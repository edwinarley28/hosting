<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>VRI · Dashboard Financiero</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
<style>
  :root{
    --verde:#046A38; --verde2:#0b8a4c; --verde-claro:#e8f5ee;
    --tinta:#0f172a; --gris:#64748b; --linea:#e2e8f0;
    --fondo:#f5f7f8; --blanco:#ffffff;
    --rojo:#b91c1c; --ambar:#b45309; --azul:#1d4ed8;
    --radio:14px;
    --sombra:0 1px 2px rgba(15,23,42,.06), 0 10px 30px rgba(15,23,42,.07);
  }
  *{box-sizing:border-box}
  body{font-family:Inter,system-ui,-apple-system,sans-serif;background:var(--fondo);color:var(--tinta);margin:0;}
  a{color:var(--verde2)}

  .topbar{background:linear-gradient(120deg,#03341c 0%, var(--verde) 55%, var(--verde2) 100%);color:#fff;padding:22px 26px;display:flex;flex-wrap:wrap;gap:16px;align-items:center;justify-content:space-between;}
  .brand{display:flex;align-items:center;gap:14px}
  .logo{width:46px;height:46px;border-radius:12px;background:rgba(255,255,255,.14);display:grid;place-items:center;font-weight:800;font-size:15px;border:1px solid rgba(255,255,255,.25);}
  .brand h1{margin:0;font-size:19px;font-weight:700;}
  .brand p{margin:2px 0 0;font-size:12.5px;opacity:.82}
  .status{font-size:12.5px;background:rgba(255,255,255,.13);border:1px solid rgba(255,255,255,.25);padding:8px 14px;border-radius:999px;}

  .wrap{max-width:1400px;margin:0 auto;padding:22px 18px 60px}
  .tabs{display:flex;gap:6px;margin:0 0 18px;flex-wrap:wrap}
  .tab{border:1px solid var(--linea);background:var(--blanco);color:var(--gris);padding:9px 18px;border-radius:999px;font-size:13.5px;font-weight:600;cursor:pointer;transition:.15s;}
  .tab.active{background:var(--verde);border-color:var(--verde);color:#fff;box-shadow:0 4px 14px rgba(4,106,56,.28)}
  .panel{display:none;} .panel.active{display:block;}

  .kpis{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:14px;margin-bottom:20px}
  .kpi{background:var(--blanco);border:1px solid var(--linea);border-radius:var(--radio);padding:16px 18px;box-shadow:var(--sombra);position:relative;overflow:hidden;}
  .kpi::after{content:"";position:absolute;left:0;top:0;bottom:0;width:4px;background:var(--gris)}
  .kpi.verde::after{background:var(--verde2)} .kpi.azul::after{background:var(--azul)}
  .kpi.ambar::after{background:var(--ambar)} .kpi.rojo::after{background:var(--rojo)}
  .kpi .lbl{font-size:12px;text-transform:uppercase;letter-spacing:.6px;color:var(--gris);font-weight:700}
  .kpi .val{font-size:22px;font-weight:800;margin:8px 0 4px;letter-spacing:-.6px;}
  .kpi .sub{font-size:11.5px;color:var(--gris);line-height:1.3}

  .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(400px,1fr));gap:16px}
  .card{background:var(--blanco);border:1px solid var(--linea);border-radius:var(--radio);padding:16px 18px 10px;box-shadow:var(--sombra);}
  .card h3{margin:0 0 12px;font-size:14px;} .chart-box{position:relative;height:300px;}

  .toolbar{display:flex;gap:10px;flex-wrap:wrap;align-items:center;margin-bottom:14px;background:var(--blanco);border:1px solid var(--linea);border-radius:var(--radio);padding:12px 14px;box-shadow:var(--sombra);}
  .toolbar label{font-size:11px;font-weight:700;color:var(--gris);text-transform:uppercase;}
  select,input[type=search]{font-family:inherit;font-size:13px;padding:8px 10px;border-radius:8px;border:1px solid var(--linea);outline:none;}
  select:focus,input[type=search]:focus{border-color:var(--verde2);}
  input[type=search]{min-width:200px;flex:1;}
  .btn{font-size:13px;font-weight:700;cursor:pointer;border-radius:8px;padding:9px 14px;border:1px solid var(--verde);background:var(--verde);color:#fff;}
  .btn.ghost{background:#fff;color:var(--verde);}
  .count{margin-left:auto;font-size:12.5px;color:var(--gris);font-weight:600;}

  .table-wrap{background:var(--blanco);border:1px solid var(--linea);border-radius:var(--radio);box-shadow:var(--sombra);overflow:auto;max-height:70vh;width:100%;}
  table{border-collapse:separate;border-spacing:0;width:100%;font-size:12.5px;min-width:1200px;}
  thead th{position:sticky;top:0;z-index:2;background:#f8fafb;text-align:left;padding:11px 12px;font-size:11px;text-transform:uppercase;color:var(--gris);border-bottom:1px solid var(--linea);white-space:nowrap;}
  tbody td{padding:10px 12px;border-bottom:1px solid #eef2f4;vertical-align:top;}
  tbody tr:hover td{background:#fbfdfc}
  td.num,th.num{text-align:right;white-space:nowrap;font-variant-numeric:tabular-nums;font-weight:600;}
  tfoot td{position:sticky;bottom:0;background:#f8fafb;font-weight:800;padding:12px;border-top:2px solid var(--linea);}
  
  .clamp{display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;max-width:400px;line-height:1.4;}
  .obs{font-size:11px;color:var(--ambar);margin-top:4px;max-width:400px;}
  .pill{display:inline-block;background:var(--verde-claro);color:var(--verde);padding:3px 8px;border-radius:999px;font-size:11px;font-weight:700;}
  .tag{display:inline-block;background:#eef2ff;color:#3730a3;padding:3px 8px;border-radius:999px;font-size:11px;font-weight:700;}
  .empty{padding:46px;text-align:center;color:var(--gris);}
</style>
</head>
<body>

<header class="topbar">
  <div class="brand">
    <div class="logo">VRI</div>
    <div>
      <h1>Vicerrectoría de Investigación</h1>
      <p>Dashboard Financiero · UdeA</p>
    </div>
  </div>
  <div class="status" id="status">Cargando datos…</div>
</header>

<div class="wrap">
  <nav class="tabs">
    <button class="tab active" data-panel="resumen">Resumen</button>
    <button class="tab" data-panel="ingresos">Ingresos</button>
    <button class="tab" data-panel="egresos">Egresos</button>
  </nav>

  <!-- ============ RESUMEN ============ -->
  <section class="panel active" id="panel-resumen">
    <div class="kpis" id="kpis"></div>
    <div class="cards">
      <div class="card">
        <h3>Egresos por Año <span>Valor Presupuestado</span></h3>
        <div class="chart-box"><canvas id="chart-anios"></canvas></div>
      </div>
      <div class="card">
        <h3>Egresos por Unidad Ejecutora <span>Top dependencias</span></h3>
        <div class="chart-box"><canvas id="chart-unidades"></canvas></div>
      </div>
      <div class="card">
        <h3>Egresos por Tipo <span>Distribución según categoría</span></h3>
        <div class="chart-box"><canvas id="chart-tipos"></canvas></div>
      </div>
      <div class="card">
        <h3>Degradación por Convocatoria <span>Top proyectos SIIU</span></h3>
        <div class="chart-box"><canvas id="chart-conv"></canvas></div>
      </div>
    </div>
  </section>

  <!-- ============ INGRESOS ============ -->
  <section class="panel" id="panel-ingresos">
    <div class="toolbar">
      <label for="ing-vig">Vigencia</label>
      <select id="ing-vig"></select>
      <input type="search" id="ing-q" placeholder="Buscar por concepto, documento, tipo…" />
      <button class="btn ghost" id="ing-csv">Descargar CSV</button>
      <span class="count" id="ing-count"></span>
    </div>
    <div class="table-wrap" id="ing-table"></div>
  </section>

  <!-- ============ EGRESOS ============ -->
  <section class="panel" id="panel-egresos">
    <div class="toolbar">
      <label>Año Desde</label>
      <select id="egr-anio-desde"></select>
      <label>Hasta</label>
      <select id="egr-anio-hasta"></select>
      
      <label>Unidad</label>
      <select id="egr-unidad"></select>
      
      <label>Tipo</label>
      <select id="egr-tipo"></select>
      
      <label>Convocatoria</label>
      <select id="egr-conv"></select>
      
      <input type="search" id="egr-q" placeholder="Buscar por beneficiario, objeto…" />
      <button class="btn ghost" id="egr-csv">Descargar CSV</button>
      <span class="count" id="egr-count"></span>
    </div>
    <div class="table-wrap" id="egr-table"></div>
  </section>
</div>

<script>
/* =========================================================
   1) CONFIGURACIÓN — Pega aquí tu URL de Apps Script
   ========================================================= */
const API_URL = 'https://script.google.com/macros/s/XXXXXXXXXXXXXXXXXXXXXXXX/exec';

/* =========================================================
   2) UTILIDADES
   ========================================================= */
const fmtCOP = new Intl.NumberFormat('es-CO',{style:'currency',currency:'COP',maximumFractionDigits:0});
const fmtNum = new Intl.NumberFormat('es-CO');
const PALETTE = ['#046A38','#0b8a4c','#2fa36b','#66c08f','#a3d9bb','#1d4ed8','#b45309','#b91c1c','#7c3aed','#0891b2'];

const $ = (id) => document.getElementById(id);
const esc = (s) => String(s == null ? '' : s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const sum = (arr, fn) => arr.reduce((a, r) => a + (Number(fn(r)) || 0), 0);
const pct = (a, b) => (b ? (a / b * 100).toFixed(1) + '%' : '—');

function compact(n){
  n = Number(n) || 0; const s = n < 0 ? '-' : ''; const a = Math.abs(n);
  if (a >= 1e9) return s + '$' + (a/1e9).toFixed(1) + ' mil M';
  if (a >= 1e6) return s + '$' + (a/1e6).toFixed(0) + ' M';
  if (a >= 1e3) return s + '$' + (a/1e3).toFixed(0) + ' K';
  return s + '$' + a.toFixed(0);
}

function uniqSorted(vals){
  return [...new Set(vals.map(v => String(v == null ? '' : v).trim()).filter(v => v && v !== 'NA'))]
    .sort((a, b) => a.localeCompare(b, 'es', {numeric:true}));
}

function groupSum(rows, keyFn, valFn){
  const m = new Map();
  rows.forEach(r => {
    const k = String(keyFn(r) || '(sin dato)').trim() || '(sin dato)';
    m.set(k, (m.get(k) || 0) + (Number(valFn(r)) || 0));
  });
  return [...m.entries()].sort((a, b) => b[1] - a[1]);
}

function loadJSONP(url){
  return new Promise((resolve, reject) => {
    const cb = 'vri_cb_' + Math.random().toString(36).slice(2);
    const sep = url.indexOf('?') === -1 ? '?' : '&';
    const script = document.createElement('script');
    let done = false;
    const timer = setTimeout(() => { if (!done){ cleanup(); reject(new Error('Tiempo de espera agotado')); } }, 30000);
    function cleanup(){ done = true; clearTimeout(timer); try { delete window[cb]; } catch(e) {} script.remove(); }
    window[cb] = (payload) => { cleanup(); resolve(payload); };
    script.onerror = () => { cleanup(); reject(new Error('No se pudo conectar con Apps Script')); };
    script.src = url + sep + 'callback=' + cb + '&t=' + Date.now();
    document.body.appendChild(script);
  });
}

function downloadCSV(filename, headers, rows){
  const q = v => '"' + String(v == null ? '' : v).replace(/"/g, '""') + '"';
  const csv = [headers.map(q).join(';')].concat(rows.map(r => r.map(q).join(';'))).join('\r\n');
  const blob = new Blob(['\ufeff' + csv], {type:'text/csv;charset=utf-8;'});
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob); a.download = filename;
  document.body.appendChild(a); a.click(); a.remove();
  setTimeout(() => URL.revokeObjectURL(a.href), 1500);
}

/* =========================================================
   3) ESTADO GLOBAL
   ========================================================= */
let DATA = { ingresos: [], egresos: [] };
const charts = {};

document.addEventListener('DOMContentLoaded', init);

async function init(){
  setupTabs();
  try{
    const res = await loadJSONP(API_URL);
    if (!res || !res.ok) throw new Error((res && res.error) || 'Error al cargar');
    DATA = res.data || { ingresos: [], egresos: [] };
    buildFilters();
    renderAll();
    $('status').textContent = 'Actualizado: ' + new Date().toLocaleString('es-CO');
  }catch(err){
    $('status').textContent = '⚠ ' + err.message;
    $('status').style.background = 'rgba(185,28,28,.9)';
    $('kpis').innerHTML = '<div class="card empty">No se pudieron cargar los datos. Revisa la conexión con Apps Script.</div>';
  }
}

function setupTabs(){
  document.querySelectorAll('.tab').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.tab').forEach(b => b.classList.remove('active'));
      document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      $('panel-' + btn.dataset.panel).classList.add('active');
    });
  });
}

/* =========================================================
   4) FILTROS
   ========================================================= */
function fillSelect(id, values, placeholder){
  const sel = $(id);
  sel.innerHTML = '<option value="">' + placeholder + '</option>' + values.map(v => '<option value="' + esc(v) + '">' + esc(v) + '</option>').join('');
}

function buildFilters(){
  // Ingresos
  fillSelect('ing-vig', uniqSorted(DATA.ingresos.map(r => r.vigencia)), 'Todas');
  
  // Egresos
  const anios = uniqSorted(DATA.egresos.map(r => r.anio));
  fillSelect('egr-anio-desde', anios, 'Min');
  fillSelect('egr-anio-hasta', anios, 'Max');
  fillSelect('egr-unidad', uniqSorted(DATA.egresos.map(r => r.unidadEjecutora)), 'Todas');
  fillSelect('egr-tipo', uniqSorted(DATA.egresos.map(r => r.tipo)), 'Todos');
  fillSelect('egr-conv', uniqSorted(DATA.egresos.map(r => r.codigoProyecto)), 'Todas');

  // Eventos
  $('ing-vig').addEventListener('change', renderIngresos);
  $('ing-q').addEventListener('input', renderIngresos);
  ['egr-anio-desde','egr-anio-hasta','egr-unidad','egr-tipo','egr-conv'].forEach(id => $(id).addEventListener('change', renderEgresos));
  $('egr-q').addEventListener('input', renderEgresos);
  
  $('ing-csv').addEventListener('click', exportIngresos);
  $('egr-csv').addEventListener('click', exportEgresos);
}

/* =========================================================
   5) RENDERIZADO GENERAL Y KPIs
   ========================================================= */
function renderAll(){
  renderKPIs();
  renderCharts();
  renderIngresos();
  renderEgresos();
}

function renderKPIs(){
  // Ingresos
  const ingProyectado = sum(DATA.ingresos, r => r.valor);
  const ingEfectivo = sum(DATA.ingresos, r => r.valor); // Asumiendo que se usa el mismo valor por ahora
  
  // Egresos (considerando todos los registros generales para el resumen)
  const egrPresupuestado = sum(DATA.egresos, r => r.valorAprobado);
  const egrEjecutado = sum(DATA.egresos, r => r.valorDesembolsado) + sum(DATA.egresos, r => r.valorComprometido);

  const cards = [
    {lbl:'Proyección de ingresos', val:fmtCOP.format(ingProyectado), sub:'Monto aprobado', tone:'verde'},
    {lbl:'Ingresos efectivos',     val:fmtCOP.format(ingEfectivo), sub:'Registrados en el sistema', tone:'verde'},
    {lbl:'Total presupuestado',    val:fmtCOP.format(egrPresupuestado), sub:'Monto Aprobado por CODI', tone:'azul'},
    {lbl:'Total ejecutado',        val:fmtCOP.format(egrEjecutado), sub:'Incluye montos aprobados, desembolsados y comprometidos', tone:'ambar'}
  ];

  $('kpis').innerHTML = cards.map(c => `
    <div class="kpi ${c.tone}">
      <div class="lbl">${esc(c.lbl)}</div>
      <div class="val">${esc(c.val)}</div>
      <div class="sub">${esc(c.sub)}</div>
    </div>
  `).join('');
}

/* =========================================================
   6) GRÁFICAS
   ========================================================= */
function makeChart(id, config){
  if (charts[id]) charts[id].destroy();
  charts[id] = new Chart($(id).getContext('2d'), config);
}

function renderCharts(){
  const moneyTip = { callbacks: { label: c => ' ' + fmtCOP.format(c.raw) } };
  const baseOpts = {
    responsive:true, maintainAspectRatio:false,
    plugins:{ legend:{position:'bottom', labels:{boxWidth:11, font:{size:11}}}, tooltip: moneyTip },
    scales:{ x:{ grid:{display:false} }, y:{ grid:{color:'#eef2f4'}, ticks:{ callback:v => compact(v) } } }
  };

  // Egresos por Año
  const anios = groupSum(DATA.egresos, r => r.anio, r => r.valorAprobado).sort((a,b) => a[0].localeCompare(b[0]));
  makeChart('chart-anios', {
    type:'bar',
    data:{ labels: anios.map(d => d[0]), datasets:[{ label:'Aprobado', data: anios.map(d => d[1]), backgroundColor:'#0b8a4c', borderRadius:6 }] },
    options: Object.assign({}, baseOpts, { plugins:{ legend:{display:false}, tooltip: moneyTip } })
  });

  // Egresos por Unidad Ejecutora
  const unis = groupSum(DATA.egresos, r => r.unidadEjecutora, r => r.valorAprobado).slice(0, 8).reverse();
  makeChart('chart-unidades', {
    type:'bar',
    data:{ labels: unis.map(d => d[0]), datasets:[{ label:'Aprobado', data: unis.map(d => d[1]), backgroundColor:'#1d4ed8', borderRadius:6 }] },
    options: { indexAxis:'y', responsive:true, maintainAspectRatio:false, plugins:{ legend:{display:false}, tooltip: moneyTip } }
  });

  // Egresos por Tipo
  const tipos = groupSum(DATA.egresos, r => r.tipo, r => r.valorAprobado).slice(0, 8).reverse();
  makeChart('chart-tipos', {
    type:'bar',
    data:{ labels: tipos.map(d => d[0]), datasets:[{ label:'Aprobado', data: tipos.map(d => d[1]), backgroundColor:'#b45309', borderRadius:6 }] },
    options: { indexAxis:'y', responsive:true, maintainAspectRatio:false, plugins:{ legend:{display:false}, tooltip: moneyTip } }
  });

  // Degradación por Convocatoria
  const convs = groupSum(DATA.egresos, r => r.codigoProyecto, r => r.valorAprobado).slice(0, 8).reverse();
  makeChart('chart-conv', {
    type:'bar',
    data:{ labels: convs.map(d => d[0]), datasets:[{ label:'Aprobado', data: convs.map(d => d[1]), backgroundColor:'#7c3aed', borderRadius:6 }] },
    options: { indexAxis:'y', responsive:true, maintainAspectRatio:false, plugins:{ legend:{display:false}, tooltip: moneyTip } }
  });
}

/* =========================================================
   7) TABLA DE INGRESOS (TODAS LAS COLUMNAS)
   ========================================================= */
function filteredIngresos(){
  const vig = $('ing-vig').value;
  const q = ($('ing-q').value || '').toLowerCase().trim();
  return DATA.ingresos.filter(r => {
    if (vig && String(r.vigencia) !== vig) return false;
    if (!q) return true;
    return [r.nombre, r.concepto, r.documento, r.tipoDocumento, r.observaciones].join(' ').toLowerCase().includes(q);
  });
}

function renderIngresos(){
  const rows = filteredIngresos();
  const total = sum(rows, r => r.valor);
  $('ing-count').textContent = fmtNum.format(rows.length) + ' registros · ' + fmtCOP.format(total);

  if (!rows.length){
    $('ing-table').innerHTML = '<div class="empty">No hay ingresos que coincidan con los filtros.</div>';
    return;
  }

  const body = rows.map(r => `
    <tr>
      <td>${esc(r.codigo)}</td>
      <td><span class="pill">${esc(r.nombre)}</span></td>
      <td>${esc(r.codigoNombre)}</td>
      <td>${esc(r.vigencia)}</td>
      <td><div class="clamp" title="${esc(r.concepto)}">${esc(r.concepto)}</div></td>
      <td>${esc(r.tii)}</td>
      <td>${esc(r.fechaTI)}</td>
      <td>${esc(r.tipoDocumento)}</td>
      <td>${esc(r.documento)}</td>
      <td>${esc(r.fecha)}</td>
      <td class="num">${fmtCOP.format(r.valor)}</td>
      <td>${esc(r.unidadEjecutora)}</td>
      <td>${esc(r.unidadPaga)}</td>
      <td>${esc(r.conciliacion)}</td>
      <td><div class="obs">${esc(r.observaciones)}</div></td>
    </tr>`).join('');

  $('ing-table').innerHTML = `
    <table>
      <thead><tr>
        <th>Cód.</th><th>Nombre ingreso</th><th>Cód. Nombre</th><th>Vigencia</th>
        <th>Concepto</th><th>TII</th><th>Fecha TI</th><th>Tipo Doc.</th>
        <th>Documento</th><th>Fecha</th><th class="num">Valor</th><th>Unidad Ejec.</th>
        <th>Unidad Paga</th><th>Conciliación SAP</th><th>Obs.</th>
      </tr></thead>
      <tbody>${body}</tbody>
      <tfoot><tr>
        <td colspan="10">Total (${fmtNum.format(rows.length)} registros)</td>
        <td class="num">${fmtCOP.format(total)}</td>
        <td colspan="4"></td>
      </tr></tfoot>
    </table>`;
}

function exportIngresos(){
  const rows = filteredIngresos();
  downloadCSV('ingresos_vri.csv',
    ['Código','Nombre','Código Nombre','Vigencia','Concepto','TII','Fecha TI','Tipo Doc','Documento','Fecha','Valor','Unidad Ejecutora','Unidad Paga','Conciliación SAP','Observaciones'],
    rows.map(r => [r.codigo, r.nombre, r.codigoNombre, r.vigencia, r.concepto, r.tii, r.fechaTI, r.tipoDocumento, r.documento, r.fecha, r.valor, r.unidadEjecutora, r.unidadPaga, r.conciliacion, r.observaciones]));
}

/* =========================================================
   8) TABLA DE EGRESOS (CON FILTROS AVANZADOS)
   ========================================================= */
function filteredEgresos(){
  const desde = $('egr-anio-desde').value;
  const hasta = $('egr-anio-hasta').value;
  const uni = $('egr-unidad').value;
  const tipo = $('egr-tipo').value;
  const conv = $('egr-conv').value;
  const q = ($('egr-q').value || '').toLowerCase().trim();

  return DATA.egresos.filter(r => {
    const anio = Number(r.anio);
    if (desde && anio < Number(desde)) return false;
    if (hasta && anio > Number(hasta)) return false;
    if (uni && String(r.unidadEjecutora) !== uni) return false;
    if (tipo && String(r.tipo) !== tipo) return false;
    if (conv && String(r.codigoProyecto) !== conv) return false;
    if (!q) return true;
    return [r.nombreBenef, r.objeto, r.evento, r.ciudad, r.nombre, r.observaciones].join(' ').toLowerCase().includes(q);
  });
}

function renderEgresos(){
  const rows = filteredEgresos();
  const tApr = sum(rows, r => r.valorAprobado);
  const tDes = sum(rows, r => r.valorDesembolsado);
  const tCom = sum(rows, r => r.valorComprometido);
  $('egr-count').textContent = fmtNum.format(rows.length) + ' registros';

  if (!rows.length){
    $('egr-table').innerHTML = '<div class="empty">No hay egresos que coincidan con los filtros.</div>';
    return;
  }

  const body = rows.map(r => `
    <tr>
      <td>${esc(r.anio)}</td>
      <td><span class="tag">${esc(r.tipo)}</span></td>
      <td>${esc(r.unidadEjecutora)}</td>
      <td>${esc(r.codigoProyecto)}</td>
      <td><b>${esc(r.nombreBenef)}</b></td>
      <td><div class="clamp" title="${esc(r.objeto)}">${esc(r.objeto)}</div></td>
      <td><div class="clamp" title="${esc(r.evento)}">${esc(r.evento)}</div></td>
      <td class="num">${fmtCOP.format(r.valorAprobado)}</td>
      <td class="num">${fmtCOP.format(r.valorDesembolsado)}</td>
      <td class="num">${fmtCOP.format(r.valorComprometido)}</td>
    </tr>`).join('');

  $('egr-table').innerHTML = `
    <table>
      <thead><tr>
        <th>Año</th><th>Tipo</th><th>Unidad Ejecutora</th><th>Convocatoria (SIIU)</th>
        <th>Beneficiario</th><th>Objeto</th><th>Evento</th>
        <th class="num">Aprobado</th><th class="num">Desembolsado</th><th class="num">Comprometido</th>
      </tr></thead>
      <tbody>${body}</tbody>
      <tfoot><tr>
        <td colspan="7">Total (${fmtNum.format(rows.length)} registros)</td>
        <td class="num">${fmtCOP.format(tApr)}</td>
        <td class="num">${fmtCOP.format(tDes)}</td>
        <td class="num">${fmtCOP.format(tCom)}</td>
      </tr></tfoot>
    </table>`;
}

function exportEgresos(){
  const rows = filteredEgresos();
  downloadCSV('egresos_vri.csv',
    ['Año','Tipo','Unidad Ejecutora','Convocatoria','Beneficiario','Objeto','Evento','Aprobado','Desembolsado','Comprometido'],
    rows.map(r => [r.anio, r.tipo, r.unidadEjecutora, r.codigoProyecto, r.nombreBenef, r.objeto, r.evento, r.valorAprobado, r.valorDesembolsado, r.valorComprometido]));
}
</script>
</body>
</html>
