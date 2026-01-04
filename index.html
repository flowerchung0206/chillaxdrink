<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chillax Drink 蕎淶清飲 訂貨管理系統</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Noto Sans TC', sans-serif; -webkit-tap-highlight-color: transparent; }
        
        .glass {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
        }

        @keyframes pulse-red {
            0%, 100% { box-shadow: 0 0 0 0 rgba(239, 68, 68, 0.5); }
            50% { box-shadow: 0 0 0 12px rgba(239, 68, 68, 0); }
        }
        .warning-breathe {
            animation: pulse-red 2s infinite;
        }

        .btn-shadow {
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .tab-active {
            @apply bg-white shadow-sm text-emerald-900 font-bold;
        }

        input::-webkit-outer-spin-button,
        input::-webkit-inner-spin-button {
            -webkit-appearance: none;
            margin: 0;
        }

        .stepper-btn {
            @apply w-10 h-10 flex items-center justify-center rounded-full bg-gray-100 text-gray-600 transition-all active:scale-90 hover:bg-emerald-100 hover:text-emerald-700;
        }

        #toast {
            visibility: hidden;
            min-width: 250px;
            margin-left: -125px;
            background-color: #1f2937;
            color: #fff;
            text-align: center;
            border-radius: 16px;
            padding: 16px;
            position: fixed;
            z-index: 1000;
            left: 50%;
            bottom: 40px;
            font-size: 14px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        #toast.show {
            visibility: visible;
            -webkit-animation: fadein 0.5s, fadeout 0.5s 2.5s;
            animation: fadein 0.5s, fadeout 0.5s 2.5s;
        }

        @keyframes fadein { from {bottom: 0; opacity: 0;} to {bottom: 40px; opacity: 1;} }
        @keyframes fadeout { from {bottom: 40px; opacity: 1;} to {bottom: 0; opacity: 0;} }
    </style>
</head>
<body class="bg-[#F3F4F6] min-h-screen pb-24 text-gray-800">

    <div id="toast">已複製訂單並準備開啟 LINE</div>

    <!-- Header -->
    <header class="bg-gradient-to-br from-[#064e3b] to-[#065f46] text-white pt-10 pb-14 px-6 rounded-b-[48px] shadow-2xl relative overflow-hidden">
        <div class="absolute top-0 right-0 -mr-10 -mt-10 w-40 h-40 bg-white/5 rounded-full blur-2xl"></div>
        <div class="max-w-2xl mx-auto flex justify-between items-center relative z-10">
            <div>
                <h1 class="text-2xl font-bold tracking-tight">Chillax Drink 蕎淶清飲</h1>
                <p class="text-emerald-200 text-lg font-medium opacity-90 mt-1">鮮奶茶•醇好茶</p>
            </div>
            <div class="w-12 h-12 bg-white/20 rounded-2xl backdrop-blur-md flex items-center justify-center border border-white/30">
                <svg class="h-7 w-7 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                </svg>
            </div>
        </div>
    </header>

    <!-- Store Information Card -->
    <div class="max-w-2xl mx-auto -mt-10 px-4 relative z-20">
        <div class="glass p-6 rounded-[32px] shadow-xl border border-white/50 space-y-3">
            <div class="flex items-center gap-3 text-sm">
                <div class="w-9 h-9 bg-emerald-100 rounded-2xl flex items-center justify-center text-emerald-700 shadow-inner">
                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"></path></svg>
                </div>
                <a href="tel:0910901956" class="font-bold text-gray-700 hover:text-emerald-700 transition-colors">0910901956</a>
                <span class="text-gray-300 mx-1">|</span>
                <span class="text-gray-600 truncate">桃園市桃園區文中二路25巷22號</span>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="max-w-2xl mx-auto mt-8 px-4">
        <div class="flex p-1.5 bg-gray-200/60 rounded-2xl backdrop-blur-md">
            <button onclick="switchTab('tea')" id="tab-tea" class="flex-1 py-3 text-sm font-medium rounded-xl transition-all tab-active">大武茶葉</button>
            <button onclick="switchTab('zheng')" id="tab-zheng" class="flex-1 py-3 text-sm font-medium rounded-xl transition-all text-gray-500">鉦旺樂</button>
            <button onclick="switchTab('lemon')" id="tab-lemon" class="flex-1 py-3 text-sm font-medium rounded-xl transition-all text-gray-500">檸檬工廠</button>
            <button onclick="switchTab('stats')" id="tab-stats" class="flex-1 py-3 text-sm font-medium rounded-xl transition-all text-gray-500">叫貨分析</button>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="p-4 max-w-2xl mx-auto space-y-6">

        <!-- 1. 大武茶葉 Section -->
        <section id="sect-tea" class="tab-content">
            <div class="flex justify-between items-center mb-5 px-2">
                <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2">
                    <span class="w-2 h-6 bg-emerald-600 rounded-full"></span>
                    大武茶葉訂貨
                </h2>
                <div class="flex flex-col items-end">
                    <span class="text-[10px] text-gray-400 font-bold uppercase tracking-wider">Payment Method</span>
                    <span class="text-xs font-bold text-emerald-700">匯款</span>
                </div>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4" id="tea-list">
                <!-- Items Rendered by JS -->
            </div>

            <!-- Receipt Summary -->
            <div class="mt-8 bg-white rounded-[32px] p-8 shadow-2xl border border-gray-100 relative overflow-hidden">
                <div class="absolute top-0 right-0 w-32 h-32 bg-emerald-50 rounded-bl-full opacity-50 -z-0"></div>
                <h3 class="font-bold text-gray-800 mb-6 flex items-center gap-2 relative z-10 text-lg">
                    <svg class="w-6 h-6 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
                    訂單結算清單
                </h3>
                <div class="space-y-4 relative z-10">
                    <div class="flex justify-between text-sm">
                        <span class="text-gray-500">本次訂購量</span>
                        <span class="font-bold text-gray-800"><span id="tea-total-qty">0</span> 斤</span>
                    </div>
                    <div class="flex justify-between text-sm">
                        <span class="text-gray-500">商品小計</span>
                        <span class="font-medium text-gray-700" id="tea-subtotal">NT$ 0</span>
                    </div>
                    <div class="flex justify-between text-sm text-red-500 font-medium">
                        <span>滿 60 斤減價優惠</span>
                        <span id="tea-discount">- NT$ 0</span>
                    </div>
                    <div class="flex justify-between text-sm text-gray-700">
                        <span>發票稅額 (5%)</span>
                        <span id="tea-tax">NT$ 0</span>
                    </div>
                    <div class="flex justify-between text-sm text-gray-500">
                        <span>物流運費 (30斤免運)</span>
                        <span id="tea-shipping">NT$ 150</span>
                    </div>
                    <div class="border-t border-dashed border-gray-200 my-6 pt-6 flex justify-between items-center">
                        <span class="text-lg font-bold text-gray-800">應付總金額</span>
                        <span class="text-3xl font-black text-emerald-700" id="tea-final-total">NT$ 0</span>
                    </div>
                </div>
                <button onclick="sendLine('tea')" class="w-full mt-6 bg-[#06C755] hover:bg-[#05b54d] text-white py-4.5 rounded-2xl font-bold flex items-center justify-center gap-3 btn-shadow transition-all active:scale-[0.97] text-lg">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/4/41/LINE_logo.svg" class="w-7 h-7" alt="LINE">
                    傳送 LINE 給廠商
                </button>
            </div>
        </section>

        <!-- 2. 鉦旺樂 Section -->
        <section id="sect-zheng" class="tab-content hidden">
            <div class="flex justify-between items-center mb-5 px-2">
                <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2">
                    <span class="w-2 h-6 bg-orange-500 rounded-full"></span>
                    鉦旺樂訂貨
                </h2>
                <span class="text-xs font-bold text-orange-700 bg-orange-50 px-3 py-1 rounded-lg">付款：貨到付款</span>
            </div>

            <div class="bg-white p-6 rounded-[32px] shadow-lg border border-gray-100 flex items-center justify-between">
                <div>
                    <div class="text-[10px] font-bold text-orange-400 uppercase tracking-widest mb-1">Mango Juice</div>
                    <div class="text-xl font-bold text-gray-800">芒果漿</div>
                    <div class="text-sm text-gray-400 font-medium mt-0.5">NT$ 170 / 瓶</div>
                </div>
                <div class="flex items-center gap-4 bg-gray-50 p-2 rounded-2xl">
                    <button onclick="step('zheng-mango-qty', -1, calcZheng)" class="stepper-btn shadow-sm bg-white">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="2" d="M20 12H4"></path></svg>
                    </button>
                    <input type="number" id="zheng-mango-qty" oninput="calcZheng()" class="w-12 text-center font-bold text-xl bg-transparent" value="0" min="0">
                    <button onclick="step('zheng-mango-qty', 1, calcZheng)" class="stepper-btn shadow-sm bg-white text-orange-600">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="2" d="M12 4v16m8-8H4"></path></svg>
                    </button>
                </div>
            </div>

            <div class="mt-8 bg-white p-8 rounded-[32px] shadow-xl border border-gray-100">
                <div class="space-y-4">
                    <div class="flex justify-between text-sm text-gray-500">
                        <span>訂購總瓶數</span>
                        <span class="font-bold text-gray-800"><span id="zheng-total-qty">0</span> 瓶</span>
                    </div>
                    <div class="flex justify-between text-sm text-gray-500">
                        <span>階梯式運費</span>
                        <span class="font-medium" id="zheng-shipping">NT$ 0</span>
                    </div>
                    <div class="border-t pt-6 flex justify-between items-center">
                        <span class="font-bold text-lg text-gray-800">總計金額</span>
                        <span class="text-3xl font-black text-orange-600" id="zheng-final-total">NT$ 0</span>
                    </div>
                </div>
                <button onclick="sendLine('zheng')" class="w-full mt-8 bg-[#06C755] text-white py-4.5 rounded-2xl font-bold flex items-center justify-center gap-3 btn-shadow active:scale-95 transition-all text-lg">
                    傳送 LINE 給廠商
                </button>
            </div>
        </section>

        <!-- 3. 檸檬工廠 Section -->
        <section id="sect-lemon" class="tab-content hidden">
            <div class="flex justify-between items-center mb-5 px-2">
                <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2">
                    <span class="w-2 h-6 bg-yellow-500 rounded-full"></span>
                    檸檬工廠訂貨
                </h2>
                <span class="text-xs font-bold text-yellow-700 bg-yellow-50 px-3 py-1 rounded-lg">付款：貨到付款</span>
            </div>

            <!-- Warning Box -->
            <div id="lemon-warning" class="hidden mb-6 p-5 bg-red-50 text-red-600 rounded-[24px] text-sm font-bold border border-red-100 warning-breathe">
                <div class="flex items-center gap-3 justify-center">
                    <div class="bg-red-500 text-white rounded-full p-1">
                        <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7 4a1 1 0 11-2 0 1 1 0 012 0zm-1-9a1 1 0 00-1 1v4a1 1 0 102 0V6a1 1 0 00-1-1z" clip-rule="evenodd"></path></svg>
                    </div>
                    不滿 24 瓶 (一箱) 無法送出訂單
                </div>
            </div>

            <div class="space-y-4" id="lemon-list">
                <!-- JS Render -->
            </div>

            <div class="mt-8 bg-white p-8 rounded-[32px] shadow-xl border border-gray-100">
                <div class="space-y-4 text-sm">
                    <div class="flex justify-between">
                        <span class="text-gray-500">總瓶數</span>
                        <span class="font-bold text-gray-800 text-base"><span id="lemon-total-qty">0</span> 瓶</span>
                    </div>
                    <div class="flex justify-between text-gray-500">
                        <span>物流運費 ($100/箱)</span>
                        <span id="lemon-shipping">NT$ 0</span>
                    </div>
                    <div class="flex justify-between text-gray-500">
                        <span>貨到付款代收費</span>
                        <span id="lemon-fee">NT$ 0</span>
                    </div>
                    <div class="border-t pt-6 flex justify-between items-center">
                        <span class="font-bold text-lg text-gray-800">結帳金額</span>
                        <span class="text-3xl font-black text-yellow-600" id="lemon-final-total">NT$ 0</span>
                    </div>
                </div>
                <button id="btn-lemon-line" onclick="sendLine('lemon')" class="w-full mt-8 bg-gray-300 text-white py-4.5 rounded-2xl font-bold flex items-center justify-center gap-3 cursor-not-allowed transition-all text-lg" disabled>
                    傳送 LINE 給廠商
                </button>
            </div>
        </section>

        <!-- 4. Analysis Section -->
        <section id="sect-stats" class="tab-content hidden">
            <div class="bg-white p-8 rounded-[40px] shadow-2xl border border-gray-100">
                <h3 class="text-xl font-bold mb-8 text-gray-800 flex items-center gap-2">
                    <svg class="w-6 h-6 text-emerald-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
                    本期訂單比例分析
                </h3>
                <div class="h-64 mb-10">
                    <canvas id="ordersChart"></canvas>
                </div>
                
                <div id="hot-tip" class="p-6 bg-emerald-50 rounded-[28px] border border-emerald-100 hidden">
                    <div class="flex items-center gap-4 text-emerald-800 font-bold mb-4">
                        <div class="w-12 h-12 bg-white rounded-2xl flex items-center justify-center shadow-sm text-2xl">📈</div>
                        <span class="text-lg">下次叫貨提示</span>
                    </div>
                    <p class="text-emerald-700 leading-relaxed text-sm font-medium" id="tip-text"></p>
                </div>
            </div>
        </section>

    </main>

    <script>
        // Data Definitions
        const TEA_ITEMS = [
            { id: 'sj', name: '四季春茶', price: 245 },
            { id: 'rh', name: '盧哈娜紅茶', price: 160 },
            { id: 'ls', name: '蘭香綠茶', price: 160 },
            { id: 'jx', name: '金萱青茶', price: 250 },
            { id: 'hjx', name: '重金萱', price: 250 },
            { id: 'old', name: '古早味紅茶', price: 100 }
        ];

        const LEMON_ITEMS = [
            { id: 'w_sug', name: '白甘蔗汁', price: 60 },
            { id: 'lem', name: '檸檬汁', price: 130 },
            { id: 'ora', name: '柳丁汁', price: 80 },
            { id: 'pas', name: '百香果汁', price: 130 }
        ];

        const storeInfo = {
            name: "Chillax Drink 蕎淶清飲",
            tagline: "鮮奶茶•醇好茶",
            phone: "0910901956",
            address: "桃園市桃園區文中二路25巷22號"
        };

        let chart = null;

        // Counter logic
        function step(id, val, callback) {
            const el = document.getElementById(id);
            let current = parseInt(el.value) || 0;
            el.value = Math.max(0, current + val);
            callback();
        }

        // Initialize UI
        function init() {
            // Render Tea Items
            const teaContainer = document.getElementById('tea-list');
            TEA_ITEMS.forEach(item => {
                teaContainer.innerHTML += `
                    <div class="bg-white p-5 rounded-[28px] shadow-sm border border-gray-50 flex justify-between items-center transition-all hover:shadow-md">
                        <div>
                            <div class="font-bold text-gray-800 mb-0.5">${item.name}</div>
                            <div class="text-[11px] text-emerald-600 font-bold tracking-wide">NT$ ${item.price} / 斤</div>
                        </div>
                        <div class="flex items-center gap-3 bg-gray-50 p-1.5 rounded-2xl">
                            <button onclick="step('tea-${item.id}', -1, calcTea)" class="stepper-btn bg-white shadow-sm">
                                <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="3" d="M20 12H4"></path></svg>
                            </button>
                            <input type="number" id="tea-${item.id}" oninput="calcTea()" class="w-8 text-center font-black text-gray-700 bg-transparent" value="0">
                            <button onclick="step('tea-${item.id}', 1, calcTea)" class="stepper-btn bg-white shadow-sm text-emerald-600">
                                <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="3" d="M12 4v16m8-8H4"></path></svg>
                            </button>
                        </div>
                    </div>
                `;
            });

            // Render Lemon Factory Items
            const lemonContainer = document.getElementById('lemon-list');
            LEMON_ITEMS.forEach(item => {
                lemonContainer.innerHTML += `
                    <div class="bg-white p-5 rounded-[28px] shadow-sm border border-gray-50 flex justify-between items-center">
                        <div>
                            <div class="font-bold text-gray-800 mb-0.5">${item.name}</div>
                            <div class="text-[11px] text-yellow-600 font-bold tracking-wide">NT$ ${item.price} / 瓶</div>
                        </div>
                        <div class="flex items-center gap-3 bg-gray-50 p-1.5 rounded-2xl">
                            <button onclick="step('lemon-${item.id}', -1, calcLemon)" class="stepper-btn bg-white shadow-sm">
                                <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="3" d="M20 12H4"></path></svg>
                            </button>
                            <input type="number" id="lemon-${item.id}" oninput="calcLemon()" class="w-8 text-center font-black text-gray-700 bg-transparent" value="0">
                            <button onclick="step('lemon-${item.id}', 1, calcLemon)" class="stepper-btn bg-white shadow-sm text-yellow-600">
                                <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-width="3" d="M12 4v16m8-8H4"></path></svg>
                            </button>
                        </div>
                    </div>
                `;
            });
            updateChart();
        }

        // Calculations - Tea
        function calcTea() {
            let totalQty = 0, subtotal = 0;
            TEA_ITEMS.forEach(item => {
                const qty = parseInt(document.getElementById(`tea-${item.id}`).value) || 0;
                totalQty += qty;
                subtotal += qty * item.price;
            });
            let discount = totalQty >= 60 ? totalQty * 10 : 0;
            const tax = Math.round((subtotal - discount) * 0.05);
            const shipping = (totalQty < 30 && totalQty > 0) ? 150 : 0;
            const final = subtotal - discount + tax + shipping;

            document.getElementById('tea-total-qty').innerText = totalQty;
            document.getElementById('tea-subtotal').innerText = `NT$ ${subtotal.toLocaleString()}`;
            document.getElementById('tea-discount').innerText = `- NT$ ${discount.toLocaleString()}`;
            document.getElementById('tea-tax').innerText = `NT$ ${tax.toLocaleString()}`;
            document.getElementById('tea-shipping').innerText = `NT$ ${shipping.toLocaleString()}`;
            document.getElementById('tea-final-total').innerText = `NT$ ${final.toLocaleString()}`;
            updateChart();
        }

        // Calculations - Zheng
        function calcZheng() {
            const qty = parseInt(document.getElementById('zheng-mango-qty').value) || 0;
            const subtotal = qty * 170;
            let shipping = 0;
            if (qty > 0 && qty < 10) shipping = 200;
            else if (qty >= 10 && qty < 20) shipping = 150;
            
            document.getElementById('zheng-total-qty').innerText = qty;
            document.getElementById('zheng-shipping').innerText = `NT$ ${shipping.toLocaleString()}`;
            document.getElementById('zheng-final-total').innerText = `NT$ ${(subtotal + shipping).toLocaleString()}`;
            updateChart();
        }

        // Calculations - Lemon
        function calcLemon() {
            let totalQty = 0, subtotal = 0;
            LEMON_ITEMS.forEach(item => {
                const qty = parseInt(document.getElementById(`lemon-${item.id}`).value) || 0;
                totalQty += qty;
                subtotal += qty * item.price;
            });

            const warning = document.getElementById('lemon-warning');
            const btn = document.getElementById('btn-lemon-line');
            
            if (totalQty > 0 && totalQty < 24) {
                warning.classList.remove('hidden');
                btn.classList.replace('bg-[#06C755]', 'bg-gray-300');
                btn.disabled = true;
            } else if (totalQty >= 24) {
                warning.classList.add('hidden');
                btn.classList.replace('bg-gray-300', 'bg-[#06C755]');
                btn.disabled = false;
            } else {
                warning.classList.add('hidden');
                btn.disabled = true;
            }

            const boxes = Math.ceil(totalQty / 24);
            const shipping = totalQty >= 24 ? boxes * 100 : 0;
            const fee = totalQty >= 24 ? 30 : 0;

            document.getElementById('lemon-total-qty').innerText = totalQty;
            document.getElementById('lemon-shipping').innerText = `NT$ ${shipping.toLocaleString()}`;
            document.getElementById('lemon-fee').innerText = `NT$ ${fee.toLocaleString()}`;
            document.getElementById('lemon-final-total').innerText = `NT$ ${(subtotal + shipping + fee).toLocaleString()}`;
            updateChart();
        }

        // UI Tabs
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(c => c.classList.add('hidden'));
            document.querySelectorAll('nav button').forEach(b => b.classList.remove('tab-active', 'bg-white', 'shadow-sm', 'text-emerald-900', 'font-bold'));
            document.querySelectorAll('nav button').forEach(b => b.classList.add('text-gray-500'));
            
            document.getElementById(`sect-${tabId}`).classList.remove('hidden');
            const activeBtn = document.getElementById(`tab-${tabId}`);
            activeBtn.classList.add('tab-active');
            activeBtn.classList.remove('text-gray-500');
            
            if (tabId === 'stats') setTimeout(updateChart, 150);
        }

        function showToast(msg) {
            const t = document.getElementById("toast");
            t.innerText = msg;
            t.className = "show";
            setTimeout(() => { t.className = t.className.replace("show", ""); }, 3000);
        }

        // Copy and Send
        function sendLine(vendor) {
            let message = `【訂單：${storeInfo.name}】\n`;
            message += `店舖資訊：${storeInfo.tagline}\n`;
            message += `訂貨日期：${new Date().toLocaleDateString()}\n`;
            message += `聯絡電話：${storeInfo.phone}\n`;
            message += `送貨地址：${storeInfo.address}\n`;
            message += `--------------------------\n`;

            if (vendor === 'tea') {
                TEA_ITEMS.forEach(item => {
                    const qty = document.getElementById(`tea-${item.id}`).value;
                    if (qty > 0) message += `● ${item.name}：${qty} 斤\n`;
                });
                message += `--------------------------\n`;
                message += `合計數量：${document.getElementById('tea-total-qty').innerText} 斤\n`;
                message += `總計金額：${document.getElementById('tea-final-total').innerText}\n`;
                message += `付款方式：匯款\n`;
            } else if (vendor === 'zheng') {
                const qty = document.getElementById('zheng-mango-qty').value;
                message += `● 芒果漿：${qty} 瓶\n`;
                message += `--------------------------\n`;
                message += `總計金額：${document.getElementById('zheng-final-total').innerText}\n`;
                message += `付款方式：貨到付款\n`;
            } else if (vendor === 'lemon') {
                LEMON_ITEMS.forEach(item => {
                    const qty = document.getElementById(`lemon-${item.id}`).value;
                    if (qty > 0) message += `● ${item.name}：${qty} 瓶\n`;
                });
                message += `--------------------------\n`;
                message += `合計數量：${document.getElementById('lemon-total-qty').innerText} 瓶\n`;
                message += `總計金額：${document.getElementById('lemon-final-total').innerText}\n`;
                message += `付款方式：貨到付款\n`;
            }

            // Clipboard Fallback
            const textArea = document.createElement("textarea");
            textArea.value = message;
            document.body.appendChild(textArea);
            textArea.select();
            try {
                document.execCommand('copy');
                showToast("訂單已複製到剪貼簿，正在開啟 LINE...");
            } catch (err) {
                console.error('無法複製');
            }
            document.body.removeChild(textArea);

            // Open LINE
            setTimeout(() => {
                const lineUrl = `https://line.me/R/msg/text/?${encodeURIComponent(message)}`;
                const a = document.createElement('a');
                a.href = lineUrl;
                a.target = '_blank';
                a.click();
            }, 500);
        }

        // Analytics Chart
        function updateChart() {
            const labels = [], data = [];
            let hottest = { name: '', qty: 0 };

            const checkList = (list, prefix) => {
                list.forEach(item => {
                    const qty = parseInt(document.getElementById(`${prefix}-${item.id}`)?.value) || 0;
                    if (qty > 0) {
                        labels.push(item.name);
                        data.push(qty);
                        if (qty > hottest.qty) hottest = { name: item.name, qty };
                    }
                });
            };

            checkList(TEA_ITEMS, 'tea');
            const zq = parseInt(document.getElementById('zheng-mango-qty').value) || 0;
            if (zq > 0) { labels.push('芒果漿'); data.push(zq); if (zq > hottest.qty) hottest = { name: '芒果漿', qty: zq }; }
            checkList(LEMON_ITEMS, 'lemon');

            const ctx = document.getElementById('ordersChart').getContext('2d');
            if (chart) chart.destroy();
            
            if (labels.length === 0) {
                // Empty state for chart
                ctx.font = '14px Noto Sans TC';
                ctx.textAlign = 'center';
                ctx.fillText('尚無訂購品項', ctx.canvas.width/2, ctx.canvas.height/2);
                return;
            }

            chart = new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: labels,
                    datasets: [{
                        data: data,
                        backgroundColor: ['#059669', '#10b981', '#34d399', '#f59e0b', '#fbbf24', '#fb7185', '#818cf8', '#a78bfa'],
                        borderWidth: 0,
                        hoverOffset: 15
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: { 
                        legend: { position: 'bottom', labels: { padding: 20, usePointStyle: true, font: { size: 12 } } } 
                    },
                    cutout: '75%',
                    animation: { animateScale: true }
                }
            });

            const tipBox = document.getElementById('hot-tip');
            if (hottest.qty > 0) {
                tipBox.classList.remove('hidden');
                document.getElementById('tip-text').innerText = `本次熱銷品項為【${hottest.name}】，訂購數量達到 ${hottest.qty} 單位。這表示近期該品項銷售速度較快，若為核心茶底，建議下次叫貨可多預備約 10% 的量，避免突發客流量導致缺貨。`;
            } else {
                tipBox.classList.add('hidden');
            }
        }

        window.onload = init;
    </script>
</body>
</html>
