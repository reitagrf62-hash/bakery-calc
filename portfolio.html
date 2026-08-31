<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
  <title>股市資產配置與成長預測 Pro</title>
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  
  <!-- 引入 Chart.js -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

  <style>
    :root {
      --bg: #f2f2f7;
      --card-bg: #ffffff;
      --text: #1c1c1e;
      --sub: #8e8e93;
      --accent: #007aff;
      --success: #34c759;
      --danger: #ff3b30;
      --border: #e5e5ea;
      --radius: 16px;
      --shadow: 0 4px 16px rgba(0,0,0,0.06);
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", "Segoe UI", Roboto, sans-serif;
      background-color: var(--bg);
      color: var(--text);
      margin: 0;
      padding: 16px;
      padding-top: calc(16px + env(safe-area-inset-top));
      padding-bottom: calc(30px + env(safe-area-inset-bottom));
      -webkit-font-smoothing: antialiased;
    }

    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 16px;
    }
    h1 { font-size: 22px; font-weight: 700; margin: 0; letter-spacing: -0.5px; }

    /* 主卡片 (Hero Card) */
    .hero-card {
      background: linear-gradient(135deg, #007aff, #0056b3);
      color: white;
      border-radius: var(--radius);
      padding: 20px;
      margin-bottom: 16px;
      box-shadow: 0 8px 24px rgba(0,122,255,0.25);
    }
    .hero-title { font-size: 13px; opacity: 0.85; font-weight: 500; }
    .hero-amount { font-size: 32px; font-weight: 800; margin: 4px 0 14px 0; letter-spacing: -0.5px; }
    .hero-rate-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: rgba(255, 255, 255, 0.15);
      padding: 8px 12px;
      border-radius: 10px;
      font-size: 13px;
    }
    .hero-rate-row input {
      width: 55px;
      background: transparent;
      border: none;
      color: white;
      font-weight: 700;
      text-align: right;
      font-size: 14px;
    }

    /* 分頁切換 (Segmented Control) */
    .segmented-control {
      display: flex;
      background: #e3e3e8;
      border-radius: 10px;
      padding: 2px;
      margin-bottom: 16px;
    }
    .segment-btn {
      flex: 1;
      padding: 8px 0;
      border: none;
      background: transparent;
      font-size: 13px;
      font-weight: 600;
      color: var(--sub);
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.2s;
    }
    .segment-btn.active {
      background: white;
      color: var(--text);
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }

    /* 通用卡片 */
    .card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 16px;
      margin-bottom: 16px;
      box-shadow: var(--shadow);
    }
    .card-title { font-size: 16px; font-weight: 700; margin-bottom: 12px; }

    /* 股票清單與表單 */
    .stock-card {
      background: var(--card-bg);
      border-radius: 14px;
      padding: 14px;
      margin-bottom: 12px;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }
    .stock-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }
    .stock-symbol { font-size: 16px; font-weight: 700; }
    .badge { font-size: 10px; padding: 2px 6px; border-radius: 4px; font-weight: 700; margin-left: 6px; }
    .badge-twd { background: #e8f5e9; color: #2e7d32; }
    .badge-usd { background: #e3f2fd; color: #1565c0; }

    .input-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 8px; }
    .field { display: flex; flex-direction: column; }
    .field label { font-size: 11px; color: var(--sub); margin-bottom: 4px; }
    input, select {
      padding: 8px 10px;
      border: 1px solid var(--border);
      border-radius: 8px;
      font-size: 14px;
      background: #fafafa;
    }
    input:focus { border-color: var(--accent); outline: none; background: #fff; }

    .status-bar {
      margin-top: 10px;
      padding-top: 8px;
      border-top: 1px solid #f0f0f0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 13px;
    }

    /* 建議與分析清單 */
    .advice-item {
      padding: 10px 12px;
      border-radius: 10px;
      background: #f8f9fa;
      margin-bottom: 8px;
      font-size: 13px;
      line-height: 1.4;
    }

    .btn-add {
      background: var(--accent);
      color: white;
      border: none;
      padding: 8px 14px;
      border-radius: 20px;
      font-size: 13px;
      font-weight: 600;
      cursor: pointer;
    }
    .btn-delete {
      background: #ffe5e5;
      color: var(--danger);
      border: none;
      padding: 4px 8px;
      border-radius: 6px;
      font-size: 11px;
      font-weight: 600;
    }

    /* Modal 視窗 */
    .modal {
      display: none;
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.4);
      backdrop-filter: blur(4px);
      align-items: center;
      justify-content: center;
      z-index: 999;
    }
    .modal-content {
      background: white;
      width: 85%;
      max-width: 340px;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    .tab-content { display: none; }
    .tab-content.active { display: block; }
  </style>
</head>
<body>

  <div class="header">
    <h1>股市資產配置</h1>
    <button class="btn-add" onclick="openModal()">+ 新增標的</button>
  </div>

  <!-- 總資產概覽 -->
  <div class="hero-card">
    <div class="hero-title">估算總資產 (TWD)</div>
    <div class="hero-amount" id="totalAsset">NT$ 0</div>
    <div class="hero-rate-row">
      <span>美金/台幣預設匯率</span>
      <div>
        <span>1 USD = </span>
        <input type="number" id="usdTwd" value="32.0" step="0.1" oninput="calculateAll()">
        <span>TWD</span>
      </div>
    </div>
  </div>

  <!-- 頁籤控制 -->
  <div class="segmented-control">
    <button class="segment-btn active" onclick="switchTab('portfolio')">持股明細</button>
    <button class="segment-btn" onclick="switchTab('rebalance')">調整建議</button>
    <button class="segment-btn" onclick="switchTab('forecast')">資產增長預測</button>
  </div>

  <!-- Tab 1: 持股明細與配比圓餅圖 -->
  <div id="tab-portfolio" class="tab-content active">
    <div class="card" style="height: 200px; padding: 10px;">
      <canvas id="pieChart"></canvas>
    </div>
    <div id="stockList"></div>
  </div>

  <!-- Tab 2: 算量與再平衡建議 -->
  <div id="tab-rebalance" class="tab-content">
    <div class="card">
      <div class="card-title">動態調倉與加減碼建議</div>
      <div id="adviceList"></div>
    </div>
  </div>

  <!-- Tab 3: 長期資產預測與成長曲線 -->
  <div id="tab-forecast" class="tab-content">
    <div class="card">
      <div class="card-title">未來 20 年複利試算模型</div>
      <div class="input-grid" style="grid-template-columns: 1fr 1fr; margin-bottom: 12px;">
        <div class="field">
          <label>每年預計投入 (TWD)</label>
          <input type="number" id="forecastInput" value="120000" step="10000">
        </div>
        <div class="field">
          <label>預期年化報酬率 (%)</label>
          <input type="number" id="forecastRoi" value="7" step="0.5">
        </div>
      </div>
      <button class="btn-add" style="width: 100%; padding: 10px; border-radius: 10px;" onclick="runForecast()">試算成長曲線</button>
      
      <div style="height: 220px; margin-top: 15px;">
        <canvas id="forecastChart"></canvas>
      </div>
    </div>
  </div>

  <!-- 新增標的彈出 Modal -->
  <div class="modal" id="addModal">
    <div class="modal-content">
      <h3 style="margin-top:0; margin-bottom: 12px;">新增股票標的</h3>
      <div class="field" style="margin-bottom: 8px;">
        <label>代號 / 名稱</label>
        <input type="text" id="newCode" placeholder="如 2330 或 VT">
      </div>
      <div class="field" style="margin-bottom: 8px;">
        <label>市場類型</label>
        <select id="newMarket">
          <option value="TWD">台股 (TWD)</option>
          <option value="USD">美股 (USD)</option>
        </select>
      </div>
      <div class="input-grid" style="margin-bottom: 16px;">
        <div class="field">
          <label>現價</label>
          <input type="number" id="newPrice" placeholder="金額">
        </div>
        <div class="field">
          <label>持股數</label>
          <input type="number" id="newShares" placeholder="股數">
        </div>
        <div class="field">
          <label>目標 %</label>
          <input type="number" id="newTarget" placeholder="%">
        </div>
      </div>
      <div style="display:flex; gap: 8px;">
        <button class="btn-add" style="flex:1; background:#e5e5ea; color:var(--text);" onclick="closeModal()">取消</button>
        <button class="btn-add" style="flex:1;" onclick="addStock()">確認新增</button>
      </div>
    </div>
  </div>

  <script>
    const defaultStocks = [
      { id: '2330 台積電', market: 'TWD', price: 980, shares: 1000, targetRatio: 40 },
      { id: '0050 元大台灣50', market: 'TWD', price: 175, shares: 3000, targetRatio: 30 },
      { id: 'VT 全球股票', market: 'USD', price: 110, shares: 250, targetRatio: 30 }
    ];

    let stocks = JSON.parse(localStorage.getItem('my_ultimate_portfolio')) || defaultStocks;
    let pieChart = null;
    let forecastChart = null;

    function saveData() { localStorage.setItem('my_ultimate_portfolio', JSON.stringify(stocks)); }

    function switchTab(tabName) {
      document.querySelectorAll('.tab-content').forEach(el => el.classList.remove('active'));
      document.querySelectorAll('.segment-btn').forEach(el => el.classList.remove('active'));
      
      document.getElementById(`tab-${tabName}`).classList.add('active');
      event.target.classList.add('active');

      if(tabName === 'forecast') runForecast();
    }

    function openModal() { document.getElementById('addModal').style.display = 'flex'; }
    function closeModal() { document.getElementById('addModal').style.display = 'none'; }

    function addStock() {
      const code = document.getElementById('newCode').value.trim();
      const market = document.getElementById('newMarket').value;
      const price = parseFloat(document.getElementById('newPrice').value) || 0;
      const shares = parseFloat(document.getElementById('newShares').value) || 0;
      const targetRatio = parseFloat(document.getElementById('newTarget').value) || 0;

      if (!code || !price) { alert('請填寫完整資訊'); return; }

      stocks.push({ id: code, market, price, shares, targetRatio });
      saveData();
      renderHtml();
      calculateAll();
      closeModal();

      document.getElementById('newCode').value = '';
      document.getElementById('newPrice').value = '';
      document.getElementById('newShares').value = '';
      document.getElementById('newTarget').value = '';
    }

    function deleteStock(index) {
      if (confirm(`確定要刪除 ${stocks[index].id} 嗎？`)) {
        stocks.splice(index, 1);
        saveData();
        renderHtml();
        calculateAll();
      }
    }

    function updateStock(index, field, value) {
      stocks[index][field] = parseFloat(value) || 0;
      saveData();
      calculateAll();
    }

    function renderHtml() {
      const container = document.getElementById('stockList');
      container.innerHTML = '';

      stocks.forEach((s, index) => {
        const badgeClass = s.market === 'USD' ? 'badge-usd' : 'badge-twd';
        container.innerHTML += `
          <div class="stock-card">
            <div class="stock-header">
              <div>
                <span class="stock-symbol">${s.id}</span>
                <span class="badge ${badgeClass}">${s.market}</span>
              </div>
              <button class="btn-delete" onclick="deleteStock(${index})">刪除</button>
            </div>
            <div class="input-grid">
              <div class="field"><label>現價</label><input type="number" value="${s.price}" oninput="updateStock(${index}, 'price', this.value)"></div>
              <div class="field"><label>股數</label><input type="number" value="${s.shares}" oninput="updateStock(${index}, 'shares', this.value)"></div>
              <div class="field"><label>目標 %</label><input type="number" value="${s.targetRatio}" oninput="updateStock(${index}, 'targetRatio', this.value)"></div>
            </div>
            <div class="status-bar">
              <span style="color:var(--sub)" id="val-${index}">市值: -</span>
              <span style="font-weight:700" id="status-${index}">-</span>
            </div>
          </div>
        `;
      });
    }

    let currentTotalTwd = 0;

    function calculateAll() {
      const usdTwd = parseFloat(document.getElementById('usdTwd').value) || 32;
      currentTotalTwd = 0;

      stocks.forEach(s => {
        let twdValue = s.shares * s.price;
        if (s.market === 'USD') twdValue *= usdTwd;
        s.currentTwdValue = twdValue;
        currentTotalTwd += twdValue;
      });

      document.getElementById('totalAsset').innerText = `NT$ ${Math.round(currentTotalTwd).toLocaleString()}`;

      let adviceHtml = '';
      let labels = [];
      let pieData = [];

      stocks.forEach((s, index) => {
        const ratio = currentTotalTwd > 0 ? (s.currentTwdValue / currentTotalTwd) * 100 : 0;
        const diff = ratio - s.targetRatio;
        const diffAmt = (currentTotalTwd * (s.targetRatio / 100)) - s.currentTwdValue;

        labels.push(s.id);
        pieData.push(Math.round(s.currentTwdValue));

        document.getElementById(`val-${index}`).innerText = `市值: NT$ ${Math.round(s.currentTwdValue).toLocaleString()} (${ratio.toFixed(1)}%)`;

        const statusElem = document.getElementById(`status-${index}`);
        if (diff > 3) {
          statusElem.innerText = `偏高 (+${diff.toFixed(1)}%)`;
          statusElem.style.color = 'var(--danger)';
          adviceHtml += `<div class="advice-item">⚠️ <b>${s.id}</b> 佔比偏高 (${ratio.toFixed(1)}%)，建議暫緩買進或適度賣出約 <b>NT$ ${Math.round(Math.abs(diffAmt)).toLocaleString()}</b>。</div>`;
        } else if (diff < -3) {
          statusElem.innerText = `偏低 (${diff.toFixed(1)}%)`;
          statusElem.style.color = 'var(--success)';
          adviceHtml += `<div class="advice-item">💡 <b>${s.id}</b> 佔比偏低 (${ratio.toFixed(1)}%)，建議優先加碼買進約 <b>NT$ ${Math.round(diffAmt).toLocaleString()}</b>。</div>`;
        } else {
          statusElem.innerText = '完美平衡';
          statusElem.style.color = 'var(--sub)';
        }
      });

      if (!adviceHtml) adviceHtml = '<div class="advice-item">✅ 資產比例非常理想，維持定期定額即可！</div>';
      document.getElementById('adviceList').innerHTML = adviceHtml;

      renderPieChart(labels, pieData);
    }

    function renderPieChart(labels, data) {
      const ctx = document.getElementById('pieChart').getContext('2d');
      if (pieChart) pieChart.destroy();

      pieChart = new Chart(ctx, {
        type: 'doughnut',
        data: {
          labels: labels,
          datasets: [{
            data: data,
            backgroundColor: ['#007aff', '#34c759', '#ff9500', '#af52de', '#ff3b30', '#5856d6']
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { position: 'right', labels: { boxWidth: 10, font: { size: 11 } } } }
        }
      });
    }

    function runForecast() {
      const annualInput = parseFloat(document.getElementById('forecastInput').value) || 0;
      const roi = (parseFloat(document.getElementById('forecastRoi').value) || 0) / 100;
      const years = 20;
      
      let labels = [];
      let dataCost = [];
      let dataValue = [];
      
      let runningTotal = currentTotalTwd;
      let runningCost = currentTotalTwd;
      const currentYear = new Date().getFullYear();

      for (let y = 0; y <= years; y++) {
        labels.push(`${currentYear + y}`);
        dataCost.push(Math.round(runningCost));
        dataValue.push(Math.round(runningTotal));
        runningTotal = (runningTotal * (1 + roi)) + annualInput;
        runningCost += annualInput;
      }

      const ctx = document.getElementById('forecastChart').getContext('2d');
      if (forecastChart) forecastChart.destroy();

      forecastChart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: labels,
          datasets: [{
            label: '預估總資產',
            data: dataValue,
            borderColor: '#007aff',
            backgroundColor: 'rgba(0,122,255,0.1)',
            fill: true,
            tension: 0.3
          }, {
            label: '累計投入成本',
            data: dataCost,
            borderColor: '#8e8e93',
            borderDash: [4, 4],
            tension: 0
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: { legend: { position: 'bottom' } },
          scales: {
            x: { grid: { display: false } },
            y: { ticks: { callback: v => (v/10000) + '萬' } }
          }
        }
      });
    }

    // 頁面初始化
    renderHtml();
    calculateAll();
  </script>
</body>
</html>
