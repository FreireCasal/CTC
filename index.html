<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>India CTC and Net Take Home Calculator</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font (3. Spacing & Typography) -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* 1. COLOR SYSTEM & 3. TYPOGRAPHY */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f7f7;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            padding: 2rem 1rem;
        }

        /* Set base text color for the entire application (1. Gray 6) */
        #calculator-app, 
        .input-group label, 
        .summary-item h4, 
        .summary-item p {
            color: #323232 !important; /* Gray 6: All text on light backgrounds */
        }
        
        /* A) INPUT BAR (Top Panel) */
        .input-panel-container {
            background-color: #F8F8F8;
            border: 1px solid #DFDFDF; /* Gray 3 border */
            border-radius: 8px;
            padding: 1.5rem;
        }
        .input-group label {
            font-size: 13px; /* 3. Typography: Small labels */
            font-weight: 500;
            margin-bottom: 0.25rem;
            display: block; /* Ensure label is block */
        }
        .input-group input, .input-group select {
            width: 100%;
            padding: 8px 12px;
            border-radius: 6px;
            border: 1px solid #DFDFDF; /* Gray 3 border */
            outline: none;
            transition: border-color 0.15s;
            background-color: white; /* Fix visual overlap issue */
        }
        .input-group input:focus, .input-group select:focus {
            border-color: #55AAC3; /* Blue focus indicator */
            box-shadow: 0 0 0 1px #55AAC3;
        }

        /* FIX: Increased padding for icon alignment (32px to 40px equivalent) */
        .input-with-icon {
            padding-left: 3rem !important; /* p-12 in Tailwind is 3rem = 48px, but since we are using fixed padding in the CSS above, we use an inline class or more specific styling */
        }

        /* B) SUMMARY CARD */
        .summary-card-container {
            background-color: white;
            border-radius: 8px; /* Rounded corners */
            box-shadow: 0 4px 12px -2px rgba(0, 0, 0, 0.05); /* Subtle shadow */
            padding: 1.5rem;
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 1.5rem;
            border: 1px solid #F0F0F0; /* Light border for definition */
        }
        @media (min-width: 768px) {
            .summary-card-container {
                grid-template-columns: repeat(4, minmax(0, 1fr));
            }
        }
        .summary-item h4 {
            font-size: 13px;
            font-weight: 500;
            margin-bottom: 0.25rem;
            text-transform: uppercase;
        }
        .summary-item p {
            font-size: 18px;
            font-weight: 700;
        }

        /* C) TABLE REDESIGN */
        .result-table-card {
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #DFDFDF; /* Gray 3 border */
            background-color: white;
            box-shadow: 0 4px 12px -2px rgba(0, 0, 0, 0.05);
        }
        .result-table {
            table-layout: fixed;
        }
        .result-table th, .result-table td {
            padding: 10px 12px; /* 3. Reduced padding to ~10-12px */
            font-size: 14px; /* 3. Row labels: 13–14px, Numeric values: 14px */
            color: #323232; /* Gray 6 */
            border-bottom: 1px solid #DFDFDF; /* Gray 3 Table grid/lines */
        }
        .result-table thead th {
            font-weight: 600;
            background-color: #DFDFDF; /* Gray 3 background (Table header row) */
            border-bottom: 1px solid #DFDFDF;
            font-size: 13px;
        }
        /* Right-align numeric values (C) */
        .result-table td:nth-child(2), 
        .result-table td:nth-child(3) {
            text-align: right; 
            font-weight: 500;
        }
        .result-table th {
            text-align: left;
            font-weight: 400; /* Regular weight for data labels */
        }
        /* Remove bottom border on the last visible row before a section header or a footer */
        .result-table tbody tr:last-child td, 
        .result-table tbody tr:last-child th {
             border-bottom: none;
        }
        
        /* D) SECTION TITLES (Band Headers) */
        .section-header-band th {
            background-color: #DFDFDF; /* Gray 3 */
            color: #323232; /* Gray 6 */
            font-size: 15px; /* 3. Section titles: 14–15px */
            font-weight: 600; /* Medium font weight */
            padding: 8px 12px;
            border-bottom: 1px solid #DFDFDF;
            border-top: 1px solid #DFDFDF;
        }
        
        /* E) COLOR BARS FOR SUBTOTALS (Subtotal Rows Only) */
        .subtotal-bar th, .subtotal-bar td {
            font-weight: 700;
            color: white !important; /* Default white text on colored bars for contrast */
            border-bottom: none;
            font-size: 14px;
        }
        
        /* FIXED CTC & TOTAL CTC (Blue) */
        .subtotal-bar-blue th, .subtotal-bar-blue td {
            background-color: #55AAC3; /* Blue */
        }
        
        /* Income Tax estimate (Orange) */
        .subtotal-bar-tax th, .subtotal-bar-tax td {
            background-color: #FFCB8B; /* Orange */
            color: #323232 !important; /* Gray 6 text for contrast on light orange */
        }
        
        /* TOTAL DEDUCTION (Purple) */
        .subtotal-bar-deduction th, .subtotal-bar-deduction td {
            background-color: #B38DC8; /* Purple */
        }

        /* NET TAKE HOME (Green 3) */
        .subtotal-bar-net th, .subtotal-bar-net td {
            background-color: #5EBA83; /* Green 3 */
            font-size: 16px;
        }
        
        /* Old Regime Info Box */
        .old-regime-info {
            background-color: #fffbeb;
            border: 1px solid #fde68a;
            color: #b45309;
        }
    </style>
</head>
<body>

<div id="calculator-app" class="w-full max-w-4xl bg-white rounded-xl p-8">
    <h1 class="text-2xl font-bold mb-6 text-center" style="color: #323232;">India CTC & Net Take Home Estimator</h1>
    <p class="text-sm text-center mb-6" style="color: #323232;">Enter the <span class="font-bold">Annual Gross Salary</span> and select your options to calculate the full CTC breakdown.</p>

    <!-- INPUT BAR (A) -->
    <div id="inputs-section" class="input-panel-container mb-6">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <!-- Annual Gross Salary Input -->
            <div class="input-group">
                <!-- FIX: Removed (₹) from the label -->
                <label for="grossSalary">Annual Gross Salary</label> 
                <div class="relative">
                    <!-- FIX: Icon positioned left-3 -->
                    <svg class="absolute left-3 top-1/2 transform -translate-y-1/2 w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 8h6m-5 0s1 4 5 4m-5 4h6m-1 3.5l1-1.5m-3-1l-1-1.5m3-1l1-1.5m-3-1l-1-1.5m2-2l-1-1.5m2 2V5m-4 14v-4m-3-1h8m-8-2h8m-8-2h8"></path></svg>
                    <!-- FIX: Increased padding to pl-12 (48px) for clear separation -->
                    <input type="number" id="grossSalary" placeholder="0" min="0" class="input-with-icon pl-12 pr-3" oninput="calculateCTC()">
                </div>
            </div>

            <!-- Tax Regime Selection (No icon change here) -->
            <div class="input-group">
                <label>Income Tax Regime</label>
                <select id="taxRegime" onchange="toggleOldRegimeAllowances(); calculateCTC()">
                    <option value="new">New Regime (Slab Tax)</option>
                    <option value="old">Old Regime (Slab Tax)</option>
                </select>
            </div>

            <!-- PF Contribution Selection -->
            <div class="input-group">
                <label>Employer PF Contribution</label>
                <div class="relative">
                    <!-- FIX: Icon positioned left-3 -->
                    <svg class="absolute left-3 top-1/2 transform -translate-y-1/2 w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c1.657 0 3 1.343 3 3s-1.343 3-3 3 1.343-3 3-3zM10 20v-5m4 0v5m-4-7h4m-4 0v-4m4 4h4m-4-4v4"></path></svg>
                    <!-- FIX: Increased padding to pl-12 (48px) for clear separation -->
                    <select id="pfOption" class="input-with-icon pl-12 pr-3" onchange="calculateCTC()">
                        <option value="percentage">12% of Basic Salary</option>
                        <option value="fixed">INR 1,800 per month (₹21,600 annual)</option>
                    </select>
                </div>
            </div>
        </div>
    </div>

    <!-- SUMMARY CARD (B) -->
    <div class="summary-card-container mb-8">
        <div class="summary-item">
            <h4>Annual CTC</h4>
            <p id="summaryAnnualCTC" style="color: #55AAC3;">—</p>
        </div>
        <div class="summary-item">
            <h4>Monthly Net Take Home</h4>
            <p id="summaryNetTakeHomeMonthly" style="color: #5EBA83;">—</p>
        </div>
        <div class="summary-item">
            <h4>PF Mode</h4>
            <p id="summaryPFMode" class="text-sm">—</p>
        </div>
        <div class="summary-item">
            <h4>Tax Regime</h4>
            <p id="summaryTaxRegime" class="text-sm">—</p>
        </div>
    </div>

    <!-- OLD REGIME ALLOWANCES (Conditional - Information Only) -->
    <div id="oldRegimeAllowances" class="p-4 old-regime-info rounded-lg mb-8 hidden">
        <h3 class="text-base font-semibold mb-2">Old Regime Exemptions (Informational Only)</h3>
        <p class="text-sm mb-2">The components below are included in the Gross Salary breakdown, but for this simplified slab-based tax calculation, <span class="font-bold">no exemptions or deductions are applied</span> (HRA, Standard Deduction, 80C, etc., are ignored).</p>
    </div>

    <!-- C) RESULTS TABLE CONTAINER -->
    <div id="results-container" class="result-table-card">
        
        <!-- Conditional Table Rendering: New Regime vs. Old Regime -->
        <table id="ctc-table-new" class="result-table w-full border-collapse" style="display: none;">
             <!-- NEW REGIME TABLE (SIMPLE STRUCTURE) -->
            <thead>
                <tr>
                    <th class="w-1/2">Description</th>
                    <th class="w-1/4">Annual (₹)</th>
                    <th class="w-1/4">Monthly (₹)</th>
                </tr>
            </thead>
            <tbody>
                
                <!-- Section 1: Direct Benefits (Fixed CTC Components) -->
                <tr class="section-header-band">
                    <th colspan="3">I. Direct Benefits (Fixed CTC Components)</th>
                </tr>
                <tr>
                    <th>Basic Salary (50% on CTC)</th>
                    <td id="basicAnnualNew">—</td>
                    <td id="basicMonthlyNew">—</td>
                </tr>
                <tr>
                    <th>HRA (40% on Basic)</th>
                    <td id="hraAnnualNew">—</td>
                    <td id="hraMonthlyNew">—</td>
                </tr>
                <tr>
                    <th>Special Allowance</th>
                    <td id="specialAllowanceAnnualNew">—</td>
                    <td id="specialAllowanceMonthlyNew">—</td>
                </tr>
                
                <!-- Subtotal: FIXED CTC (Blue) -->
                <tr class="subtotal-bar subtotal-bar-blue">
                    <th>FIXED CTC</th>
                    <td id="fixedCTCAnnualNew">—</td>
                    <td id="fixedCTCMonthlyNew">—</td>
                </tr>

                <!-- Section 2: Employer Savings (PF) -->
                <tr class="section-header-band">
                    <th colspan="3">II. Employer Savings (PF)</th>
                </tr>
                <tr>
                    <th>Employer PF Contribution (<span id="pfRateDisplayNew">12% of Basic Salary</span>)</th>
                    <td id="employerPFAnnualNew">—</td>
                    <td id="employerPFMonthlyNew">—</td>
                </tr>

                <!-- Section 3: Cost to Company (Total CTC) -->
                <tr class="section-header-band">
                    <th colspan="3">III. Cost to Company (Total CTC)</th>
                </tr>
                <!-- Subtotal: TOTAL CTC (Blue) -->
                <tr class="subtotal-bar subtotal-bar-blue">
                    <th>TOTAL CTC</th>
                    <td id="annualCTCNew">—</td>
                    <td id="monthlyCTCNew">—</td>
                </tr>
                
                <!-- Section 4: Employee Deductions -->
                <tr class="section-header-band">
                    <th colspan="3">IV. Employee Deductions</th>
                </tr>
                
                <!-- Deductions -->
                <tr>
                    <th>Employee PF Contribution</th>
                    <td id="employeePFAnnualNew">—</td>
                    <td id="employeePFMonthlyNew">—</td>
                </tr>
                <tr>
                    <th>Professional Tax</th>
                    <td id="ptAnnualNew">—</td>
                    <td id="ptMonthlyNew">—</td>
                </tr>
                <!-- E) Subtotal: Income Tax Estimate (Orange) -->
                <tr class="subtotal-bar subtotal-bar-tax">
                    <th>Income Tax (<span id="regimeDisplayNew">New Regime (Slab Tax)</span>)</th>
                    <td id="incomeTaxAnnualNew">—</td>
                    <td id="incomeTaxMonthlyNew">—</td>
                </tr>
                
                <!-- E) Subtotal: TOTAL DEDUCTION (Purple) -->
                <tr class="subtotal-bar subtotal-bar-deduction">
                    <th>TOTAL DEDUCTION</th>
                    <td id="totalDeductionAnnualNew">—</td>
                    <td id="totalDeductionMonthlyNew">—</td>
                </tr>
                
                <!-- D) Section 5: Net Take Home (Final) -->
                <tr class="section-header-band">
                    <th colspan="3">V. Net Take Home (Final)</th>
                </tr>
                <!-- E) Final Take Home (Green 3) -->
                <tr class="subtotal-bar subtotal-bar-net">
                    <th>TOTAL NET TAKE HOME (ESTIMATE)</th>
                    <td id="netTakeHomeAnnualNew">—</td>
                    <td id="netTakeHomeMonthlyNew">—</td>
                </tr>
            </tbody>
        </table>

        <!-- OLD REGIME TABLE (EXPANDED STRUCTURE - Default current structure) -->
        <table id="ctc-table-old" class="result-table w-full border-collapse" style="display: none;">
            <thead>
                <tr>
                    <th class="w-1/2">Description</th>
                    <th class="w-1/4">Annual (₹)</th>
                    <th class="w-1/4">Monthly (₹)</th>
                </tr>
            </thead>
            <tbody>
                
                <!-- Section 1: Direct Benefits (Fixed CTC Components) -->
                <tr class="section-header-band">
                    <th colspan="3">I. Direct Benefits (Fixed CTC Components)</th>
                </tr>
                <tr>
                    <th>Basic Salary (50% of CTC)</th>
                    <td id="basicAnnualOld">—</td>
                    <td id="basicMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>House Rent Allowance (HRA) (40% of Basic)</th>
                    <td id="hraAnnualOld">—</td>
                    <td id="hraMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Leave Travel Allowance (LTA) (1 Month Basic)</th>
                    <td id="ltaAnnualOld">—</td>
                    <td id="ltaMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Children Education Allowance (CEA)</th>
                    <td id="ceaAnnualOld">—</td>
                    <td id="ceaMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Telephone/Internet Allowance</th>
                    <td id="telephoneAnnualOld">—</td>
                    <td id="telephoneMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Meal/Sodexo Coupons</th>
                    <td id="sodexoAnnualOld">—</td>
                    <td id="sodexoMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Car Repair & Maintenance</th>
                    <td id="carRepairAnnualOld">—</td>
                    <td id="carRepairMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Professional Development</th>
                    <td id="profDevAnnualOld">—</td>
                    <td id="profDevMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Books & Periodicals</th>
                    <td id="booksAnnualOld">—</td>
                    <td id="booksMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Special Allowance (Balancing Figure)</th>
                    <td id="specialAllowanceAnnualOld">—</td>
                    <td id="specialAllowanceMonthlyOld">—</td>
                </tr>
                
                <!-- E) Subtotal: FIXED CTC (Blue) -->
                <tr class="subtotal-bar subtotal-bar-blue">
                    <th>FIXED CTC (Annual Gross Salary)</th>
                    <td id="fixedCTCAnnualOld">—</td>
                    <td id="fixedCTCMonthlyOld">—</td>
                </tr>

                <!-- D) Section 2: Employer Savings (PF) -->
                <tr class="section-header-band">
                    <th colspan="3">II. Employer Savings (PF)</th>
                </tr>
                <tr>
                    <th>Employer PF Contribution (<span id="pfRateDisplayOld">12% of Basic Salary</span>)</th>
                    <td id="employerPFAnnualOld">—</td>
                    <td id="employerPFMonthlyOld">—</td>
                </tr>

                <!-- D) Section 3: Cost to Company (Total CTC) -->
                <tr class="section-header-band">
                    <th colspan="3">III. Cost to Company (Total CTC)</th>
                </tr>
                <!-- E) Subtotal: TOTAL CTC (Blue) -->
                <tr class="subtotal-bar subtotal-bar-blue">
                    <th>ANNUAL CTC</th>
                    <td id="annualCTCOld">—</td>
                    <td id="monthlyCTCOld">—</td>
                </tr>
                
                <!-- D) Section 4: Employee Deductions -->
                <tr class="section-header-band">
                    <th colspan="3">IV. Employee Deductions</th>
                </tr>
                
                <!-- Deductions -->
                <tr>
                    <th>Employee PF Contribution</th>
                    <td id="employeePFAnnualOld">—</td>
                    <td id="employeePFMonthlyOld">—</td>
                </tr>
                <tr>
                    <th>Professional Tax</th>
                    <td id="ptAnnualOld">—</td>
                    <td id="ptMonthlyOld">—</td>
                </tr>
                <!-- E) Subtotal: Income Tax Estimate (Orange) -->
                <tr class="subtotal-bar subtotal-bar-tax">
                    <th>Estimated Income Tax (<span id="regimeDisplayOld">Old Regime (Slab Tax)</span>)</th>
                    <td id="incomeTaxAnnualOld">—</td>
                    <td id="incomeTaxMonthlyOld">—</td>
                </tr>
                
                <!-- E) Subtotal: TOTAL DEDUCTION (Purple) -->
                <tr class="subtotal-bar subtotal-bar-deduction">
                    <th>TOTAL DEDUCTION</th>
                    <td id="totalDeductionAnnualOld">—</td>
                    <td id="totalDeductionMonthlyOld">—</td>
                </tr>
                
                <!-- D) Section 5: Net Take Home (Final) -->
                <tr class="section-header-band">
                    <th colspan="3">V. Net Take Home (Final)</th>
                </tr>
                <!-- E) Final Take Home (Green 3) -->
                <tr class="subtotal-bar subtotal-bar-net">
                    <th>TOTAL NET TAKE HOME (ESTIMATE)</th>
                    <td id="netTakeHomeAnnualOld">—</td>
                    <td id="netTakeHomeMonthlyOld">—</td>
                </tr>
            </tbody>
        </table>
    </div>
    
    <div class="flex justify-center mt-6">
        <!-- 5. PDF BUTTON (Blue) -->
        <button onclick="downloadPDF()" class="bg-[#55AAC3] hover:bg-[#3F8DA6] text-white font-semibold py-2 px-6 rounded-lg shadow-lg transition duration-150 flex items-center">
             <!-- Document/Download Icon -->
            <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
            Download Full PDF Report
        </button>
    </div>
    <p class="text-xs text-gray-500 mt-4 text-center" style="color: #323232;">Disclaimer: This tool provides an <strong>estimation</strong> strictly based on the defined model logic. Actual tax and net take-home salary may vary significantly.</p>

</div>

<!-- jsPDF and html2canvas CDNs for PDF generation -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>

<script>
    // --- CONFIGURATION CONSTANTS ---
    const CEA_ANNUAL = 2400;
    const TELEPHONE_ANNUAL = 36000;
    const SODEXO_ANNUAL = 36000;
    const CAR_REPAIR_ANNUAL = 28000;
    const PROF_DEV_ANNUAL = 36000;
    const BOOKS_ANNUAL = 36000;
    const PROFESSIONAL_TAX_ANNUAL = 2400;
    const MONTHS_PER_YEAR = 12;

    // --- 4. NUMBER FORMATTING (English-India Excel style) ---
    const formatCurrencyDisplay = (value) => {
        // Replace zero values with a dash '—'
        if (value === 0 || value === null || isNaN(value)) {
            return '—';
        }

        const roundedValue = Math.round(value);
        const isNegative = roundedValue < 0;
        const absValue = Math.abs(roundedValue);

        // Use en-US locale for Western grouping (600,000)
        const numberFormatter = new Intl.NumberFormat('en-US', {
            style: 'decimal',
            minimumFractionDigits: 0,
            maximumFractionDigits: 0,
        });

        const numberString = numberFormatter.format(absValue);

        // Construct the final string: [optional -] + ₹ + Space + numberString
        let result = `₹ ${numberString}`;

        if (isNegative) {
            result = `-${result}`;
        }
        
        return result;
    };
    
    // --- TAX CALCULATION HELPERS (Based on the prompt slabs) ---

    // New Regime Tax Slabs (Includes 4% Cess)
    function computeNewRegimeTax(taxableIncome) {
        let tax = 0;
        let income = taxableIncome;
        
        // Slabs: 3L@0, 3-6L@5%, 6-9L@10%, 9-12L@15%, 12-15L@20%, >15L@30%
        if (income > 1500000) {
            tax += (income - 1500000) * 0.30;
            income = 1500000;
        }
        if (income > 1200000) {
            tax += (income - 1200000) * 0.20;
            income = 1200000;
        }
        if (income > 900000) {
            tax += (income - 900000) * 0.15;
            income = 900000;
        }
        if (income > 600000) {
            tax += (income - 600000) * 0.10;
            income = 600000;
        }
        if (income > 300000) {
            tax += (income - 300000) * 0.05;
            income = 300000;
        }
        
        let totalTax = tax * 1.04; // Apply 4% Cess
        
        return Math.round(Math.max(0, totalTax));
    }

    // Old Regime Tax Slabs (Includes 4% Cess)
    function computeOldRegimeTax(taxableIncome) {
        let tax = 0;
        let income = taxableIncome;

        // Slabs: 2.5L@0, 2.5-5L@5%, 5-10L@20%, >10L@30%
        if (income > 1000000) {
            tax += (income - 1000000) * 0.30;
            income = 1000000;
        }
        if (income > 500000) {
            tax += (income - 500000) * 0.20;
            income = 500000;
        }
        if (income > 250000) {
            tax += (income - 250000) * 0.05;
            income = 250000;
        }
        
        let totalTax = tax * 1.04; // Apply 4% Cess

        return Math.round(Math.max(0, totalTax));
    }

    // Helper to clear all results to '—' (C)
    function clearResults() {
        // Collect all potential IDs for both tables
        const ids = [
            // New Regime IDs
            'annualCTCNew', 'monthlyCTCNew', 'basicAnnualNew', 'basicMonthlyNew', 'hraAnnualNew', 'hraMonthlyNew', 
            'specialAllowanceAnnualNew', 'specialAllowanceMonthlyNew', 'fixedCTCAnnualNew', 'fixedCTCMonthlyNew', 
            'employerPFAnnualNew', 'employerPFMonthlyNew', 'employeePFAnnualNew', 'employeePFMonthlyNew', 
            'ptAnnualNew', 'ptMonthlyNew', 'incomeTaxAnnualNew', 'incomeTaxMonthlyNew', 
            'totalDeductionAnnualNew', 'totalDeductionMonthlyNew', 'netTakeHomeAnnualNew', 'netTakeHomeMonthlyNew',
            
            // Old Regime IDs
            'annualCTCOld', 'monthlyCTCOld', 'basicAnnualOld', 'basicMonthlyOld', 'hraAnnualOld', 'hraMonthlyOld', 
            'ltaAnnualOld', 'ltaMonthlyOld', 'ceaAnnualOld', 'ceaMonthlyOld', 'telephoneAnnualOld', 'telephoneMonthlyOld', 
            'sodexoAnnualOld', 'sodexoMonthlyOld', 'carRepairAnnualOld', 'carRepairMonthlyOld', 'profDevAnnualOld', 'profDevMonthlyOld', 
            'booksAnnualOld', 'booksMonthlyOld', 'specialAllowanceAnnualOld', 'specialAllowanceMonthlyOld', 
            'fixedCTCAnnualOld', 'fixedCTCMonthlyOld', 'employerPFAnnualOld', 'employerPFMonthlyOld', 
            'employeePFAnnualOld', 'employeePFMonthlyOld', 'ptAnnualOld', 'ptMonthlyOld', 
            'incomeTaxAnnualOld', 'incomeTaxMonthlyOld', 'totalDeductionAnnualOld', 'totalDeductionMonthlyOld', 
            'netTakeHomeAnnualOld', 'netTakeHomeMonthlyOld',
            
            // Summary Card IDs
            'summaryAnnualCTC', 'summaryNetTakeHomeMonthly'
        ];
        
        ids.forEach(id => {
            const element = document.getElementById(id);
            if (element) element.textContent = '—';
        });
        
        // Reset dynamic displays and Summary Card texts
        const pfOption = document.getElementById('pfOption');
        const taxRegime = document.getElementById('taxRegime');

        document.getElementById('pfRateDisplayNew').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('pfRateDisplayOld').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('regimeDisplayNew').textContent = taxRegime.options[taxRegime.selectedIndex].textContent;
        document.getElementById('regimeDisplayOld').textContent = taxRegime.options[taxRegime.selectedIndex].textContent;
        document.getElementById('summaryPFMode').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('summaryTaxRegime').textContent = taxRegime.options[taxRegime.selectedIndex].textContent;
    }


    // --- MAIN CTC CALCULATION ---
    
    function calculateCTC() {
        const grossSalaryInput = document.getElementById('grossSalary').value;
        const annual_gross_salary = parseFloat(grossSalaryInput) || 0;
        
        const pf_mode_selection = document.getElementById('pfOption').value;
        const tax_regime = document.getElementById('taxRegime').value;
        const pf_mode = (pf_mode_selection === 'percentage') ? 'PERCENT_12' : 'CAP_1800';

        if (annual_gross_salary <= 0 && grossSalaryInput !== '0') {
            clearResults();
            renderTable(tax_regime); // Still render the correct empty table
            return;
        }
        
        // --- 1) ANNUAL CTC (Derived from Gross) ---
        // Note: The logic fixed_ctc_annual * 0.94 should equal gross_salary.
        const annual_ctc = Math.round(annual_gross_salary / 0.94);

        // --- 2) BASIC (50% of CTC) AND HRA (40% OF BASIC) ---
        const basic_annual = Math.round(annual_ctc * 0.50);
        const basic_monthly = Math.round(basic_annual / MONTHS_PER_YEAR);
        const hra_annual = Math.round(basic_annual * 0.40);
        const hra_monthly = Math.round(hra_annual / MONTHS_PER_YEAR);

        // --- 3) ALLOWANCES (fixed annuals are constants) ---
        const lta_annual = basic_monthly;
        const lta_monthly = Math.round(lta_annual / MONTHS_PER_YEAR);

        const cea_annual = CEA_ANNUAL;
        const telephone_annual = TELEPHONE_ANNUAL;
        const sodexo_annual = SODEXO_ANNUAL;
        const car_repair_annual = CAR_REPAIR_ANNUAL;
        const prof_dev_annual = PROF_DEV_ANNUAL;
        const books_annual = BOOKS_ANNUAL;

        const cea_monthly = Math.round(cea_annual / MONTHS_PER_YEAR);
        const telephone_monthly = Math.round(telephone_annual / MONTHS_PER_YEAR);
        const sodexo_monthly = Math.round(sodexo_annual / MONTHS_PER_YEAR);
        const car_repair_monthly = Math.round(car_repair_annual / MONTHS_PER_YEAR);
        const prof_dev_monthly = Math.round(prof_dev_annual / MONTHS_PER_YEAR);
        const books_monthly = Math.round(books_annual / MONTHS_PER_YEAR);
        
        // --- 4) SPECIAL ALLOWANCE & FIXED CTC ---
        const sum_fixed_components_without_special =
            basic_annual + hra_annual + lta_annual + cea_annual + telephone_annual
            + sodexo_annual + car_repair_annual + prof_dev_annual + books_annual;

        const special_allowance_annual = annual_ctc - sum_fixed_components_without_special;
        const special_allowance_monthly = Math.round(special_allowance_annual / MONTHS_PER_YEAR);

        const fixed_ctc_annual = sum_fixed_components_without_special + special_allowance_annual;
        const fixed_ctc_monthly = Math.round(fixed_ctc_annual / MONTHS_PER_YEAR);
        
        // --- 5) PROVIDENT FUND – 2 MODES ---
        let employer_pf_annual, employer_pf_monthly;

        if (pf_mode === "PERCENT_12") {
            employer_pf_annual = Math.round(basic_annual * 0.12);
            employer_pf_monthly = Math.round(employer_pf_annual / MONTHS_PER_YEAR);
        } else { // pf_mode === "CAP_1800"
            employer_pf_monthly = 1800;
            employer_pf_annual = employer_pf_monthly * MONTHS_PER_YEAR;
        }

        const employee_pf_annual = employer_pf_annual;
        const employee_pf_monthly = employer_pf_monthly;

        // --- 6) TOTAL CTC ---
        const total_ctc_annual = fixed_ctc_annual + employer_pf_annual;
        const total_ctc_monthly = fixed_ctc_monthly + employer_pf_monthly;

        // --- 7) EMPLOYEE DEDUCTIONS ---
        const prof_tax_annual = PROFESSIONAL_TAX_ANNUAL;
        const prof_tax_monthly = Math.round(prof_tax_annual / MONTHS_PER_YEAR);

        const taxable_income = fixed_ctc_annual;
        let income_tax_annual;
        
        if (tax_regime === "new") {
            income_tax_annual = computeNewRegimeTax(taxable_income);
        } else {
            income_tax_annual = computeOldRegimeTax(taxable_income); 
        }

        const income_tax_monthly = Math.round(income_tax_annual / MONTHS_PER_YEAR);

        const total_deductions_annual = employee_pf_annual + prof_tax_annual + income_tax_annual;
        const total_deductions_monthly = employee_pf_monthly + prof_tax_monthly + income_tax_monthly;

        // --- 8) NET TAKE-HOME (ESTIMATE) ---
        const net_take_home_annual = fixed_ctc_annual - total_deductions_annual;
        const net_take_home_monthly = fixed_ctc_monthly - total_deductions_monthly;

        // --- FINAL UI UPDATE (Conditional based on regime) ---
        
        // Update dynamic text displays
        const pfOption = document.getElementById('pfOption');
        document.getElementById('pfRateDisplayNew').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('pfRateDisplayOld').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('regimeDisplayNew').textContent = tax_regime === 'new' ? 'New Regime (Slab Tax)' : 'Old Regime (Slab Tax)';
        document.getElementById('regimeDisplayOld').textContent = tax_regime === 'new' ? 'New Regime (Slab Tax)' : 'Old Regime (Slab Tax)';
        
        // Summary Card Update (B)
        document.getElementById('summaryAnnualCTC').textContent = formatCurrencyDisplay(total_ctc_annual);
        document.getElementById('summaryNetTakeHomeMonthly').textContent = formatCurrencyDisplay(net_take_home_monthly);
        document.getElementById('summaryPFMode').textContent = pfOption.options[pfOption.selectedIndex].textContent;
        document.getElementById('summaryTaxRegime').textContent = tax_regime === 'new' ? 'New Regime' : 'Old Regime';


        if (tax_regime === 'new') {
            // New Regime (Simple structure)
            document.getElementById('basicAnnualNew').textContent = formatCurrencyDisplay(basic_annual);
            document.getElementById('basicMonthlyNew').textContent = formatCurrencyDisplay(basic_monthly);
            document.getElementById('hraAnnualNew').textContent = formatCurrencyDisplay(hra_annual);
            document.getElementById('hraMonthlyNew').textContent = formatCurrencyDisplay(hra_monthly);
            document.getElementById('specialAllowanceAnnualNew').textContent = formatCurrencyDisplay(special_allowance_annual);
            document.getElementById('specialAllowanceMonthlyNew').textContent = formatCurrencyDisplay(special_allowance_monthly);
            document.getElementById('fixedCTCAnnualNew').textContent = formatCurrencyDisplay(fixed_ctc_annual);
            document.getElementById('fixedCTCMonthlyNew').textContent = formatCurrencyDisplay(fixed_ctc_monthly);
            document.getElementById('employerPFAnnualNew').textContent = formatCurrencyDisplay(employer_pf_annual);
            document.getElementById('employerPFMonthlyNew').textContent = formatCurrencyDisplay(employer_pf_monthly);
            document.getElementById('annualCTCNew').textContent = formatCurrencyDisplay(total_ctc_annual);
            document.getElementById('monthlyCTCNew').textContent = formatCurrencyDisplay(total_ctc_monthly);
            document.getElementById('employeePFAnnualNew').textContent = formatCurrencyDisplay(employee_pf_annual);
            document.getElementById('employeePFMonthlyNew').textContent = formatCurrencyDisplay(employee_pf_monthly);
            document.getElementById('ptAnnualNew').textContent = formatCurrencyDisplay(prof_tax_annual);
            document.getElementById('ptMonthlyNew').textContent = formatCurrencyDisplay(prof_tax_monthly);
            document.getElementById('incomeTaxAnnualNew').textContent = formatCurrencyDisplay(income_tax_annual);
            document.getElementById('incomeTaxMonthlyNew').textContent = formatCurrencyDisplay(income_tax_monthly);
            document.getElementById('totalDeductionAnnualNew').textContent = formatCurrencyDisplay(total_deductions_annual);
            document.getElementById('totalDeductionMonthlyNew').textContent = formatCurrencyDisplay(total_deductions_monthly);
            document.getElementById('netTakeHomeAnnualNew').textContent = formatCurrencyDisplay(net_take_home_annual);
            document.getElementById('netTakeHomeMonthlyNew').textContent = formatCurrencyDisplay(net_take_home_monthly);
            
        } else {
            // Old Regime (Expanded structure)
            document.getElementById('basicAnnualOld').textContent = formatCurrencyDisplay(basic_annual);
            document.getElementById('basicMonthlyOld').textContent = formatCurrencyDisplay(basic_monthly);
            document.getElementById('hraAnnualOld').textContent = formatCurrencyDisplay(hra_annual);
            document.getElementById('hraMonthlyOld').textContent = formatCurrencyDisplay(hra_monthly);
            document.getElementById('ltaAnnualOld').textContent = formatCurrencyDisplay(lta_annual);
            document.getElementById('ltaMonthlyOld').textContent = formatCurrencyDisplay(lta_monthly);
            document.getElementById('ceaAnnualOld').textContent = formatCurrencyDisplay(cea_annual);
            document.getElementById('ceaMonthlyOld').textContent = formatCurrencyDisplay(cea_monthly);
            document.getElementById('telephoneAnnualOld').textContent = formatCurrencyDisplay(telephone_annual);
            document.getElementById('telephoneMonthlyOld').textContent = formatCurrencyDisplay(telephone_monthly);
            document.getElementById('sodexoAnnualOld').textContent = formatCurrencyDisplay(sodexo_annual);
            document.getElementById('sodexoMonthlyOld').textContent = formatCurrencyDisplay(sodexo_monthly);
            document.getElementById('carRepairAnnualOld').textContent = formatCurrencyDisplay(car_repair_annual);
            document.getElementById('carRepairMonthlyOld').textContent = formatCurrencyDisplay(car_repair_monthly);
            document.getElementById('profDevAnnualOld').textContent = formatCurrencyDisplay(prof_dev_annual);
            document.getElementById('profDevMonthlyOld').textContent = formatCurrencyDisplay(prof_dev_monthly);
            document.getElementById('booksAnnualOld').textContent = formatCurrencyDisplay(books_annual);
            document.getElementById('booksMonthlyOld').textContent = formatCurrencyDisplay(books_monthly);
            document.getElementById('specialAllowanceAnnualOld').textContent = formatCurrencyDisplay(special_allowance_annual);
            document.getElementById('specialAllowanceMonthlyOld').textContent = formatCurrencyDisplay(special_allowance_monthly);
            document.getElementById('fixedCTCAnnualOld').textContent = formatCurrencyDisplay(fixed_ctc_annual);
            document.getElementById('fixedCTCMonthlyOld').textContent = formatCurrencyDisplay(fixed_ctc_monthly);
            document.getElementById('employerPFAnnualOld').textContent = formatCurrencyDisplay(employer_pf_annual);
            document.getElementById('employerPFMonthlyOld').textContent = formatCurrencyDisplay(employer_pf_monthly);
            document.getElementById('annualCTCOld').textContent = formatCurrencyDisplay(total_ctc_annual);
            document.getElementById('monthlyCTCOld').textContent = formatCurrencyDisplay(total_ctc_monthly);
            document.getElementById('employeePFAnnualOld').textContent = formatCurrencyDisplay(employee_pf_annual);
            document.getElementById('employeePFMonthlyOld').textContent = formatCurrencyDisplay(employee_pf_monthly);
            document.getElementById('ptAnnualOld').textContent = formatCurrencyDisplay(prof_tax_annual);
            document.getElementById('ptMonthlyOld').textContent = formatCurrencyDisplay(prof_tax_monthly);
            document.getElementById('incomeTaxAnnualOld').textContent = formatCurrencyDisplay(income_tax_annual);
            document.getElementById('incomeTaxMonthlyOld').textContent = formatCurrencyDisplay(income_tax_monthly);
            document.getElementById('totalDeductionAnnualOld').textContent = formatCurrencyDisplay(total_deductions_annual);
            document.getElementById('totalDeductionMonthlyOld').textContent = formatCurrencyDisplay(total_deductions_monthly);
            document.getElementById('netTakeHomeAnnualOld').textContent = formatCurrencyDisplay(net_take_home_annual);
            document.getElementById('netTakeHomeMonthlyOld').textContent = formatCurrencyDisplay(net_take_home_monthly);
        }

        renderTable(tax_regime);
    }
    
    function renderTable(regime) {
        const tableNew = document.getElementById('ctc-table-new');
        const tableOld = document.getElementById('ctc-table-old');
        const infoBox = document.getElementById('oldRegimeAllowances');

        if (regime === 'new') {
            tableNew.style.display = 'table';
            tableOld.style.display = 'none';
            infoBox.classList.add('hidden'); // Hide info box for new regime
        } else {
            tableNew.style.display = 'none';
            tableOld.style.display = 'table';
            infoBox.classList.remove('hidden'); // Show info box for old regime
        }
    }

    function toggleOldRegimeAllowances() {
        // This function is now redundant for visibility control, but keeps input event handler clean.
        // Visibility is now fully controlled by renderTable(regime) inside calculateCTC() and initialization.
    }

    // --- PDF Download Functionality (Captures the visible table) ---
    async function downloadPDF() {
        // Determine which table is currently visible and set it as the input element
        const isNewRegime = document.getElementById('taxRegime').value === 'new';
        const visibleTableId = isNewRegime ? 'ctc-table-new' : 'ctc-table-old';
        
        // Capture the parent container, which is what html2canvas expects for sizing
        const input = document.getElementById('results-container'); 
        const { jsPDF } = window.jspdf;
        
        if (!input) {
            console.error("PDF Error: 'results-container' element not found.");
            const messageBox = document.createElement('div');
            messageBox.style.cssText = 'position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); background: white; padding: 20px; border: 2px solid red; border-radius: 10px; z-index: 1000; box-shadow: 0 4px 8px rgba(0,0,0,0.2);';
            messageBox.innerHTML = '<strong>Error!</strong> Could not find the table to generate the PDF. Please try refreshing the page.';
            document.body.appendChild(messageBox);
            setTimeout(() => document.body.removeChild(messageBox), 4000);
            return;
        }

        calculateCTC(); 

        // Important: html2canvas captures the WHOLE div, which works best here.
        html2canvas(input, { scale: 2 }).then(canvas => {
            const imgData = canvas.toDataURL('image/png');
            const pdf = new jsPDF('p', 'mm', 'a4');
            
            const pdfWidth = pdf.internal.pageSize.getWidth();
            const pdfHeight = pdf.internal.pageSize.getHeight();
            const imgHeight = (canvas.height * pdfWidth) / canvas.width;

            // Add title text
            pdf.setFontSize(16);
            pdf.text('India CTC Breakdown & Net Take Home Estimate', pdfWidth / 2, 15, { align: 'center' });
            pdf.setFontSize(10);
            pdf.text('Generated on: ' + new Date().toLocaleDateString(), pdfWidth / 2, 22, { align: 'center' });

            // Add image of the table
            pdf.addImage(imgData, 'PNG', 10, 30, pdfWidth - 20, imgHeight * (pdfWidth - 20) / pdfWidth);
            
            // Add disclaimer
            pdf.setFontSize(8);
            pdf.text('Disclaimer: This tool provides an **estimation** for illustrative purposes only. Actual net take-home salary may vary based on company policies, investment declarations, and final tax calculations.', 10, pdfHeight - 10);
            
            pdf.save(`CTC_Breakdown_Report_${isNewRegime ? 'New' : 'Old'}_Regime.pdf`);
        }).catch(error => {
            console.error("Error generating PDF:", error);
            const messageBox = document.createElement('div');
            messageBox.style.cssText = 'position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); background: white; padding: 20px; border: 2px solid red; border-radius: 10px; z-index: 1000; box-shadow: 0 4px 8px rgba(0,0,0,0.2);';
            messageBox.innerHTML = '<strong>Error!</strong> Could not generate PDF. Please try again or check the console for details.';
            document.body.appendChild(messageBox);
            setTimeout(() => document.body.removeChild(messageBox), 3000);
        });
    }

    // Initialize on load
    window.onload = function() {
        clearResults(); 
        calculateCTC(); 
        // Initial render based on default dropdown value
        renderTable(document.getElementById('taxRegime').value);
    };

</script>

</body>
</html>