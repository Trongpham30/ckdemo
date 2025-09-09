<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Stock Game — Enhanced</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lightweight-charts@3.8.0/dist/lightweight-charts.standalone.production.js"></script>
  <style>
    html,body,#app{height:100%}
    .avatar-sm{width:36px;height:36px;border-radius:9999px;object-fit:cover}
    .avatar-lg{width:64px;height:64px;border-radius:9999px;object-fit:cover}
  </style>
</head>
<body class="bg-gradient-to-b from-slate-50 to-slate-100 text-slate-800" id="app">
  <div class="max-w-6xl mx-auto p-4">
    <header class="flex items-center justify-between mb-4">
      <div class="flex items-center gap-3">
        <div class="p-2 bg-white rounded-full shadow"><img src="" id="header-logo" alt="logo" class="w-10 h-10 rounded-full" /></div>
        <div>
          <h1 class="text-xl font-bold">Stock Game — Enhanced</h1>
          <div class="text-xs text-slate-500">Realtime demo — giá cập nhật từng giây · Limit & Stop orders · Avatar người chơi</div>
        </div>
      </div>
      <div id="top-controls" class="flex items-center gap-3"></div>
    </header>

    <main class="grid grid-cols-1 md:grid-cols-4 gap-4">
      <!-- Left: profile + tickers + trade form -->
      <section class="md:col-span-1 bg-white p-4 rounded-lg shadow-sm">
        <div class="flex items-center gap-3">
          <img src="" id="profile-avatar" class="avatar-lg bg-slate-100" alt="avatar" />
          <div>
            <div class="font-semibold" id="ui-username">-</div>
            <div class="text-sm text-slate-500">Tiền: <span id="ui-cash">0</span> ₫</div>
          </div>
        </div>

        <div class="mt-4">
          <label class="block text-sm font-medium">Thay avatar</label>
          <input id="avatar-input" type="file" accept="image/*" class="mt-2" />
        </div>

        <hr class="my-3" />
        <h3 class="font-semibold">Tickers</h3>
        <div id="ticker-list" class="space-y-2 max-h-40 overflow-auto mt-2"></div>

        <div class="mt-4">
          <h3 class="font-semibold">Đặt lệnh</h3>
          <div class="space-y-2 mt-2">
            <select id="trade-ticker" class="w-full p-2 border rounded"></select>
            <div class="grid grid-cols-2 gap-2">
              <input id="trade-qty" type="number" placeholder="Số lượng" class="p-2 border rounded" value="1" />
              <input id="trade-price" type="number" placeholder="Giá (để limit)" class="p-2 border rounded" />
            </div>
            <div class="grid grid-cols-3 gap-2">
              <button id="market-buy" class="p-2 bg-green-500 text-white rounded">Mua MKT</button>
              <button id="limit-buy" class="p-2 bg-emerald-600 text-white rounded">Mua Limit</button>
              <button id="stop-buy" class="p-2 bg-teal-500 text-white rounded">Mua Stop</button>
            </div>
            <div class="grid grid-cols-3 gap-2 mt-2">
              <button id="market-sell" class="p-2 bg-red-500 text-white rounded">Bán MKT</button>
              <button id="limit-sell" class="p-2 bg-rose-600 text-white rounded">Bán Limit</button>
              <button id="stop-sell" class="p-2 bg-fuchsia-500 text-white rounded">Bán Stop</button>
            </div>
            <div class="text-xs text-slate-500 mt-1">Limit: khớp khi có đối ứng. Stop: khi giá đạt stop -> tạo lệnh market.</div>
          </div>
        </div>
      </section>

      <!-- Center: chart + orderbook + history -->
      <section class="md:col-span-2 bg-white p-4 rounded-lg shadow-sm">
        <div class="flex items-center justify-between mb-3">
          <h2 class="font-semibold" id="chart-title">Biểu đồ</h2>
          <div class="flex items-center gap-2">
            <label class="text-sm">Candle (s)</label>
            <input id="candle-interval" type="number" min="1" value="1" class="w-16 p-1 border rounded text-sm" />
          </div>
        </div>
        <div id="chart" style="height:320px;"></div>

        <div class="mt-3 grid grid-cols-1 md:grid-cols-3 gap-3">
          <div class="col-span-1">
            <h4 class="font-semibold">Order Book</h4>
            <div id="order-book" class="max-h-40 overflow-auto text-sm mt-2"></div>
          </div>
          <div class="col-span-1">
            <h4 class="font-semibold">Lệnh của bạn</h4>
            <div id="my-orders" class="max-h-40 overflow-auto text-sm mt-2"></div>
          </div>
          <div class="col-span-1">
            <h4 class="font-semibold">Lịch sử giao dịch</h4>
            <div id="trade-history" class="max-h-40 overflow-auto text-sm mt-2"></div>
          </div>
        </div>
      </section>

      <!-- Right: portfolio + admin -->
      <section class="md:col-span-1 bg-white p-4 rounded-lg shadow-sm">
        <h2 class="font-semibold">Danh mục</h2>
        <div id="portfolio-list" class="mt-2 space-y-2 text-sm"></div>

        <div class="mt-4">
          <button id="btn-logout" class="w-full p-2 bg-gray-700 text-white rounded">Đăng xuất</button>
        </div>

        <hr class="my-4">
        <div>
          <h3 class="font-semibold">Admin</h3>
          <div class="mt-2">
            <input id="admin-pin" type="password" placeholder="Mã PIN admin" class="w-full p-2 border rounded" />
            <button id="admin-login" class="w-full mt-2 p-2 bg-indigo-600 text-white rounded">Đăng nhập admin</button>
          </div>
          <div id="admin-panel" class="mt-3 hidden">
            <h4 class="font-semibold">Quản lý người chơi</h4>
            <div id="admin-players" class="max-h-28 overflow-auto text-sm mt-2"></div>
            <h4 class="font-semibold mt-3">Quản lý tickers</h4>
            <div class="mt-2 space-y-2">
              <input id="new-ticker-code" placeholder="Mã (VD: AAPL)" class="w-full p-2 border rounded" />
              <input id="new-ticker-name" placeholder="Tên" class="w-full p-2 border rounded" />
              <input id="new-ticker-start" placeholder="Giá khởi điểm" class="w-full p-2 border rounded" />
              <div class="grid grid-cols-2 gap-2">
                <button id="add-ticker" class="p-2 bg-green-500 text-white rounded">Thêm</button>
                <button id="reset-data" class="p-2 bg-yellow-500 text-white rounded">Reset</button>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Login modal -->
    <div id="login-modal" class="fixed inset-0 flex items-center justify-center bg-black/40">
      <div class="bg-white p-6 rounded-lg w-full max-w-md">
        <h2 class="text-xl font-semibold mb-3">Đăng nhập / Tạo tài khoản</h2>
        <input id="login-username" placeholder="Tên người chơi" class="w-full p-2 border rounded mb-2" />
        <input id="login-pin" placeholder="Mã PIN (4 số)" class="w-full p-2 border rounded mb-2" />
        <div class="grid grid-cols-2 gap-2">
          <button id="btn-login" class="p-2 bg-blue-600 text-white rounded">Đăng nhập</button>
          <button id="btn-register" class="p-2 bg-green-600 text-white rounded">Tạo tài khoản mới</button>
        </div>
        <p class="text-xs text-slate-500 mt-2">Admin mặc định: PIN <strong id="default-admin-pin">1234</strong> (có thể đổi trong Admin)</p>
      </div>
    </div>

  </div>

  <script>
  /* Enhanced Stock Game - single-file
     - Avatar upload (stored per-user as dataURL in localStorage)
     - Limit & Stop orders + simple orderbook matching
     - UI improvements
  */

  const fmt = n => Number(n).toLocaleString('vi-VN');
  const now = () => new Date().toISOString();
  const DEFAULT_ADMIN_PIN = '1234';
  const DEFAULT_CASH = 100000000;

  const sampleTickers = {
    AAPL: { code:'AAPL', name:'Apple', price:170, vol:0.6 },
    GOOGL:{ code:'GOOGL', name:'Alphabet', price:135, vol:0.8 },
    TSLA:{ code:'TSLA', name:'Tesla', price:250, vol:1.4 }
  };

  function loadState(){
    const s = JSON.parse(localStorage.getItem('sg_state')||'{}');
    if(!s.tickers) s.tickers = sampleTickers;
    if(!s.users) s.users = {};
    if(!s.adminPin) s.adminPin = DEFAULT_ADMIN_PIN;
    if(!s.orders) s.orders = {}; // per-ticker orderbook { bids:[], asks:[] }
    if(!s.stopOrders) s.stopOrders = []; // global stop orders
    if(!s.settings) s.settings = { candleIntervalSec:1 };
    return s;
  }
  function saveState(s){ localStorage.setItem('sg_state', JSON.stringify(s)); }
  let state = loadState();

  // engine: price + candles
  const engine = { series:{}, init(){ for(const [k,v] of Object.entries(state.tickers)){ this.series[k]=this.series[k]||{price:v.price,candles:[]}; this.series[k].price=v.price; } }, step(){ const candleSec = Math.max(1, Number(document.getElementById('candle-interval').value||1)); const bucket = Math.floor(Date.now()/1000 / candleSec) * candleSec; for(const [code,meta] of Object.entries(state.tickers)){ const s = this.series[code]||{price:meta.price,candles:[]}; const vol = meta.vol||1; const changePct = (Math.random()*2-1)*vol/100; const newPrice = Math.max(0.01, s.price * (1+changePct)); if(!s.candles.length || s.candles[s.candles.length-1].time !== bucket){ s.candles.push({ time:bucket, open:s.price, high:newPrice, low:newPrice, close:newPrice }); } else { const c = s.candles[s.candles.length-1]; c.high = Math.max(c.high,newPrice); c.low = Math.min(c.low,newPrice); c.close = newPrice; } s.price = newPrice; this.series[code]=s; } } };
  engine.init();

  // Orderbook structures: orders stored with id, user, side, qty, price (for limit), type ('limit'|'market'), remaining
  function ensureOrderbook(code){ state.orders[code] = state.orders[code] || { bids:[], asks:[] }; }

  // matching: simple price-time priority
  function matchOrder(code){ ensureOrderbook(code); const book = state.orders[code]; // match bids vs asks
    let trades = [];
    // Try to match best bid >= best ask
    while(book.bids.length && book.asks.length){
      const bestBid = book.bids[0];
      const bestAsk = book.asks[0];
      if(bestBid.price < bestAsk.price) break; // no match
      const qty = Math.min(bestBid.remaining, bestAsk.remaining);
      const price = (bestBid.timestamp <= bestAsk.timestamp) ? bestAsk.price : bestBid.price; // price rule: earlier order's price or mid -> choose ask.price to simplify
      // execute
      bestBid.remaining -= qty; bestAsk.remaining -= qty;
      trades.push({ time: now(), code, qty, price, buyUser: bestBid.user, sellUser: bestAsk.user });
      // credit/debit users
      const buyer = state.users[bestBid.user]; const seller = state.users[bestAsk.user];
      buyer.positions = buyer.positions||{}; seller.positions = seller.positions||{};
      buyer.cash -= price*qty; buyer.positions[code] = (buyer.positions[code]||0) + qty;
      seller.cash += price*qty; seller.positions[code] = (seller.positions[code]||0) - qty;
      // remove filled orders
      if(bestBid.remaining <= 0) book.bids.shift();
      if(bestAsk.remaining <= 0) book.asks.shift();
    }
    if(trades.length){ state.lastTrades = state.lastTrades||[]; state.lastTrades.unshift(...trades); if(state.lastTrades.length>200) state.lastTrades.length = 200; saveState(state); }
  }

  // place limit order
  function placeLimitOrder(user,code,side,qty,price){ ensureOrderbook(code); const id = 'o'+Date.now()+'-'+Math.random().toString(36).slice(2,7); const order = { id, user, side, qty, price, remaining:qty, timestamp:Date.now(), type:'limit' }; const book = state.orders[code]; if(side==='buy'){ book.bids.push(order); book.bids.sort((a,b)=>b.price - a.price || a.timestamp - b.timestamp); } else { book.asks.push(order); book.asks.sort((a,b)=>a.price - b.price || a.timestamp - b.timestamp); } saveState(state); matchOrder(code); }

  // place market order -> match immediately against book
  function placeMarketOrder(user,code,side,qty){ ensureOrderbook(code); const book = state.orders[code]; let remaining = qty; const trades = []; if(side==='buy'){ while(remaining>0 && book.asks.length){ const a = book.asks[0]; const q = Math.min(remaining, a.remaining); const price = a.price; remaining -= q; a.remaining -= q; trades.push({ time:now(), code, qty:q, price, buyUser:user, sellUser:a.user }); const buyer = state.users[user]; const seller = state.users[a.user]; buyer.positions = buyer.positions||{}; seller.positions = seller.positions||{}; buyer.cash -= price*q; buyer.positions[code] = (buyer.positions[code]||0)+q; seller.cash += price*q; seller.positions[code] = (seller.positions[code]||0)-q; if(a.remaining<=0) book.asks.shift(); } } else { while(remaining>0 && book.bids.length){ const b = book.bids[0]; const q = Math.min(remaining, b.remaining); const price = b.price; remaining -= q; b.remaining -= q; trades.push({ time:now(), code, qty:q, price, buyUser:b.user, sellUser:user }); const buyer = state.users[b.user]; const seller = state.users[user]; buyer.positions = buyer.positions||{}; seller.positions = seller.positions||{}; buyer.cash -= price*q; buyer.positions[code] = (buyer.positions[code]||0)+q; seller.cash += price*q; seller.positions[code] = (seller.positions[code]||0)-q; if(b.remaining<=0) book.bids.shift(); } }
    if(trades.length){ state.lastTrades = state.lastTrades||[]; state.lastTrades.unshift(...trades); if(state.lastTrades.length>200) state.lastTrades.length = 200; saveState(state); }
  }

  // stop orders: when triggered, convert to market order
  function placeStopOrder(user,code,side,qty,stopPrice){ state.stopOrders = state.stopOrders||[]; state.stopOrders.push({ id:'s'+Date.now(), user, code, side, qty, stopPrice, created:Date.now() }); saveState(state); }
  function evaluateStopOrders(){ const triggered = []; for(const s of (state.stopOrders||[])){ const cur = engine.series[s.code] ? engine.series[s.code].price : state.tickers[s.code].price; if(s.side==='buy' && cur >= s.stopPrice){ triggered.push(s); } if(s.side==='sell' && cur <= s.stopPrice){ triggered.push(s); } }
    for(const t of triggered){ // convert to market order
      placeMarketOrder(t.user, t.code, t.side, t.qty);
      state.stopOrders = state.stopOrders.filter(x=>x.id!==t.id);
    }
    if(triggered.length) saveState(state);
  }

  // UI & session
  let currentUser = null;
  const el = { tickerList:document.getElementById('ticker-list'), tradeTicker:document.getElementById('trade-ticker'), tradeQty:document.getElementById('trade-qty'), tradePrice:document.getElementById('trade-price'), marketBuy:document.getElementById('market-buy'), limitBuy:document.getElementById('limit-buy'), stopBuy:document.getElementById('stop-buy'), marketSell:document.getElementById('market-sell'), limitSell:document.getElementById('limit-sell'), stopSell:document.getElementById('stop-sell'), uiUsername:document.getElementById('ui-username'), uiCash:document.getElementById('ui-cash'), portfolioList:document.getElementById('portfolio-list'), tradeHistory:document.getElementById('trade-history'), chartTitle:document.getElementById('chart-title'), candleInterval:document.getElementById('candle-interval'), loginModal:document.getElementById('login-modal'), loginUsername:document.getElementById('login-username'), loginPin:document.getElementById('login-pin'), btnLogin:document.getElementById('btn-login'), btnRegister:document.getElementById('btn-register'), adminPin:document.getElementById('admin-pin'), adminLogin:document.getElementById('admin-login'), adminPanel:document.getElementById('admin-panel'), adminPlayers:document.getElementById('admin-players'), newTickerCode:document.getElementById('new-ticker-code'), newTickerName:document.getElementById('new-ticker-name'), newTickerStart:document.getElementById('new-ticker-start'), addTicker:document.getElementById('add-ticker'), resetData:document.getElementById('reset-data'), defaultAdminPin:document.getElementById('default-admin-pin'), btnLogout:document.getElementById('btn-logout'), orderBook:document.getElementById('order-book'), myOrders:document.getElementById('my-orders'), profileAvatar:document.getElementById('profile-avatar'), avatarInput:document.getElementById('avatar-input') };
  el.defaultAdminPin.textContent = state.adminPin || DEFAULT_ADMIN_PIN;

  // Chart
  const chart = LightweightCharts.createChart(document.getElementById('chart'));
  const candleSeries = chart.addCandlestickSeries();
  let currentChartTicker = Object.keys(state.tickers)[0];
  function rebuildChartFor(code){ currentChartTicker = code; el.chartTitle.textContent = `Biểu đồ — ${code} ${state.tickers[code].name||''}`; const s = engine.series[code]; const data = (s && s.candles) ? s.candles.map(c=>({ time:c.time, open:c.open, high:c.high, low:c.low, close:c.close })) : []; candleSeries.setData(data); chart.timeScale().fitContent(); }

  // render tickers
  function renderTickers(){ el.tickerList.innerHTML=''; el.tradeTicker.innerHTML=''; Object.keys(state.tickers).sort().forEach(code=>{ const t = state.tickers[code]; const s = engine.series[code]||{price:t.price}; const price = s.price; const div = document.createElement('div'); div.className='flex items-center justify-between p-2 border rounded'; div.innerHTML = `<div><div class="font-semibold">${code} <span class="text-xs text-slate-500">${t.name||''}</span></div><div class="text-sm">Giá: <span class="price-${code}">${fmt(price.toFixed(2))}</span></div></div><div class="flex flex-col gap-1"><button data-code="${code}" class="open-chart p-1 bg-slate-100 rounded text-sm">Mở</button><button data-code="${code}" class="watch p-1 bg-slate-100 rounded text-sm">Chọn</button></div>`; el.tickerList.appendChild(div); const opt = document.createElement('option'); opt.value = code; opt.textContent = code; el.tradeTicker.appendChild(opt); }); }

  function ensureUserExists(username){ state.users = state.users || {}; if(!state.users[username]){ state.users[username] = { cash:DEFAULT_CASH, positions:{}, history:[], avatar:null }; saveState(state); } }
  function loginUser(username,pin){ ensureUserExists(username); currentUser = username; el.loginModal.style.display='none'; renderUI(); }
  function logout(){ currentUser=null; el.loginModal.style.display='flex'; renderUI(); }

  function placeBuyMarket(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); placeMarketOrder(currentUser,code,'buy',qty); renderUI(); }
  function placeSellMarket(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); placeMarketOrder(currentUser,code,'sell',qty); renderUI(); }
  function placeBuyLimit(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); const price = Number(el.tradePrice.value); if(!price) return alert('Nhập giá limit'); placeLimitOrder(currentUser,code,'buy',qty,price); renderUI(); }
  function placeSellLimit(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); const price = Number(el.tradePrice.value); if(!price) return alert('Nhập giá limit'); placeLimitOrder(currentUser,code,'sell',qty,price); renderUI(); }
  function placeBuyStop(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); const stop = Number(el.tradePrice.value); if(!stop) return alert('Nhập giá stop'); placeStopOrder(currentUser,code,'buy',qty,stop); alert('Stop buy đặt thành công'); }
  function placeSellStop(){ if(!currentUser) return alert('Đăng nhập trước'); const code = el.tradeTicker.value; const qty = Number(el.tradeQty.value||1); const stop = Number(el.tradePrice.value); if(!stop) return alert('Nhập giá stop'); placeStopOrder(currentUser,code,'sell',qty,stop); alert('Stop sell đặt thành công'); }

  // Admin
  function adminLogin(pin){ if(pin === state.adminPin){ el.adminPanel.classList.remove('hidden'); renderAdminPlayers(); } else alert('PIN admin sai'); }
  function addTicker(code,name,start){ code=(code||'').toUpperCase().trim(); if(!code) return alert('Mã trống'); state.tickers[code]={ code,name,price:Number(start)||1, vol:1 }; engine.series[code]={ price:Number(start)||1, candles:[] }; saveState(state); renderTickers(); }
  function resetData(){ if(!confirm('Reset toàn bộ dữ liệu?')) return; state = { tickers:sampleTickers, users:{}, adminPin:DEFAULT_ADMIN_PIN, orders:{}, stopOrders:[], settings:{ candleIntervalSec:1 } }; saveState(state); engine.init(); location.reload(); }
  function renderAdminPlayers(){ el.adminPlayers.innerHTML=''; for(const [u,ud] of Object.entries(state.users)){ const div = document.createElement('div'); div.className='p-2 border rounded mb-1 flex items-center justify-between'; div.innerHTML = `<div><div class="font-semibold">${u}</div><div class="text-xs">Tiền: ${fmt(ud.cash)} ₫</div></div><div class="flex gap-1"><button data-user="${u}" class="set-cash p-1 bg-slate-100 rounded text-sm">Set tiền</button><button data-user="${u}" class="del-user p-1 bg-red-100 rounded text-sm">Xóa</button></div>`; el.adminPlayers.appendChild(div); }
    el.adminPlayers.querySelectorAll('.del-user').forEach(btn=>btn.onclick=e=>{ const u=e.target.dataset.user; if(confirm('Xóa '+u+'?')){ delete state.users[u]; saveState(state); renderAdminPlayers(); } });
    el.adminPlayers.querySelectorAll('.set-cash').forEach(btn=>btn.onclick=e=>{ const u=e.target.dataset.user; const v=prompt('Nhập tiền mới cho '+u, String(state.users[u].cash)); if(v!==null){ state.users[u].cash=Number(v)||0; saveState(state); renderAdminPlayers(); } }); }

  // UI render
  function renderOrderBook(code){ ensureOrderbook(code); const book = state.orders[code] || { bids:[], asks:[] }; el.orderBook.innerHTML=''; const headerB = document.createElement('div'); headerB.className='text-xs text-slate-500'; headerB.textContent='Bids (buy)'; el.orderBook.appendChild(headerB); book.bids.slice(0,10).forEach(b=>{ const d=document.createElement('div'); d.className='text-sm'; d.textContent = `@${fmt(b.price)} x ${b.remaining} — ${b.user}`; el.orderBook.appendChild(d); }); const headerA = document.createElement('div'); headerA.className='text-xs text-slate-500 mt-2'; headerA.textContent='Asks (sell)'; el.orderBook.appendChild(headerA); book.asks.slice(0,10).forEach(a=>{ const d=document.createElement('div'); d.className='text-sm'; d.textContent = `@${fmt(a.price)} x ${a.remaining} — ${a.user}`; el.orderBook.appendChild(d); }); }

  function renderMyOrders(){ el.myOrders.innerHTML=''; if(!currentUser) return; for(const [code,book] of Object.entries(state.orders||{})){ book.bids.concat(book.asks).filter(o=>o.user===currentUser).forEach(o=>{ const d=document.createElement('div'); d.className='p-1 border-b text-sm'; d.innerHTML = `${o.side.toUpperCase()} ${code} @${fmt(o.price||0)} x ${o.remaining} <button data-id="${o.id}" class="ml-2 cancel-order text-xs bg-rose-100 rounded px-1">Hủy</button>`; el.myOrders.appendChild(d); }); } document.querySelectorAll('.cancel-order').forEach(b=>b.onclick=e=>{ const id = e.target.dataset.id; for(const code of Object.keys(state.orders||{})){ ['bids','asks'].forEach(side=>{ state.orders[code][side] = state.orders[code][side].filter(o=>o.id!==id); }); } saveState(state); renderMyOrders(); renderOrderBook(el.tradeTicker.value); }); }

  function renderTrades(){ el.tradeHistory.innerHTML=''; for(const t of (state.lastTrades||[]).slice(0,50)){ const d=document.createElement('div'); d.className='p-1 border-b text-sm'; d.textContent = `${t.time} ${t.buyUser} bought ${t.qty} ${t.code} from ${t.sellUser} @ ${fmt(t.price)}`; el.tradeHistory.appendChild(d); } }

  function renderPortfolio(){ el.portfolioList.innerHTML=''; if(!currentUser) return; const u = state.users[currentUser]; el.uiUsername.textContent = currentUser; el.uiCash.textContent = fmt(u.cash); el.profileAvatar.src = u.avatar || ''; for(const [code,qty] of Object.entries(u.positions||{})){ const p = engine.series[code] ? engine.series[code].price : state.tickers[code].price; const div = document.createElement('div'); div.className='p-2 border rounded'; div.innerHTML = `<div class="flex items-center justify-between"><div>${code} x ${qty}</div><div>${fmt((p*qty).toFixed(2))} ₫</div></div>`; el.portfolioList.appendChild(div); } }

  function renderUI(){ renderTickers(); renderPortfolio(); renderOrderBook(el.tradeTicker.value || Object.keys(state.tickers)[0]); renderMyOrders(); renderTrades(); for(const code of Object.keys(state.tickers)){ const span = document.querySelector('.price-'+code); if(span) span.textContent = fmt((engine.series[code].price).toFixed(2)); } }

  // Events
  el.btnLogin.onclick = ()=>{ const u=el.loginUsername.value.trim(); const p=el.loginPin.value.trim(); if(!u||!p) return alert('Nhập tên và pin'); ensureUserExists(u); loginUser(u,p); };
  el.btnRegister.onclick = ()=>{ const u=el.loginUsername.value.trim(); const p=el.loginPin.value.trim(); if(!u||!p) return alert('Nhập tên và pin'); ensureUserExists(u); loginUser(u,p); };
  el.marketBuy.onclick = placeBuyMarket; el.marketSell.onclick = placeSellMarket; el.limitBuy.onclick = placeBuyLimit; el.limitSell.onclick = placeSellLimit; el.stopBuy.onclick = placeBuyStop; el.stopSell.onclick = placeSellStop;
  el.adminLogin.onclick = ()=>adminLogin(el.adminPin.value.trim()); el.addTicker.onclick = ()=>{ addTicker(el.newTickerCode.value, el.newTickerName.value, Number(el.newTickerStart.value||1)); el.newTickerCode.value=''; el.newTickerName.value=''; el.newTickerStart.value=''; };
  el.resetData.onclick = resetData; el.btnLogout.onclick = logout;

  document.addEventListener('click', e=>{ if(e.target.matches('.open-chart')){ const code = e.target.dataset.code; rebuildChartFor(code); } if(e.target.matches('.watch')){ const code = e.target.dataset.code; el.tradeTicker.value = code; rebuildChartFor(code); renderOrderBook(code); } });

  el.avatarInput.onchange = e=>{ const f = e.target.files[0]; if(!f) return; const r = new FileReader(); r.onload = ()=>{ if(!currentUser) return alert('Đăng nhập trước'); state.users[currentUser].avatar = r.result; saveState(state); renderPortfolio(); }; r.readAsDataURL(f); };

  // Main loop
  function tick(){ engine.step(); evaluateStopOrders(); // after price change, check stop orders
    // update UI
    renderUI(); // update chart data
    const s = engine.series[currentChartTicker]; if(s && s.candles && s.candles.length){ candleSeries.setData(s.candles.map(c=>({ time:c.time, open:c.open, high:c.high, low:c.low, close:c.close }))); }
  }
  setInterval(tick, 1000);

  // Init
  if(!currentUser) el.loginModal.style.display='flex'; else el.loginModal.style.display='none'; renderTickers(); rebuildChartFor(currentChartTicker); renderUI();

  // top controls: export/import
  const exp = document.createElement('button'); exp.className='p-2 bg-slate-100 rounded text-sm'; exp.textContent='Export State'; exp.onclick = ()=>{ const a=document.createElement('a'); a.href='data:application/json,'+encodeURIComponent(localStorage.getItem('sg_state')); a.download='sg_state.json'; a.click(); };
  const imp = document.createElement('button'); imp.className='p-2 bg-slate-100 rounded text-sm'; imp.textContent='Import State'; imp.onclick = ()=>{ const file=document.createElement('input'); file.type='file'; file.accept='.json'; file.onchange = e=>{ const f=e.target.files[0]; const reader=new FileReader(); reader.onload=()=>{ localStorage.setItem('sg_state', reader.result); location.reload(); }; reader.readAsText(f); }; file.click(); };
  document.getElementById('top-controls').appendChild(exp); document.getElementById('top-controls').appendChild(imp);

  </script>
</body>
</html>
