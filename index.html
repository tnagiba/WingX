<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>WingX Operator Dashboard</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body { margin:0; font-family: Arial; background:#070A12; color:white; }
    .container { max-width:1200px; margin:auto; padding:20px; }
    .card { background:rgba(255,255,255,0.05); border:1px solid rgba(255,255,255,0.1); border-radius:16px; padding:20px; margin-bottom:20px; }
    h1 { font-size:32px; margin-bottom:10px; }
    .kpis { display:grid; grid-template-columns:repeat(4,1fr); gap:12px; }
    .kpi { background:rgba(255,255,255,0.06); padding:16px; border-radius:12px; }
    select { background:#020617; color:white; padding:8px; border-radius:8px; border:1px solid #333; }
  </style>
</head>
<body>
<div class="container">
  <h1>Where competitor flying is concentrated</h1>
  <p style="color:#94a3b8">Top 10 operators · Hourly band breakdown</p>

  <div class="kpis" id="kpis"></div>

  <div class="card">
    <canvas id="chart"></canvas>
  </div>

  <div class="card">
    <label>Operator Drilldown:</label>
    <select id="operatorSelect"></select>
    <canvas id="pie"></canvas>
  </div>
</div>

<script>
const data = [
  { operator:"flyExclusive", under2:6814, b23:5924, b34:3013, b4:1172 },
  { operator:"Vista America", under2:3750, b23:3790, b34:1638, b4:3515 },
  { operator:"Wheels Up", under2:5398, b23:3328, b34:1444, b4:1131 },
  { operator:"Nicholas Air", under2:2996, b23:1253, b34:398, b4:154 },
  { operator:"Thrive", under2:1222, b23:702, b34:655, b4:1144 },
  { operator:"ATI Jet", under2:1755, b23:1383, b34:442, b4:126 },
  { operator:"Sky Quest", under2:778, b23:1038, b34:87, b4:94 },
  { operator:"Silverhawk", under2:848, b23:726, b34:351, b4:26 },
  { operator:"Kalitta", under2:913, b23:589, b34:260, b4:41 },
  { operator:"Pittsburgh Jet", under2:842, b23:712, b34:91, b4:66 }
];

function total(o){ return o.under2+o.b23+o.b34+o.b4 }

const sorted = data.map(o=>({...o,total:total(o)})).sort((a,b)=>b.total-a.total);

// KPIs
const totalHours = sorted.reduce((s,o)=>s+o.total,0);
const kpisHTML = `
  <div class="kpi"><b>Total Hours</b><br>${Math.round(totalHours)}</div>
  <div class="kpi"><b>Leader</b><br>${sorted[0].operator}</div>
  <div class="kpi"><b>Short Haul %</b><br>${Math.round(sorted.reduce((s,o)=>s+o.under2,0)/totalHours*100)}%</div>
  <div class="kpi"><b>Long Haul %</b><br>${Math.round(sorted.reduce((s,o)=>s+o.b34+o.b4,0)/totalHours*100)}%</div>
`;
document.getElementById('kpis').innerHTML = kpisHTML;

// Bar chart
new Chart(document.getElementById('chart'),{
  type:'bar',
  data:{
    labels:sorted.map(o=>o.operator),
    datasets:[
      {label:'<2h', data:sorted.map(o=>o.under2), backgroundColor:'#22d3ee'},
      {label:'2-3h', data:sorted.map(o=>o.b23), backgroundColor:'#38bdf8'},
      {label:'3-4h', data:sorted.map(o=>o.b34), backgroundColor:'#818cf8'},
      {label:'4h+', data:sorted.map(o=>o.b4), backgroundColor:'#c084fc'}
    ]
  },
  options:{responsive:true, plugins:{legend:{labels:{color:'white'}}}, scales:{x:{ticks:{color:'white'}},y:{ticks:{color:'white'}}}}
});

// Dropdown
const select = document.getElementById('operatorSelect');
sorted.forEach(o=>{
  const opt = document.createElement('option');
  opt.value=o.operator;
  opt.text=o.operator;
  select.appendChild(opt);
});

let pie;
function renderPie(op){
  const o = sorted.find(x=>x.operator===op);
  if(pie) pie.destroy();
  pie = new Chart(document.getElementById('pie'),{
    type:'pie',
    data:{
      labels:['<2h','2-3h','3-4h','4h+'],
      datasets:[{data:[o.under2,o.b23,o.b34,o.b4], backgroundColor:['#22d3ee','#38bdf8','#818cf8','#c084fc']}]
    }
  });
}

select.addEventListener('change',e=>renderPie(e.target.value));
renderPie(sorted[0].operator);

</script>
</body>
</html>
