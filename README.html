<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dakhla Camp Kite School - Invoice Generator</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- html2pdf -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap');
        
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #e5e7eb;
        }

        /* A4 Paper Dimensions & Layout */
        #invoice-element {
            background: white;
            width: 210mm;
            min-height: 297mm;
            margin: 0 auto;
            padding: 15mm;
            position: relative; 
            box-sizing: border-box; 
            color: #000;
            display: block; 
        }

        /* Table Styling */
        .camp-table {
            width: 100%;
            border-collapse: collapse;
            border: 2px solid #000;
            margin-bottom: 20px;
        }

        .camp-table th {
            background-color: #000;
            color: #fff;
            padding: 8px 5px;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 12px;
            border: 1px solid #fff;
        }

        .camp-table td {
            border: 1px solid #000;
            padding: 6px 5px;
            text-align: center;
            font-size: 12px;
            height: 30px; 
        }

        /* Input Styles */
        .input-field {
            background-color: #f9fafb;
            border: 1px solid #d1d5db;
            color: #111827;
            border-radius: 0.375rem;
            padding: 0.5rem;
            width: 100%;
            font-size: 0.875rem;
        }

        .custom-file-upload {
            border: 1px dashed #ccc;
            display: inline-block;
            padding: 6px 12px;
            cursor: pointer;
            width: 100%;
            text-align: center;
            border-radius: 4px;
            background: #f8f9fa;
            font-size: 0.875rem;
        }

        /* Specific Totals Layout */
        .totals-container {
            display: flex;
            justify-content: flex-end;
            margin-top: 10px;
            page-break-inside: avoid;
        }

        .totals-right-col {
            width: 60%; 
        }

        .summary-boxes {
            display: flex;
            gap: 10px;
            margin-bottom: 5px;
        }

        .summary-box {
            border: 1px solid #000;
            padding: 10px;
            width: 50%;
            background: white;
        }

        .summary-title {
            font-weight: 700;
            text-transform: uppercase;
            font-size: 11px;
            border-bottom: 1px solid #000;
            padding-bottom: 2px;
            margin-bottom: 5px;
        }

        .summary-row {
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            margin-bottom: 2px;
        }

        .summary-price {
            font-weight: 900;
            font-size: 14px;
            text-align: right;
        }

        .bar-euro {
            background-color: #000;
            color: #fff;
            padding: 8px 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 900;
            text-transform: uppercase;
            margin-bottom: 2px;
        }

        .bar-mad {
            background-color: #f3f4f6; /* Light grey */
            color: #000;
            border: 1px solid #d1d5db; /* Slight border for visibility on white */
            padding: 8px 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 900;
            text-transform: uppercase;
            position: relative;
        }

        /* Footer positioning */
        .footer-area {
            margin-top: 50px; 
            padding-top: 10px;
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            page-break-inside: avoid; /* Keep signatures together */
        }

        .signature-line {
            width: 100%;
            border-bottom: 2px solid #000;
            margin-top: 40px;
        }

        .editable-hours {
            width: 100%;
            text-align: center;
            font-weight: bold;
            background: transparent;
            border: 1px solid transparent;
            border-radius: 4px;
        }
        .editable-hours:hover { border-color: #cbd5e1; }
        .editable-hours:focus { background: #fff; border-color: #3b82f6; outline: none; }

        /* Auto-expanding notes area */
        .invoice-note-box {
            font-family: 'Roboto', sans-serif;
            line-height: 1.5;
            min-height: 40px;
            height: auto;
            width: 100%;
            border: 1px solid #9ca3af; /* gray-400 */
            border-radius: 4px;
            padding: 8px;
            font-size: 0.875rem; /* text-sm */
            background: transparent;
            outline: none;
            overflow: hidden; /* Hide scrollbars */
        }
        .invoice-note-box:focus {
            background: white;
            border-color: #000;
        }
        /* Placeholder support for contenteditable */
        .invoice-note-box[contenteditable]:empty:before {
            content: attr(placeholder);
            color: #9ca3af;
            display: block; /* For Firefox */
        }
        
        tr { page-break-inside: avoid; }
        .hidden { display: none !important; }
    </style>
</head>
<body class="p-4 bg-gray-200">

    <div class="max-w-[1400px] mx-auto flex flex-col lg:flex-row gap-6">
        
        <!-- CONTROL PANEL -->
        <div class="w-full lg:w-[350px] bg-white p-6 rounded-lg shadow-xl h-fit shrink-0">
            <h2 class="text-lg font-bold mb-4 text-gray-800 border-b pb-2">Settings</h2>

            <!-- Invoice Type Switcher -->
            <div class="mb-4 bg-blue-50 p-2 rounded border border-blue-200">
                <label class="block text-xs font-bold text-blue-800 mb-1 uppercase">Select Invoice Type</label>
                <select id="invoiceMode" onchange="toggleMode()" class="w-full p-2 border border-blue-300 rounded text-sm font-bold">
                    <option value="lessons">Kite/Wing Lessons</option>
                    <option value="facility">Facility Service</option>
                </select>
            </div>

            <!-- Logo Upload -->
            <div class="mb-4">
                <label class="block text-xs font-bold text-gray-700 mb-1">School Logo</label>
                <label for="logo-upload" class="custom-file-upload hover:bg-gray-100">
                    <i class="fa fa-cloud-upload"></i> Upload Logo
                </label>
                <input id="logo-upload" type="file" accept="image/*" onchange="loadLogo(event)"/>
            </div>

            <!-- Client Info -->
            <div class="space-y-3 mb-4">
                <div>
                    <label class="block text-xs font-bold text-gray-500 uppercase">Client Name</label>
                    <input type="text" id="clientName" placeholder="Client Name" class="input-field">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-500 uppercase">Date</label>
                    <input type="date" id="invoiceDate" class="input-field">
                </div>
            </div>

            <!-- Add Session / Service -->
            <div class="bg-gray-50 p-4 rounded border border-gray-200 mb-4">
                <h3 id="addHeader" class="font-bold text-gray-800 text-xs mb-3 uppercase">Add Session</h3>
                
                <div class="grid grid-cols-2 gap-2 mb-2">
                    <div>
                        <label class="block text-[10px] font-bold text-gray-500">DATE</label>
                        <input type="date" id="sessionDate" class="w-full p-1 border rounded text-xs">
                    </div>
                    
                    <!-- Hours Input (Lessons Mode) -->
                    <div id="hoursInputGroup">
                        <label class="block text-[10px] font-bold text-gray-500">HOURS</label>
                        <input type="number" id="sessionHours" step="0.5" placeholder="2" class="w-full p-1 border rounded text-xs">
                    </div>

                    <!-- Pax Input (Facility Mode) -->
                    <div id="paxInputGroup" class="hidden">
                        <label class="block text-[10px] font-bold text-gray-500">PAX (Persons)</label>
                        <input type="number" id="sessionPax" min="1" step="1" value="1" class="w-full p-1 border rounded text-xs">
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-2 mb-3">
                    <div id="activityInputGroup">
                        <label class="block text-[10px] font-bold text-gray-500">ACTIVITY</label>
                        <select id="sessionActivity" class="w-full p-1 border rounded text-xs">
                            <option value="Kite">Kite</option>
                            <option value="Wing">Wing</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-[10px] font-bold text-gray-500">TYPE</label>
                        <select id="sessionType" class="w-full p-1 border rounded text-xs">
                            <option value="Semi-Private">Semi-Private</option>
                            <option value="Private">Private</option>
                        </select>
                    </div>
                </div>

                <button onclick="addItem()" class="w-full bg-black text-white font-bold py-2 rounded text-xs hover:bg-gray-800 transition">
                    ADD LINE
                </button>
            </div>

            <!-- Controls -->
            <div class="grid grid-cols-2 gap-3">
                <button onclick="clearAll()" class="bg-red-50 text-red-600 font-bold py-2 rounded border border-red-200 hover:bg-red-100 text-xs">
                    RESET
                </button>
                <button onclick="generatePDF()" class="bg-green-600 text-white font-bold py-2 rounded hover:bg-green-700 text-xs">
                    DOWNLOAD PDF
                </button>
            </div>
        </div>

        <!-- A4 PREVIEW -->
        <div class="w-full overflow-auto flex justify-center bg-gray-500 p-8 rounded-lg">
            <div id="invoice-element">
                
                <!-- Content Wrapper -->
                <div>
                    <!-- Header -->
                    <div class="flex justify-between items-start mb-6 border-b-2 border-black pb-4">
                        <div class="w-1/2">
                            <img id="logo-preview" src="" alt="Logo" class="h-20 object-contain mb-2 hidden">
                            <div id="logo-text-fallback">
                                <h1 class="text-3xl font-black italic font-serif">Dakhla Camp</h1>
                                <p class="text-xs font-bold tracking-[0.2em] uppercase">KiteSchool</p>
                            </div>
                        </div>
                        <div class="w-1/2 text-right pt-2">
                            <h2 class="text-2xl font-black uppercase tracking-tighter">DAKHLA CAMP KITESCHOOL</h2>
                            <p class="text-xs text-gray-600 uppercase font-bold mt-1">Kitesurf and Wingfoil</p>
                        </div>
                    </div>

                    <!-- Client Name -->
                    <div class="mb-4">
                        <div class="flex items-baseline mb-1">
                            <span class="font-bold text-sm mr-2 whitespace-nowrap">Client Name:</span>
                            <div class="text-sm font-bold" id="displayClientName"></div>
                        </div>
                    </div>

                    <!-- Table -->
                    <table class="camp-table">
                        <thead id="tableHead">
                            <!-- Headers injected by JS based on mode -->
                        </thead>
                        <tbody id="invoiceTableBody">
                            <!-- JS Generated Rows -->
                        </tbody>
                    </table>

                    <!-- Notes Section (Auto-expanding DIV) -->
                    <div class="mb-4">
                        <label class="font-bold text-xs uppercase text-gray-800 block mb-1">Package Details / Notes:</label>
                        <!-- Replaced textarea with contenteditable div for auto-height in PDF -->
                        <div 
                            id="invoiceNote" 
                            contenteditable="true" 
                            class="invoice-note-box"
                            placeholder="Add notes here..."
                        ></div>
                    </div>

                    <!-- TOTALS LAYOUT -->
                    <div class="totals-container">
                        <div class="totals-right-col">
                            
                            <!-- Breakdown Boxes -->
                            <div class="summary-boxes">
                                <!-- Semi Private Box -->
                                <div class="summary-box">
                                    <div class="summary-title">Semi-Private</div>
                                    <div class="summary-row">
                                        <span id="labelSummary1">Total Hours:</span>
                                        <span><span id="totalSemiQty">0</span><span id="unitSemi">h</span></span>
                                    </div>
                                    <div class="summary-row" style="margin-top: 8px;">
                                        <span class="font-bold">Price:</span>
                                        <span class="summary-price"><span id="priceSemi">0</span>€</span>
                                    </div>
                                </div>
                                
                                <!-- Private Box -->
                                <div class="summary-box">
                                    <div class="summary-title">Private</div>
                                    <div class="summary-row">
                                        <span id="labelSummary2">Total Hours:</span>
                                        <span><span id="totalPrivateQty">0</span><span id="unitPrivate">h</span></span>
                                    </div>
                                    <div class="summary-row" style="margin-top: 8px;">
                                        <span class="font-bold">Price:</span>
                                        <span class="summary-price"><span id="pricePrivate">0</span>€</span>
                                    </div>
                                </div>
                            </div>

                            <!-- Black Bar Euro -->
                            <div class="bar-euro">
                                <span>TOTAL EURO</span>
                                <span class="text-2xl"><span id="grandTotalEur">0</span>€</span>
                            </div>

                            <!-- Grey Bar MAD -->
                            <div class="bar-mad">
                                <span>TOTAL MAD</span>
                                <div>
                                    <span class="text-xs font-normal absolute top-0 right-1 transform -translate-y-full text-black mr-1 mb-1">Client Signature</span>
                                    <span class="text-2xl"><span id="grandTotalMad">0</span> MAD</span>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>

                <!-- Footer Signatures -->
                <div class="footer-area">
                    <div class="w-1/3">
                        <p class="font-bold text-xs uppercase tracking-wider mb-8 text-center">School Management</p>
                        <div class="signature-line"></div>
                    </div>
                    <div class="w-1/3"></div>
                </div>

            </div>
        </div>
    </div>

    <script>
        // --- PRICING DATA ---
        const LESSON_PRICING = {
            SEMI: { 
                table: { 
                    2: { eur: 90, mad: 990 },
                    4: { eur: 171, mad: 1881 },
                    6: { eur: 243, mad: 2673 },
                    8: { eur: 306, mad: 3366 },
                    10: { eur: 366, mad: 4026 },
                    12: { eur: 430, mad: 4818 } 
                },
                CALC_BASE_12: { eur: 438, mad: 4818 },
                EXTRA_1H: { eur: 36, mad: 396 },
                EXTRA_2H: { eur: 72, mad: 792 }
            },
            PRIVATE: { 
                table: { 
                    2: { eur: 135, mad: 1485 },
                    4: { eur: 252, mad: 2772 },
                    6: { eur: 360, mad: 3960 },
                    8: { eur: 446, mad: 5104 },
                    10: { eur: 549, mad: 6039 },
                    12: { eur: 657, mad: 7227 }
                },
                EXTRA_1H: { eur: 54, mad: 594 },
                EXTRA_2H: { eur: 108, mad: 1188 }
            }
        };

        const FACILITY_PRICING = {
            SEMI_PER_PAX: 10,
            PRIVATE_PER_PAX: 15,
            MAD_RATE: 11
        };

        const FACILITY_NOTE = "Facility Service: This includes secure storage for your equipment, the security boat service, and full assistance with launching and landing and supervision.";

        let currentMode = 'lessons'; 
        let items = [];
        
        const today = new Date().toISOString().split('T')[0];
        document.getElementById('invoiceDate').value = today;
        document.getElementById('sessionDate').value = today;

        function toggleMode() {
            const select = document.getElementById('invoiceMode');
            currentMode = select.value;
            
            const hoursGroup = document.getElementById('hoursInputGroup');
            const paxGroup = document.getElementById('paxInputGroup');
            const activityGroup = document.getElementById('activityInputGroup');
            const addHeader = document.getElementById('addHeader');
            const noteBox = document.getElementById('invoiceNote');

            if (currentMode === 'lessons') {
                hoursGroup.classList.remove('hidden');
                paxGroup.classList.add('hidden');
                activityGroup.classList.remove('hidden');
                addHeader.innerText = "ADD SESSION";
                document.getElementById('labelSummary1').innerText = "Total Hours:";
                document.getElementById('labelSummary2').innerText = "Total Hours:";
                document.getElementById('unitSemi').innerText = "h";
                document.getElementById('unitPrivate').innerText = "h";
                
                // Clear note only if it's the facility default
                if (noteBox.innerText === FACILITY_NOTE) {
                    noteBox.innerText = "";
                }
            } else {
                hoursGroup.classList.add('hidden');
                paxGroup.classList.remove('hidden');
                activityGroup.classList.add('hidden');
                addHeader.innerText = "ADD SERVICE DAY";
                document.getElementById('labelSummary1').innerText = "Total Days:";
                document.getElementById('labelSummary2').innerText = "Total Days:";
                document.getElementById('unitSemi').innerText = "d";
                document.getElementById('unitPrivate').innerText = "d";
                noteBox.innerText = FACILITY_NOTE;
            }

            if(items.length > 0 && confirm("Switching modes will clear current items. Continue?")) {
                items = [];
            } else if (items.length > 0) {
                select.value = currentMode === 'lessons' ? 'facility' : 'lessons'; 
                items = [];
            }
            updateUI();
        }

        function loadLogo(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = document.getElementById('logo-preview');
                    img.src = e.target.result;
                    img.classList.remove('hidden');
                    document.getElementById('logo-text-fallback').classList.add('hidden');
                };
                reader.readAsDataURL(file);
            }
        }

        function addItem() {
            const date = document.getElementById('sessionDate').value;
            const type = document.getElementById('sessionType').value;

            if (!date) return alert("Please select a date");

            if (currentMode === 'lessons') {
                const hours = parseFloat(document.getElementById('sessionHours').value);
                const activity = document.getElementById('sessionActivity').value;
                if (!hours || hours <= 0) return alert("Invalid Hours");
                items.push({ date, hours, activity, type, mode: 'lessons' });
            } else {
                const pax = parseInt(document.getElementById('sessionPax').value);
                if (!pax || pax <= 0) return alert("Invalid Pax");
                items.push({ date, pax, type, mode: 'facility' });
            }
            updateUI();
        }

        function removeItem(index) {
            items.splice(index, 1);
            updateUI();
        }

        function updateItemValue(index, val) {
            const num = parseFloat(val);
            if (num && num > 0) {
                if (currentMode === 'lessons') items[index].hours = num;
                else items[index].pax = num; 
                updateUI(false); 
            }
        }

        function calculateLessonPrice(totalHours, tierData) {
            if (totalHours <= 0) return { eur: 0, mad: 0 };
            const { table, EXTRA_1H, EXTRA_2H, CALC_BASE_12 } = tierData;

            if (Number.isInteger(totalHours) && table[totalHours]) return table[totalHours];

            if (totalHours > 12) {
                const basePrice = CALC_BASE_12 || table[12];
                const remainder = totalHours - 12;
                const pairs = Math.floor(remainder / 2);
                const singles = remainder % 2;
                return {
                    eur: basePrice.eur + (pairs * EXTRA_2H.eur) + (singles * EXTRA_1H.eur),
                    mad: basePrice.mad + (pairs * EXTRA_2H.mad) + (singles * EXTRA_1H.mad)
                };
            }
            if (totalHours < 12) {
                const floorEven = Math.floor(totalHours / 2) * 2;
                const remainder = totalHours - floorEven; 
                let basePrice = { eur: 0, mad: 0 };
                if (floorEven > 0) basePrice = table[floorEven];
                return {
                    eur: basePrice.eur + (remainder * EXTRA_1H.eur),
                    mad: basePrice.mad + (remainder * EXTRA_1H.mad)
                };
            }
            return { eur: 0, mad: 0 };
        }

        function calculateFacilityPrice(itemsList, type) {
            const relevantItems = itemsList.filter(i => i.type === type);
            let totalEur = 0;
            let totalDays = relevantItems.length; 

            relevantItems.forEach(i => {
                const rate = (type === 'Semi-Private') ? FACILITY_PRICING.SEMI_PER_PAX : FACILITY_PRICING.PRIVATE_PER_PAX;
                totalEur += rate * i.pax;
            });

            return {
                days: totalDays,
                eur: totalEur,
                mad: totalEur * FACILITY_PRICING.MAD_RATE
            };
        }

        function updateUI(shouldRenderTable = true) {
            document.getElementById('displayClientName').innerText = document.getElementById('clientName').value;
            const thead = document.getElementById('tableHead');
            const tbody = document.getElementById('invoiceTableBody');

            let totalSemi = 0; 
            let totalPrivate = 0;
            let priceSemi = { eur: 0, mad: 0 };
            let pricePrivate = { eur: 0, mad: 0 };

            if (currentMode === 'lessons') {
                if(shouldRenderTable) {
                    thead.innerHTML = `
                        <tr>
                            <th style="width: 25%;">Date</th>
                            <th style="width: 15%;">Wing</th>
                            <th style="width: 15%;">Kite</th>
                            <th style="width: 15%;">Private</th>
                            <th style="width: 15%;">Semi-Private</th>
                            <th style="width: 10%;">Hours</th>
                            <th style="width: 5%; border:none; background:white;" data-html2canvas-ignore="true"></th>
                        </tr>
                    `;
                    tbody.innerHTML = '';
                    items.forEach((item, index) => {
                        const tr = document.createElement('tr');
                        const check = '<i class="fa-solid fa-check"></i>';
                        tr.innerHTML = `
                            <td>${item.date}</td>
                            <td>${item.activity === 'Wing' ? check : ''}</td>
                            <td>${item.activity === 'Kite' ? check : ''}</td>
                            <td>${item.type === 'Private' ? check : ''}</td>
                            <td>${item.type === 'Semi-Private' ? check : ''}</td>
                            <td class="font-bold">
                                <input type="number" step="0.5" value="${item.hours}" onchange="updateItemValue(${index}, this.value)" class="editable-hours">
                            </td>
                            <td style="border:none; background:transparent;" data-html2canvas-ignore="true">
                                <button onclick="removeItem(${index})" class="text-red-500 hover:text-red-700 px-2 py-1"><i class="fa-solid fa-trash"></i></button>
                            </td>
                        `;
                        tbody.appendChild(tr);
                    });
                }

                items.forEach(i => {
                    if (i.type === 'Semi-Private') totalSemi += i.hours;
                    else totalPrivate += i.hours;
                });
                priceSemi = calculateLessonPrice(totalSemi, LESSON_PRICING.SEMI);
                pricePrivate = calculateLessonPrice(totalPrivate, LESSON_PRICING.PRIVATE);

            } else {
                if(shouldRenderTable) {
                    thead.innerHTML = `
                        <tr>
                            <th style="width: 30%;">Date</th>
                            <th style="width: 30%;">Service Type</th>
                            <th style="width: 20%;">Pax</th>
                            <th style="width: 20%;">Price (EUR)</th>
                            <th style="width: 5%; border:none; background:white;" data-html2canvas-ignore="true"></th>
                        </tr>
                    `;
                    tbody.innerHTML = '';
                    items.forEach((item, index) => {
                        const tr = document.createElement('tr');
                        const rate = (item.type === 'Semi-Private') ? FACILITY_PRICING.SEMI_PER_PAX : FACILITY_PRICING.PRIVATE_PER_PAX;
                        const linePrice = rate * item.pax;
                        tr.innerHTML = `
                            <td>${item.date}</td>
                            <td>Facility - ${item.type}</td>
                            <td class="font-bold">
                                <input type="number" min="1" step="1" value="${item.pax}" onchange="updateItemValue(${index}, this.value)" class="editable-hours">
                            </td>
                            <td>${linePrice}€</td>
                            <td style="border:none; background:transparent;" data-html2canvas-ignore="true">
                                <button onclick="removeItem(${index})" class="text-red-500 hover:text-red-700 px-2 py-1"><i class="fa-solid fa-trash"></i></button>
                            </td>
                        `;
                        tbody.appendChild(tr);
                    });
                }

                const semiResult = calculateFacilityPrice(items, 'Semi-Private');
                const privateResult = calculateFacilityPrice(items, 'Private');
                
                totalSemi = semiResult.days;
                priceSemi = { eur: semiResult.eur, mad: semiResult.mad };
                
                totalPrivate = privateResult.days;
                pricePrivate = { eur: privateResult.eur, mad: privateResult.mad };
            }

            document.getElementById('totalSemiQty').innerText = totalSemi;
            document.getElementById('priceSemi').innerText = priceSemi.eur.toFixed(0);
            
            document.getElementById('totalPrivateQty').innerText = totalPrivate;
            document.getElementById('pricePrivate').innerText = pricePrivate.eur.toFixed(0);

            const totalEur = priceSemi.eur + pricePrivate.eur;
            const totalMad = priceSemi.mad + pricePrivate.mad;

            document.getElementById('grandTotalEur').innerText = totalEur.toFixed(0);
            document.getElementById('grandTotalMad').innerText = totalMad.toFixed(0);
        }

        function clearAll() {
            items = [];
            document.getElementById('clientName').value = '';
            // Reset note
            const noteBox = document.getElementById('invoiceNote');
            if(currentMode === 'lessons') noteBox.innerText = '';
            else noteBox.innerText = FACILITY_NOTE;
            updateUI();
        }

        function generatePDF() {
            const element = document.getElementById('invoice-element');
            const name = document.getElementById('clientName').value || 'Invoice';
            const suffix = currentMode === 'facility' ? '_Facility' : '';
            
            const opt = {
                margin:       0,
                filename:     `DakhlaCamp_${name.replace(/\s+/g, '_')}${suffix}.pdf`,
                image:        { type: 'jpeg', quality: 0.98 },
                html2canvas:  { scale: 2, useCORS: true, scrollY: 0 }, 
                jsPDF:        { unit: 'mm', format: 'a4', orientation: 'portrait' },
                pagebreak:    { mode: ['avoid-all', 'css', 'legacy'] }
            };
            html2pdf().set(opt).from(element).save();
        }

        // Init
        updateUI();
        document.getElementById('clientName').addEventListener('input', () => updateUI(false));
        document.getElementById('invoiceDate').addEventListener('change', () => updateUI(false));
    </script>
</body>
</html>
