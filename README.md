<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nysa Subscription Bill</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #FFD700;
            --secondary-color: #FDB931;
            --background-dark: #1a1a1f;
            --background-light: #25252e;
            --text-light: #ffffff;
            --text-dark: #000000;
            --text-muted: #b8c2cc;
            --accent-gradient: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            --error-color: #ff4444;
            --success-color: #00C851;
            --silver-color: #C0C0C0;
            --gold-color: #FFD700;
            --diamond-color: #b9f2ff;
            --border-radius: 12px;
            --box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            --card-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.2), 0 10px 10px -5px rgba(0, 0, 0, 0.1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: var(--background-dark);
            color: var(--text-light);
            line-height: 1.6;
            min-height: 100vh;
        }

        .header {
            padding: 30px 20px;
            text-align: center;
            background: linear-gradient(135deg, var(--background-dark), var(--background-light));
            position: relative;
            overflow: hidden;
            z-index: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiPjxkZWZzPjxwYXR0ZXJuIGlkPSJwYXR0ZXJuIiB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHBhdHRlcm5Vbml0cz0idXNlclNwYWNlT25Vc2UiIHBhdHRlcm5UcmFuc2Zvcm09InJvdGF0ZSg0NSkiPjxyZWN0IHdpZHRoPSIyMCIgaGVpZ2h0PSIyMCIgZmlsbD0icmdiYSgyNTUsMjU1LDI1NSwwLjAzKSIvPjwvcGF0dGVybj48L2RlZnM+PHJlY3Qgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgZmlsbD0idXJsKCNwYXR0ZXJuKSIvPjwvc3ZnPg==');
            z-index: -1;
        }

        /* Massive Logo Size Adjustments */
        .logo-img {
            height: 180px; /* Very large size for desktop */
            margin-bottom: 10px;
            transition: var(--transition);
            object-fit: contain;
            width: auto; /* Maintain aspect ratio */
            max-width: 100%; /* Prevent overflow */
        }

        /* For large desktop screens */
        @media (max-width: 1600px) {
            .logo-img {
                height: 160px;
            }
        }

        @media (max-width: 1200px) {
            .logo-img {
                height: 140px;
            }
        }

        @media (max-width: 992px) {
            .logo-img {
                height: 120px;
            }
        }

        @media (max-width: 768px) {
            .logo-img {
                height: 100px;
                margin-bottom: 1.5rem;
            }
        }

        @media (max-width: 576px) {
            .logo-img {
                height: 90px;
                margin-bottom: 1.2rem;
            }
        }

        /* For massive screens (4K and beyond) */
        @media (min-width: 2000px) {
            .logo-img {
                height: 220px;
            }
        }

        /* Adjust header padding for the larger logo */
        .header {
            padding: 40px 20px 30px;
        }

        @media (max-width: 768px) {
            .header {
                padding: 30px 15px 20px;
            }
        }

        .subtitle {
            margin-top: 0.5rem;
            color: var(--text-muted);
            font-weight: 400;
            font-size: 1.1rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7;
            padding: 0 20px;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem 1.5rem;
        }

        /* Selection Process */
        .selection-process {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .selection-step {
            background: rgba(255, 255, 255, 0.03);
            border-radius: var(--border-radius);
            padding: 1.5rem;
            box-shadow: var(--box-shadow);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .step-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .step-title i {
            font-size: 1.4rem;
        }

        .selection-options {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            justify-content: center;
        }

        .option-btn {
            padding: 0.8rem 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: 50px;
            color: var(--text-light);
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .option-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background: var(--accent-gradient);
            transition: var(--transition);
            z-index: -1;
        }

        .option-btn:hover, .option-btn.active {
            color: var(--text-dark);
            border-color: transparent;
            transform: translateY(-2px);
        }

        .option-btn.active::before, .option-btn:hover::before {
            width: 100%;
        }

        /* Bill Summary */
        .bill-summary {
            background: rgba(255, 255, 255, 0.03);
            border-radius: var(--border-radius);
            padding: 2rem;
            margin-top: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: var(--box-shadow);
        }

        .bill-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .bill-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--primary-color);
        }

        .bill-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .bill-item {
            background: rgba(255, 255, 255, 0.02);
            padding: 1.2rem;
            border-radius: var(--border-radius);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .bill-item-title {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin-bottom: 0.5rem;
        }

        .bill-item-value {
            font-size: 1.1rem;
            font-weight: 500;
        }

        .bill-features {
            margin-top: 2rem;
        }

        .feature-list {
            list-style: none;
        }

        .feature-list li {
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
            font-size: 0.95rem;
        }

        .feature-list li:last-child {
            border-bottom: none;
        }

        .feature-list li i {
            margin-right: 0.8rem;
            font-size: 1.1rem;
            min-width: 20px;
        }

        .silver .feature-list li i {
            color: var(--silver-color);
        }

        .gold .feature-list li i {
            color: var(--gold-color);
        }

        .diamond .feature-list li i {
            color: var(--diamond-color);
        }

        /* Customer Information */
        .customer-info {
            margin-top: 3rem;
            background: rgba(255, 255, 255, 0.03);
            border-radius: var(--border-radius);
            padding: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: var(--box-shadow);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--text-muted);
        }

        .form-input {
            width: 100%;
            padding: 0.8rem 1rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: var(--border-radius);
            color: var(--text-light);
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-input:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 2px rgba(255, 215, 0, 0.2);
        }

        /* Payment Method Selector */
        .payment-methods {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-bottom: 1.5rem;
        }

        .payment-method {
            display: flex;
            align-items: center;
            padding: 0.8rem 1.2rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: var(--border-radius);
            cursor: pointer;
            transition: var(--transition);
        }

        .payment-method i {
            margin-right: 0.5rem;
            font-size: 1.2rem;
        }

        .payment-method.active {
            background: rgba(255, 215, 0, 0.2);
            border-color: var(--primary-color);
        }

        /* Action Buttons */
        .action-buttons {
            display: flex;
            justify-content: flex-end;
            gap: 1rem;
            margin-top: 2rem;
        }

        .btn {
            padding: 1rem 2rem;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--accent-gradient);
            color: var(--text-dark);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: var(--text-light);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-3px);
        }

        /* Tooltip */
        .tooltip {
            position: relative;
            display: inline-block;
            margin-left: 0.5rem;
            cursor: pointer;
        }

        .tooltip i {
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        .tooltip .tooltip-text {
            visibility: hidden;
            width: 200px;
            background-color: rgba(0, 0, 0, 0.8);
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 0.8rem;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            transform: translateX(-50%);
            opacity: 0;
            transition: opacity 0.3s;
            font-size: 0.85rem;
            font-weight: 400;
        }

        .tooltip .tooltip-text::after {
            content: "";
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: rgba(0, 0, 0, 0.8) transparent transparent transparent;
        }

        .tooltip:hover .tooltip-text {
            visibility: visible;
            opacity: 1;
        }

        /* Confirmation Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: var(--background-light);
            border-radius: var(--border-radius);
            width: 90%;
            max-width: 500px;
            padding: 2rem;
            box-shadow: var(--card-shadow);
            position: relative;
            animation: fadeIn 0.3s ease-out;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .modal-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--primary-color);
        }

        .close-modal {
            background: none;
            border: none;
            color: var(--text-muted);
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .close-modal:hover {
            color: var(--text-light);
        }

        .modal-body {
            margin-bottom: 2rem;
        }

        .modal-footer {
            display: flex;
            justify-content: flex-end;
            gap: 1rem;
        }

        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            animation: fadeIn 0.6s ease-out forwards;
        }

        .delay-1 {
            animation-delay: 0.2s;
        }

        .delay-2 {
            animation-delay: 0.4s;
        }

        .delay-3 {
            animation-delay: 0.6s;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header {
                padding: 2rem 1rem;
            }
            
            .logo-img {
                height: 90px;
            }
            
            .subtitle {
                font-size: 1.05rem;
                padding: 0 10px;
            }
            
            .selection-options {
                justify-content: center;
            }
            
            .option-btn {
                padding: 0.7rem 1.2rem;
                font-size: 0.9rem;
            }
            
            .bill-details {
                grid-template-columns: 1fr;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
        }

        @media (max-width: 576px) {
            .logo-img {
                height: 80px;
                margin-bottom: 1rem;
            }
            
            .subtitle {
                font-size: 0.95rem;
                line-height: 1.6;
            }
            
            .selection-step {
                padding: 1.2rem;
            }
            
            .option-btn {
                padding: 0.6rem 1rem;
                font-size: 0.85rem;
            }
        }

        body > h1:first-of-type:not(.heading) { 
        display: none !important; 
        }

       .markdown-body h1:first-child { 
       display: none !important; 
        }

      .position-relative h1:first-child { 
       display: none !important; 
        }

    </style>
</head>
<body>
    <header class="header">
        <div class="header-content">
            <img src="https://i.ibb.co/20MHWR6V/Nysa-New-Logo-removebg-preview-1.png" alt="Nysa Logo" class="logo-img">
            <div class="subtitle">Generate subscription bills and send confirmation emails to your customers. Select the business category and type, choose a subscription plan, and complete the billing process.</div>
        </div>
    </header>

    <div class="container">
        <!-- Selection Process -->
        <div class="selection-process">
            <div class="selection-step">
                <h3 class="step-title"><i class="fas fa-layer-group"></i> 1. Select Your Business Category</h3>
                <div class="selection-options" id="categorySelector">
                    <!-- Categories will be populated by JavaScript -->
                </div>
            </div>
            
            <div class="selection-step">
                <h3 class="step-title"><i class="fas fa-store"></i> 2. Select Your Business Type</h3>
                <div class="selection-options" id="subcategorySelector">
                    <!-- Subcategories will be populated by JavaScript -->
                </div>
            </div>
            
            <div class="selection-step">
                <h3 class="step-title"><i class="fas fa-chart-line"></i> 3. Select Your Business Size</h3>
                <div class="selection-options" id="sizeSelector">
                    <button class="option-btn" data-size="small">Small Business</button>
                    <button class="option-btn active" data-size="medium">Medium Business</button>
                    <button class="option-btn" data-size="large">Large Business</button>
                    <button class="option-btn" data-size="enterprise">Enterprise</button>
                </div>
            </div>
            
            <div class="selection-step">
                <h3 class="step-title"><i class="fas fa-calendar-alt"></i> 4. Select Subscription Duration</h3>
                <div class="selection-options" id="durationSelector">
                    <button class="option-btn" data-months="1">1 Month</button>
                    <button class="option-btn active" data-months="3">3 Months (Save 10%)</button>
                    <button class="option-btn" data-months="6">6 Months (Save 20%)</button>
                    <button class="option-btn" data-months="12">12 Months (Save 30%)</button>
                </div>
            </div>
            
            <div class="selection-step">
                <h3 class="step-title"><i class="fas fa-gem"></i> 5. Select Subscription Plan</h3>
                <div class="selection-options" id="planSelector">
                    <button class="option-btn" data-plan="silver">Silver</button>
                    <button class="option-btn active" data-plan="gold">Gold</button>
                    <button class="option-btn" data-plan="diamond">Diamond</button>
                </div>
            </div>
        </div>

        <!-- Bill Summary -->
        <div class="bill-summary fade-in">
            <div class="bill-header">
                <h2 class="bill-title">Subscription Bill Summary</h2>
                <div class="bill-price" id="billTotal">₹0</div>
            </div>
            
            <div class="bill-details">
                <div class="bill-item">
                    <div class="bill-item-title">Business Category</div>
                    <div class="bill-item-value" id="billCategory">-</div>
                </div>
                
                <div class="bill-item">
                    <div class="bill-item-title">Business Type</div>
                    <div class="bill-item-value" id="billSubcategory">-</div>
                </div>
                
                <div class="bill-item">
                    <div class="bill-item-title">Business Size</div>
                    <div class="bill-item-value" id="billSize">-</div>
                </div>
                
                <div class="bill-item">
                    <div class="bill-item-title">Subscription Plan</div>
                    <div class="bill-item-value" id="billPlan">-</div>
                </div>
                
                <div class="bill-item">
                    <div class="bill-item-title">Duration</div>
                    <div class="bill-item-value" id="billDuration">-</div>
                </div>
                
                <div class="bill-item">
                    <div class="bill-item-title">Subscription Price</div>
                    <div class="bill-item-value" id="billPrice">₹0</div>
                </div>
            </div>
            
            <div class="bill-features">
                <h3 class="step-title"><i class="fas fa-list-check"></i> Included Features</h3>
                <ul class="feature-list" id="billFeatures">
                    <li>Select a subscription plan to view features</li>
                </ul>
            </div>
        </div>

        <!-- Customer Information -->
        <div class="customer-info fade-in delay-1">
            <h2 class="step-title"><i class="fas fa-user"></i> Customer Information</h2>
            
            <div class="form-group">
                <label for="customerName" class="form-label">Full Name <span class="required">*</span></label>
                <input type="text" id="customerName" class="form-input" placeholder="Enter customer's full name" required>
            </div>
            
            <div class="form-group">
                <label for="customerEmail" class="form-label">Email Address <span class="required">*</span></label>
                <input type="email" id="customerEmail" class="form-input" placeholder="Enter customer's email address" required>
            </div>
            
            <div class="form-group">
                <label for="customerPhone" class="form-label">Phone Number <span class="required">*</span></label>
                <input type="tel" id="customerPhone" class="form-input" placeholder="Enter customer's phone number" required>
            </div>
            
            <div class="form-group">
                <label for="businessName" class="form-label">Business Name <span class="required">*</span></label>
                <input type="text" id="businessName" class="form-input" placeholder="Enter business name" required>
            </div>
            
            <div class="form-group">
                <label for="businessAddress" class="form-label">Business Address</label>
                <textarea id="businessAddress" class="form-input" rows="3" placeholder="Enter business address"></textarea>
            </div>
            
            <!-- Payment Method Selection -->
            <div class="form-group">
                <label class="form-label">Payment Method <span class="required">*</span></label>
                <div class="payment-methods" id="paymentMethods">
                    <div class="payment-method active" data-method="online">
                        <i class="fas fa-credit-card"></i>
                        <span>Online Payment</span>
                    </div>
                    <div class="payment-method" data-method="cash">
                        <i class="fas fa-money-bill-wave"></i>
                        <span>Cash</span>
                    </div>
                    <div class="payment-method" data-method="bank-transfer">
                        <i class="fas fa-university"></i>
                        <span>Bank Transfer</span>
                    </div>
                    <div class="payment-method" data-method="cheque">
                        <i class="fas fa-money-check"></i>
                        <span>Cheque</span>
                    </div>
                    <div class="payment-method" data-method="upi">
                        <i class="fas fa-mobile-alt"></i>
                        <span>UPI</span>
                    </div>
                </div>
            </div>
            
            <div class="action-buttons">
                <button class="btn btn-secondary" id="downloadBill">
                    <i class="fas fa-download"></i> Download Bill
                </button>
                <button class="btn btn-primary" id="confirmSubscription">
                    <i class="fas fa-envelope"></i> Happy Subscribe
                </button>
            </div>
        </div>
    </div>

    <!-- Confirmation Modal -->
    <div class="modal" id="confirmationModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Subscription Confirmed!</h3>
                <button class="close-modal" id="closeModal">&times;</button>
            </div>
            <div class="modal-body">
                <p>Thank you for subscribing to Nysa! A confirmation email with all the details has been sent to the customer.</p>
                <p>The subscription details have been recorded and the customer can now enjoy all the benefits of their selected plan.</p>
            </div>
            <div class="modal-footer">
                <button class="btn btn-secondary" id="closeModalBtn">Close</button>
                <button class="btn btn-primary" id="viewBill">
                    <i class="fas fa-file-invoice"></i> View Bill
                </button>
            </div>
        </div>
    </div>

    <!-- Email Sending Status Modal -->
    <div class="modal" id="emailStatusModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title" id="emailStatusTitle">Sending Email...</h3>
                <button class="close-modal" id="closeEmailModal">&times;</button>
            </div>
            <div class="modal-body">
                <div id="emailStatusMessage">
                    <div class="loader"></div>
                    <p>Please wait while we send the subscription confirmation to your email.</p>
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-secondary" id="closeEmailModalBtn" style="display: none;">Close</button>
            </div>
        </div>
    </div>

    <script>
        // Subscription Plans Data
        const subscriptionData = {
            categories: [
                { 
                    id: 'service-providers', 
                    name: 'Service Providers', 
                    icon: 'fas fa-tools',
                    subcategories: [
                        { id: 'electrician', name: 'Electrician', icon: 'fas fa-bolt' },
                        { id: 'plumber', name: 'Plumber', icon: 'fas fa-faucet' },
                        { id: 'carpenter', name: 'Carpenter', icon: 'fas fa-hammer' },
                        { id: 'painter', name: 'Painter', icon: 'fas fa-paint-roller' },
                        { id: 'pest-control', name: 'Pest Control Services', icon: 'fas fa-bug' },
                        { id: 'cleaning-services', name: 'House Cleaning Services', icon: 'fas fa-broom' },
                        { id: 'solar-services', name: 'Solar Panel Services', icon: 'fas fa-solar-panel' },
                        { id: 'masonry', name: 'Masonry Workers', icon: 'fas fa-hard-hat' },
                        { id: 'ac-repair', name: 'AC Repair Technician', icon: 'fas fa-wind' },
                        { id: 'bridal-makeup', name: 'Bridal Makeup Artist', icon: 'fas fa-makeup-brush' },
                        { id: 'mehndi-artist', name: 'Mehndi Artist', icon: 'fas fa-hand-holding-heart' },
                        { id: 'internet-provider', name: 'Internet & Wifi Providers', icon: 'fas fa-wifi' },
                        { id: 'laundry', name: 'Laundry & Dry Cleaning', icon: 'fas fa-tshirt' },
                        { id: 'catering', name: 'Catering & Tent', icon: 'fas fa-utensils' },
                        { id: 'tiffin', name: 'Tiffin Services', icon: 'fas fa-box-open' },
                        { id: 'security', name: 'Security Guard Services', icon: 'fas fa-shield-alt' },
                        { id: 'event-decorators', name: 'Event Decorators', icon: 'fas fa-gem' },
                        { id: 'dhol-players', name: 'Dhol Players', icon: 'fas fa-drum' },
                        { id: 'dj', name: 'DJ', icon: 'fas fa-music' },
                        { id: 'wedding-planners', name: 'Wedding Planners', icon: 'fas fa-ring' },
                        { id: 'live-bands', name: 'Live Bands & Performers', icon: 'fas fa-guitar' },
                        { id: 'photography', name: 'Photo & Videography', icon: 'fas fa-camera' },
                        { id: 'tattoo-studio', name: 'Tattoo & Artist Studio', icon: 'fas fa-paint-brush' },
                        { id: 'lawyers', name: 'Lawyers', icon: 'fas fa-gavel' },
                        { id: 'hair-extensions', name: 'Hair Extensions & Wig', icon: 'fas fa-cut' },
                        { id: 'ca', name: 'Chartered Accountant', icon: 'fas fa-calculator' },
                        { id: 'vehicle-maintenance', name: 'Car & Bike Maintenance', icon: 'fas fa-car' },
                        { id: 'architect', name: 'Architect & Interior Designers', icon: 'fas fa-ruler-combined' },
                        { id: 'travel-agency', name: 'Travel Agency', icon: 'fas fa-plane' },
                        { id: 'bus-operators', name: 'Bus Operators', icon: 'fas fa-bus' },
                        { id: 'packers-movers', name: 'Packers & Movers', icon: 'fas fa-truck-moving' },
                        { id: 'astrologers', name: 'Astrologers & Pandits', icon: 'fas fa-star' },
                        { id: 'music-teachers', name: 'Music Teachers', icon: 'fas fa-music' },
                        { id: 'yoga', name: 'Yoga & Fitness Centres', icon: 'fas fa-spa' },
                        { id: 'dance-classes', name: 'Dance Classes', icon: 'fas fa-child' },
                        { id: 'towing', name: 'Vehicle Towing Services', icon: 'fas fa-truck-pickup' },
                        { id: 'rentals', name: 'Rentals (bikes, cars, etc.)', icon: 'fas fa-key' },
                        { id: 'home-tutors', name: 'Home Tutors', icon: 'fas fa-book' },
                        { id: 'language-classes', name: 'Language Classes', icon: 'fas fa-language' },
                        { id: 'printing', name: 'Banner & Flex Printing', icon: 'fas fa-print' },
                        { id: 'water-supply', name: 'Water Supply', icon: 'fas fa-tint' },
                        { id: 'news-agency', name: 'News Agency', icon: 'fas fa-newspaper' },
                        { id: 'insurance', name: 'Insurance Agents', icon: 'fas fa-shield-alt' },
                        { id: 'bhajan-mandli', name: 'Bhajan Mandli', icon: 'fas fa-pray' }
                    ]
                },
                { 
                    id: 'stores', 
                    name: 'Stores', 
                    icon: 'fas fa-store',
                    subcategories: [
                        { id: 'jewelry', name: 'Jewellery Stores', icon: 'fas fa-gem' },
                        { id: 'grocery', name: 'Grocery & Supermarkets', icon: 'fas fa-shopping-basket' },
                        { id: 'fashion', name: 'Fashion Apparel Stores', icon: 'fas fa-tshirt' },
                        { id: 'electronics', name: 'Electronics Stores', icon: 'fas fa-laptop' },
                        { id: 'furniture', name: 'Furniture Stores', icon: 'fas fa-couch' },
                        { id: 'health-wellness', name: 'Health & Wellness Stores', icon: 'fas fa-heartbeat' },
                        { id: 'beauty', name: 'Beauty & Personal Care', icon: 'fas fa-spa' },
                        { id: 'automobile', name: 'Automobile & Tyre Stores', icon: 'fas fa-car' },
                        { id: 'kitchen', name: 'Kitchen Stores', icon: 'fas fa-utensils' },
                        { id: 'watch', name: 'Watch Stores', icon: 'fas fa-clock' },
                        { id: 'building-materials', name: 'Building Material Stores', icon: 'fas fa-hammer' },
                        { id: 'books', name: 'Books & Stationery', icon: 'fas fa-book' },
                        { id: 'sports', name: 'Sports Stores', icon: 'fas fa-running' },
                        { id: 'toys', name: 'Toys & Kids Stores', icon: 'fas fa-gamepad' },
                        { id: 'music-instruments', name: 'Music & Instrument Stores', icon: 'fas fa-guitar' },
                        { id: 'bakery', name: 'Bakery & Confectionery', icon: 'fas fa-birthday-cake' },
                        { id: 'restaurant', name: 'Restaurant & Café\'s', icon: 'fas fa-utensils' },
                        { id: 'gift', name: 'Gift Stores', icon: 'fas fa-gift' },
                        { id: 'eyewear', name: 'Eyewear & Optical Stores', icon: 'fas fa-glasses' },
                        { id: 'uniform', name: 'School Uniform Stores', icon: 'fas fa-user-graduate' },
                        { id: 'dairy', name: 'Dairy Stores', icon: 'fas fa-wine-bottle' },
                        { id: 'wedding-cards', name: 'Wedding Cards Stores', icon: 'fas fa-envelope-open-text' },
                        { id: 'mobile-repair', name: 'Mobile Repair Stores', icon: 'fas fa-mobile-alt' },
                        { id: 'luggage', name: 'Luggage & Bag Stores', icon: 'fas fa-suitcase' },
                        { id: 'pet', name: 'Pet & Supplies Stores', icon: 'fas fa-paw' },
                        { id: 'salon', name: 'Men\'s & Women\'s Salon', icon: 'fas fa-cut' },
                        { id: 'mattress', name: 'Mattress Stores', icon: 'fas fa-bed' },
                        { id: 'solar-dealers', name: 'Solar Panel Dealers', icon: 'fas fa-solar-panel' },
                        { id: 'electrical', name: 'Electrical Stores', icon: 'fas fa-lightbulb' },
                        { id: 'laundry-store', name: 'Laundry Stores', icon: 'fas fa-tshirt' },
                        { id: 'fire-safety', name: 'Fire Safety Equipment', icon: 'fas fa-fire-extinguisher' }
                    ]
                },
                { 
                    id: 'public-places', 
                    name: 'Public Places', 
                    icon: 'fas fa-umbrella-beach',
                    subcategories: [
                        { id: 'amusement-parks', name: 'Amusement Parks', icon: 'fas fa-ferris-wheel' },
                        { id: 'water-parks', name: 'Water Parks', icon: 'fas fa-swimming-pool' },
                        { id: 'shopping-malls', name: 'Shopping Malls', icon: 'fas fa-store-alt' },
                        { id: 'petrol-pumps', name: 'Petrol Pumps', icon: 'fas fa-gas-pump' },
                        { id: 'movie-theatres', name: 'Movie Theatres', icon: 'fas fa-film' },
                        { id: 'gyms', name: 'Fitness Centres & Gyms', icon: 'fas fa-dumbbell' },
                        { id: 'schools', name: 'Schools', icon: 'fas fa-school' },
                        { id: 'colleges', name: 'Colleges', icon: 'fas fa-university' },
                        { id: 'coaching-centres', name: 'Coaching Centres', icon: 'fas fa-chalkboard-teacher' },
                        { id: 'hospitals', name: 'Hospitals', icon: 'fas fa-hospital' },
                        { id: 'hotels', name: 'Hotels & Resorts', icon: 'fas fa-hotel' },
                        { id: 'wedding-venues', name: 'Wedding Venues', icon: 'fas fa-ring' },
                        { id: 'atms', name: 'ATMs (Private Banks)', icon: 'fas fa-money-bill-wave' },
                        { id: 'banks', name: 'Banks & Financial Institutions', icon: 'fas fa-piggy-bank' },
                        { id: 'coworking', name: 'Co-working Spaces', icon: 'fas fa-laptop-house' },
                        { id: 'gaming-zones', name: 'Gaming Zones', icon: 'fas fa-gamepad' }
                    ]
                },
                { 
                    id: 'real-estate', 
                    name: 'Real Estate', 
                    icon: 'fas fa-building',
                    subcategories: [
                        { id: 'residential', name: 'Residential Real Estate', icon: 'fas fa-home' },
                        { id: 'commercial', name: 'Commercial Real Estate', icon: 'fas fa-city' },
                        { id: 'land', name: 'Lands & Plots', icon: 'fas fa-mountain' },
                        { id: 'rental', name: 'Rental & Lease', icon: 'fas fa-key' }
                    ]
                },
                { 
                    id: 'travel', 
                    name: 'Travel', 
                    icon: 'fas fa-route',
                    subcategories: [
                        { id: 'e-rickshaw', name: 'E-Rickshaw', icon: 'fas fa-rickshaw' },
                        { id: 'three-wheeler', name: 'Three-Wheeler (Cargo)', icon: 'fas fa-shuttle-van' },
                        { id: 'mini-trucks', name: 'Mini Trucks (Tata Ace etc.)', icon: 'fas fa-truck' },
                        { id: 'vans', name: 'Vans & Goods Carriers', icon: 'fas fa-van-shuttle' },
                        { id: 'medium-trucks', name: 'Medium Trucks', icon: 'fas fa-truck-moving' },
                        { id: 'passenger-vans', name: 'Passenger Vans (Tourist/Private)', icon: 'fas fa-bus-alt' }
                    ]
                },
                { 
                    id: 'distributors', 
                    name: 'Distributors & Wholesalers', 
                    icon: 'fas fa-truck-loading',
                    subcategories: [
                        { id: 'grocery-distributor', name: 'Grocery Distributor', icon: 'fas fa-boxes' },
                        { id: 'electronics-distributor', name: 'Electronics Distributor', icon: 'fas fa-box-open' },
                        { id: 'medical-distributor', name: 'Medical Distributor', icon: 'fas fa-briefcase-medical' },
                        { id: 'construction-distributor', name: 'Construction Distributor', icon: 'fas fa-tools' },
                        { id: 'automotive-distributor', name: 'Automotive Distributor', icon: 'fas fa-car-alt' },
                        { id: 'fashion-distributor', name: 'Fashion Distributor', icon: 'fas fa-tshirt' },
                        { id: 'furniture-distributor', name: 'Furniture Distributor', icon: 'fas fa-couch' },
                        { id: 'pharma-distributor', name: 'Pharmaceutical Distributor', icon: 'fas fa-pills' },
                        { id: 'food-beverage-distributor', name: 'Food & Beverage Distributor', icon: 'fas fa-utensils' },
                        { id: 'beauty-distributor', name: 'Beauty Products Distributor', icon: 'fas fa-spa' },
                        { id: 'stationery-distributor', name: 'Stationery Distributor', icon: 'fas fa-pencil-alt' },
                        { id: 'toy-distributor', name: 'Toy Distributor', icon: 'fas fa-gamepad' },
                        { id: 'sports-distributor', name: 'Sports Goods Distributor', icon: 'fas fa-running' },
                        { id: 'kitchen-distributor', name: 'Kitchenware Distributor', icon: 'fas fa-utensil-spoon' },
                        { id: 'electrical-distributor', name: 'Electrical Goods Distributor', icon: 'fas fa-plug' },
                        { id: 'hardware-distributor', name: 'Hardware Distributor', icon: 'fas fa-tools' },
                        { id: 'agriculture-distributor', name: 'Agriculture Products Distributor', icon: 'fas fa-tractor' },
                        { id: 'pet-distributor', name: 'Pet Supplies Distributor', icon: 'fas fa-paw' },
                        { id: 'book-distributor', name: 'Book Distributor', icon: 'fas fa-book' },
                        { id: 'jewelry-distributor', name: 'Jewelry Distributor', icon: 'fas fa-gem' },
                        { id: 'building-materials-distributor', name: 'Building Materials Distributor', icon: 'fas fa-hard-hat' },
                        { id: 'solar-distributor', name: 'Solar Products Distributor', icon: 'fas fa-solar-panel' },
                        { id: 'safety-distributor', name: 'Safety Equipment Distributor', icon: 'fas fa-shield-alt' },
                        { id: 'office-distributor', name: 'Office Supplies Distributor', icon: 'fas fa-briefcase' },
                        { id: 'textile-distributor', name: 'Textile Distributor', icon: 'fas fa-tshirt' },
                        { id: 'chemical-distributor', name: 'Chemical Distributor', icon: 'fas fa-flask' },
                        { id: 'plastic-distributor', name: 'Plastic Products Distributor', icon: 'fas fa-cubes' },
                        { id: 'metal-distributor', name: 'Metal Products Distributor', icon: 'fas fa-hammer' },
                        { id: 'glass-distributor', name: 'Glass Products Distributor', icon: 'fas fa-wine-glass-alt' },
                        { id: 'paper-distributor', name: 'Paper Products Distributor', icon: 'fas fa-file-alt' }
                    ]
                }
            ],
            
            features: [
                { name: "Business Profile Listing", description: "Create and manage your business profile with all necessary details" },
                { name: "Verified Badge", description: "Get a verified badge to build trust with customers" },
                { name: "Priority Placement", description: "Your business appears higher in search results" },
                { name: "Unlimited Products/Services", description: "List all your products or services without limits" },
                { name: "Advanced Analytics", description: "Get detailed insights about your customers and performance" },
                { name: "Customer Reviews", description: "Collect and display customer reviews and ratings" },
                { name: "Promotional Offers", description: "Create and manage special offers and discounts" },
                { name: "24/7 Support", description: "Round-the-clock customer support for your business" },
                { name: "AI Assistant", description: "AI-powered assistant to help manage customer queries" },
                { name: "VR Showcase", description: "Showcase your business with virtual reality tours" },
                { name: "Lead Generation", description: "Get qualified leads directly to your business" },
                { name: "Search Priority", description: "Higher visibility in search results" },
                { name: "Custom Features", description: "Integrate with your existing systems using our API" },
                { name: "Bulk Upload", description: "Upload multiple products or services at once" },
                { name: "Multi-user Access", description: "Add team members with different access levels" },
                { name: "Advanced Security", description: "Enhanced security features for your business data" },
                { name: "Dedicated Account Manager", description: "Personal account manager to help you grow" }
            ],
            
    plans: {
    // Service Providers Plans
    'electrician': {
        small: {
            silver: { price: {1: 299, 3: 499, 6: 899, 12: 1599}, features: [0,1,2,3,4] },
            gold: { price: {1: 499, 3: 1299, 6: 2399, 12: 4199}, features: [0,1,2,3,4,5,6,7] },
            diamond: { price: {1: 999, 3: 2699, 6: 4999, 12: 8999}, features: [0,1,2,3,4,5,6,7,8,9,10] }
        },
        medium: {
            silver: { price: {1: 399, 3: 999, 6: 1799, 12: 3199}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 12999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        large: {
            silver: { price: {1: 699, 3: 1799, 6: 3299, 12: 5899}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        enterprise: {
            silver: { price: {1: 1199, 3: 3099, 6: 5699, 12: 9999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        }
    },
    'plumber': {
        small: {
            silver: { price: {1: 299, 3: 499, 6: 899, 12: 1599}, features: [0,1,2,3,4] },
            gold: { price: {1: 499, 3: 1299, 6: 2399, 12: 4199}, features: [0,1,2,3,4,5,6,7] },
            diamond: { price: {1: 999, 3: 2699, 6: 4999, 12: 8999}, features: [0,1,2,3,4,5,6,7,8,9,10] }
        },
        medium: {
            silver: { price: {1: 399, 3: 999, 6: 1799, 12: 3199}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 12999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        large: {
            silver: { price: {1: 699, 3: 1799, 6: 3299, 12: 5899}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        enterprise: {
            silver: { price: {1: 1199, 3: 3099, 6: 5699, 12: 9999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        }
    },
    'carpenter': {
        small: {
            silver: { price: {1: 299, 3: 499, 6: 899, 12: 1599}, features: [0,1,2,3,4] },
            gold: { price: {1: 499, 3: 1299, 6: 2399, 12: 4199}, features: [0,1,2,3,4,5,6,7] },
            diamond: { price: {1: 999, 3: 2699, 6: 4999, 12: 8999}, features: [0,1,2,3,4,5,6,7,8,9,10] }
        },
        medium: {
            silver: { price: {1: 399, 3: 999, 6: 1799, 12: 3199}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 12999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        large: {
            silver: { price: {1: 699, 3: 1799, 6: 3299, 12: 5899}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        enterprise: {
            silver: { price: {1: 1199, 3: 3099, 6: 5699, 12: 9999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        }
    },
    'painter': {
        small: {
            silver: { price: {1: 299, 3: 499, 6: 899, 12: 1599}, features: [0,1,2,3,4] },
            gold: { price: {1: 499, 3: 1299, 6: 2399, 12: 4199}, features: [0,1,2,3,4,5,6,7] },
            diamond: { price: {1: 999, 3: 2699, 6: 4999, 12: 8999}, features: [0,1,2,3,4,5,6,7,8,9,10] }
        },
        medium: {
            silver: { price: {1: 399, 3: 999, 6: 1799, 12: 3199}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 12999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        large: {
            silver: { price: {1: 699, 3: 1799, 6: 3299, 12: 5899}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        enterprise: {
            silver: { price: {1: 1199, 3: 3099, 6: 5699, 12: 9999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        }
    },
    'pest-control': {
        small: {
            silver: { price: {1: 399, 3: 799, 6: 1499, 12: 2699}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 599, 3: 1599, 6: 2999, 12: 5399}, features: [0,1,2,3,4,5,6,7,8] },
            diamond: { price: {1: 1199, 3: 3199, 6: 5999, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        medium: {
            silver: { price: {1: 499, 3: 1299, 6: 2399, 12: 4299}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 999, 3: 2599, 6: 4799, 12: 8599}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 1799, 3: 4699, 6: 8699, 12: 15499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        large: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1499, 3: 3899, 6: 7199, 12: 12799}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 2599, 3: 6799, 6: 12499, 12: 21999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3999, 3: 10399, 6: 18999, 12: 33499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
    // Continuing with all other service providers in the same pattern...
    'cleaning-services': {
        small: {
            silver: { price: {1: 299, 3: 799, 6: 1499, 12: 2699}, features: [0,1,2,3,4,5] },
            gold: { price: {1: 599, 3: 1599, 6: 2999, 12: 5399}, features: [0,1,2,3,4,5,6,7,8] },
            diamond: { price: {1: 1199, 3: 3199, 6: 5999, 12: 10999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
        },
        medium: {
            silver: { price: {1: 499, 3: 1299, 6: 2399, 12: 4299}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 999, 3: 2599, 6: 4799, 12: 8599}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 1799, 3: 4699, 6: 8699, 12: 15499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        large: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1499, 3: 3899, 6: 7199, 12: 12799}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] },
            diamond: { price: {1: 2599, 3: 6799, 6: 12499, 12: 21999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3999, 3: 10399, 6: 18999, 12: 33499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
    'solar-services': {
        small: {
            silver: { price: {1: 799, 3: 1499, 6: 1999, 12: 2799}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 999, 3: 1999, 6: 2999, 12: 3999}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 999, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1399, 3: 2999, 6: 4999, 12: 7999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 1999, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'masonry': {
            small: {
            silver: { price: {1: 299, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },        
        'ac-repair': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },        
        'bridal-makeup': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },        
        'mehndi-artist': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'internet-provider': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'laundry': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'catering': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'tiffin': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'security': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'event-decorators': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'dhol-players': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'dj': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'wedding-planners': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'live-bands': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'photography': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'tattoo-studio': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'lawyers': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'hair-extensions': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'ca': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'vehicle-maintenance': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 1499, 6: 2999, 12: 4999}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'architect': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'travel-agency': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'bus-operators': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'packers-movers': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'astrologers': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'music-teachers': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'yoga': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'dance-classes': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'towing': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'rentals': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'home-tutors': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'language-classes': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'printing': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'water-supply': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 699, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'news-agency': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'insurance': {
            small: {
            silver: { price: {1: 499, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1299, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        'bhajan-mandli': {
            small: {
            silver: { price: {1: 399, 3: 999, 6: 1899, 12: 3499}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 599, 3: 2099, 6: 3999, 12: 7199}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 999, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 699, 3: 1799, 6: 3399, 12: 6099}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1299, 3: 3399, 6: 6299, 12: 11199}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 2299, 3: 5999, 6: 10999, 12: 19499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        large: {
            silver: { price: {1: 1199, 3: 3099, 6: 5799, 12: 10399}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] }
        },
        enterprise: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            gold: { price: {1: 3299, 3: 8499, 6: 15499, 12: 27499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15] },
            diamond: { price: {1: 5499, 3: 13999, 6: 25499, 12: 44999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18] }
        }
    },
        
        // Stores Plans
        'jewelry': {
            small: {
            silver: { price: {1: 799, 3: 1999, 6: 2999, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1299, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1999, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'grocery': {
            small: {
            silver: { price: {1: 299, 3: 499, 6: 1999, 12: 2999}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 499, 3: 1099, 6: 1899, 12: 3999}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 799, 3: 1499, 6: 2299, 12: 4499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 799, 3: 1499, 6: 2499, 12: 3499}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 1099, 3: 1999, 6: 2999, 12: 3999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 1499, 3: 2499, 6: 3999, 12: 5999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1499, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 2299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 3499, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'fashion': {
            small: {
            silver: { price: {1: 499, 3: 1299, 6: 1999, 12: 2999}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 799, 3: 1499, 6: 2499, 12: 2999}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 1299, 3: 2499, 6: 3499, 12: 4999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'electronics': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'furniture': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'health-wellness': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'beauty': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'automobile': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'kitchen': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'watch': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'building-materials': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'books': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'sports': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'toys': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'music-instruments': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'bakery': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'restaurant': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'gift': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'eyewear': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'uniform': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'dairy': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'wedding-cards': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'mobile-repair': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'luggage': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'pet': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'salon': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'mattress': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'solar-dealers': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'electrical': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'laundry-store': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'fire-safety': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        
        // Public Places Plans
        'amusement-parks': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'water-parks': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'shopping-malls': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'petrol-pumps': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'movie-theatres': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'gyms': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'schools': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'colleges': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'coaching-centres': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'hospitals': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'hotels': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'wedding-venues': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'atms': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'banks': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'coworking': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'gaming-zones': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        
        // Real Estate Plans
        'residential': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'commercial': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'land': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'rental': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        
        // Travel Plans
        'e-rickshaw': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'three-wheeler': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'mini-trucks': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'vans': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'medium-trucks': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'passenger-vans': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        
        // Distributors & Wholesalers Plans
        'grocery-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'electronics-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'medical-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'construction-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'automotive-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'fashion-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'furniture-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'pharma-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'food-beverage-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'beauty-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'stationery-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'toy-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'sports-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'kitchen-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'electrical-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'hardware-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'agriculture-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'pet-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'book-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'jewelry-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'building-materials-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'solar-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'safety-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'office-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'textile-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'chemical-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'plastic-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'metal-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'glass-distributor': {
            small: {
            silver: { price: {1: 799, 3: 2099, 6: 3899, 12: 6899}, features: [0,1,2,3,4,5,6] },
            gold: { price: {1: 1499, 3: 3999, 6: 7499, 12: 13499}, features: [0,1,2,3,4,5,6,7,8,9] },
            diamond: { price: {1: 2499, 3: 6599, 6: 12499, 12: 22499}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12] }
        },
        medium: {
            silver: { price: {1: 1299, 3: 3399, 6: 6299, 12: 10999}, features: [0,1,2,3,4,5,6,7] },
            gold: { price: {1: 2299, 3: 5999, 6: 10999, 12: 18999}, features: [0,1,2,3,4,5,6,7,8,9,10] },
            diamond: { price: {1: 3499, 3: 8999, 6: 16499, 12: 28999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] }
        },
        large: {
            silver: { price: {1: 1999, 3: 5199, 6: 9599, 12: 16999}, features: [0,1,2,3,4,5,6,7,8] },
            gold: { price: {1: 3299, 3: 8599, 6: 15899, 12: 27999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] },
            diamond: { price: {1: 4999, 3: 12999, 6: 23999, 12: 41999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] }
        },
        enterprise: {
            silver: { price: {1: 2999, 3: 7799, 6: 14399, 12: 25199}, features: [0,1,2,3,4,5,6,7,8,9] },
            gold: { price: {1: 4499, 3: 11699, 6: 21599, 12: 37999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13] },
            diamond: { price: {1: 6999, 3: 18199, 6: 33599, 12: 58999}, features: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16] }
        }
    },
        'paper-distributor': {
            small: {
                silver: { price: {1: 899, 3: 2299, 6: 4199, 12: 7299}, features: [0,1,2,3,4,5,6] },
                gold: { price: {1: 1599, 3: 4199, 6: 7799, 12: 13599}, features: [0,1,2,3,4,5,6,7,8,9] },
                diamond: { price: {1: 2599, 3: 6699, 6: 12199, 12: 20999}, features: [0,1,2,3,4,5,6,7,8,9,10,11] }
            }
        }
    }
};

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            populateCategories();
            setupEventListeners();
            setupPaymentMethodSelection();
            updateBill('electrician', 'medium', 3, 'gold'); // Default selection
        });

        function populateCategories() {
            const categorySelector = document.getElementById('categorySelector');
            
            subscriptionData.categories.forEach((category, index) => {
                const categoryBtn = document.createElement('button');
                categoryBtn.className = `option-btn ${index === 0 ? 'active' : ''}`;
                categoryBtn.innerHTML = `<i class="${category.icon}"></i> ${category.name}`;
                categoryBtn.dataset.category = category.id;
                
                categorySelector.appendChild(categoryBtn);
            });
            
            // Populate subcategories for the first category by default
            updateSubcategories(subscriptionData.categories[0].id);
        }

        function updateSubcategories(categoryId) {
            const subcategorySelector = document.getElementById('subcategorySelector');
            subcategorySelector.innerHTML = '';
            
            const category = subscriptionData.categories.find(c => c.id === categoryId);
            if (!category) return;
            
            category.subcategories.forEach((subcategory, index) => {
                const subBtn = document.createElement('button');
                subBtn.className = `option-btn ${index === 0 ? 'active' : ''}`;
                subBtn.innerHTML = `<i class="${subcategory.icon}"></i> ${subcategory.name}`;
                subBtn.dataset.subcategory = subcategory.id;
                
                subBtn.addEventListener('click', function() {
                    document.querySelectorAll('#subcategorySelector .option-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    const subcategory = this.dataset.subcategory;
                    const size = document.querySelector('#sizeSelector .option-btn.active').dataset.size;
                    const months = document.querySelector('#durationSelector .option-btn.active').dataset.months;
                    const plan = document.querySelector('#planSelector .option-btn.active').dataset.plan;
                    updateBill(subcategory, size, months, plan);
                });
                
                subcategorySelector.appendChild(subBtn);
            });
        }

        function setupPaymentMethodSelection() {
            const paymentMethods = document.querySelectorAll('.payment-method');
            
            paymentMethods.forEach(method => {
                method.addEventListener('click', function() {
                    document.querySelectorAll('.payment-method').forEach(m => m.classList.remove('active'));
                    this.classList.add('active');
                });
            });
        }

        function setupEventListeners() {
            // Category selection
            document.querySelectorAll('#categorySelector .option-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('#categorySelector .option-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    const categoryId = this.dataset.category;
                    updateSubcategories(categoryId);
                    
                    // Select the first subcategory by default
                    const firstSubcategory = document.querySelector('#subcategorySelector .option-btn');
                    if (firstSubcategory) {
                        firstSubcategory.click();
                    }
                });
            });
            
            // Size selector
            document.querySelectorAll('#sizeSelector .option-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('#sizeSelector .option-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    const subcategory = document.querySelector('#subcategorySelector .option-btn.active')?.dataset.subcategory || 'electrician';
                    const size = this.dataset.size;
                    const months = document.querySelector('#durationSelector .option-btn.active').dataset.months;
                    const plan = document.querySelector('#planSelector .option-btn.active').dataset.plan;
                    updateBill(subcategory, size, months, plan);
                });
            });
            
            // Duration selector
            document.querySelectorAll('#durationSelector .option-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('#durationSelector .option-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    const subcategory = document.querySelector('#subcategorySelector .option-btn.active')?.dataset.subcategory || 'electrician';
                    const size = document.querySelector('#sizeSelector .option-btn.active').dataset.size;
                    const months = this.dataset.months;
                    const plan = document.querySelector('#planSelector .option-btn.active').dataset.plan;
                    updateBill(subcategory, size, months, plan);
                });
            });
            
            // Plan selector
            document.querySelectorAll('#planSelector .option-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('#planSelector .option-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    const subcategory = document.querySelector('#subcategorySelector .option-btn.active')?.dataset.subcategory || 'electrician';
                    const size = document.querySelector('#sizeSelector .option-btn.active').dataset.size;
                    const months = document.querySelector('#durationSelector .option-btn.active').dataset.months;
                    const plan = this.dataset.plan;
                    updateBill(subcategory, size, months, plan);
                });
            });
            
            // Download Bill button
            document.getElementById('downloadBill').addEventListener('click', function() {
                downloadBill();
            });
            
            // Confirm Subscription button
            document.getElementById('confirmSubscription').addEventListener('click', function() {
                confirmSubscription();
            });
            
            // Modal close buttons
            document.getElementById('closeModal').addEventListener('click', function() {
                document.getElementById('confirmationModal').style.display = 'none';
            });
            
            document.getElementById('closeModalBtn').addEventListener('click', function() {
                document.getElementById('confirmationModal').style.display = 'none';
            });
            
            document.getElementById('viewBill').addEventListener('click', function() {
                document.getElementById('confirmationModal').style.display = 'none';
                downloadBill();
            });
            
            // Email status modal close buttons
            document.getElementById('closeEmailModal').addEventListener('click', function() {
                document.getElementById('emailStatusModal').style.display = 'none';
            });
            
            document.getElementById('closeEmailModalBtn').addEventListener('click', function() {
                document.getElementById('emailStatusModal').style.display = 'none';
            });
        }

        function updateBill(subcategory, size, months, plan) {
            // Get the selected category name
            const category = subscriptionData.categories.find(c => 
                c.subcategories.some(sc => sc.id === subcategory)
            );
            
            // Get the selected subcategory name
            const subcategoryObj = category.subcategories.find(sc => sc.id === subcategory);
            
            // Update bill summary
            document.getElementById('billCategory').textContent = category.name;
            document.getElementById('billSubcategory').textContent = subcategoryObj.name;
            document.getElementById('billSize').textContent = size.charAt(0).toUpperCase() + size.slice(1);
            document.getElementById('billPlan').textContent = plan.charAt(0).toUpperCase() + plan.slice(1);
            document.getElementById('billDuration').textContent = `${months} Month${months > 1 ? 's' : ''}`;
            
            // Get price and features
            const price = subscriptionData.plans[subcategory][size][plan].price[months];
            const features = subscriptionData.plans[subcategory][size][plan].features;
            
            document.getElementById('billPrice').textContent = `₹${price.toLocaleString()}`;
            document.getElementById('billTotal').textContent = `₹${price.toLocaleString()}`;
            
            // Update features list
            const featuresList = document.getElementById('billFeatures');
            featuresList.innerHTML = '';
            
            features.forEach(featureIndex => {
                const feature = subscriptionData.features[featureIndex];
                const li = document.createElement('li');
                
                li.innerHTML = `
                    <i class="fas fa-check"></i>
                    ${feature.name}
                    ${feature.description ? `
                    <div class="tooltip">
                        <i class="fas fa-info-circle"></i>
                        <span class="tooltip-text">${feature.description}</span>
                    </div>
                    ` : ''}
                `;
                
                featuresList.appendChild(li);
            });
        }

        function generateProfessionalBillHTML(customerData, subscriptionDetails) {
            const today = new Date();
            const formattedDate = today.toLocaleDateString('en-US', { 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            });
            
            // Get payment method details
            const paymentMethod = document.querySelector('.payment-method.active').dataset.method;
            let paymentMethodText = '';
            let paymentIcon = '';
            
            switch(paymentMethod) {
                case 'online':
                    paymentMethodText = 'Online Payment';
                    paymentIcon = 'fas fa-credit-card';
                    break;
                case 'cash':
                    paymentMethodText = 'Cash';
                    paymentIcon = 'fas fa-money-bill-wave';
                    break;
                case 'bank-transfer':
                    paymentMethodText = 'Bank Transfer';
                    paymentIcon = 'fas fa-university';
                    break;
                case 'cheque':
                    paymentMethodText = 'Cheque';
                    paymentIcon = 'fas fa-money-check';
                    break;
                case 'upi':
                    paymentMethodText = 'UPI Payment';
                    paymentIcon = 'fas fa-mobile-alt';
                    break;
                default:
                    paymentMethodText = 'Online Payment';
                    paymentIcon = 'fas fa-credit-card';
            }
            
            return `
                <!DOCTYPE html>
                <html lang="en">
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>Nysa Subscription Invoice</title>
                    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .invoice-container {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            padding: 30px;
        }
        .header {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eee;
            text-align: center;
        }
        @media (min-width: 768px) {
            .header {
                flex-direction: row;
                justify-content: space-between;
                align-items: center;
                text-align: left;
            }
        }
        .logo {
            max-width: 150px;
            margin-bottom: 15px;
        }
        @media (min-width: 768px) {
            .logo {
                margin-bottom: 0;
            }
        }
        .invoice-title {
            font-size: 20px; /* Default size for mobile */
            font-weight: bold;
            color: #333;
            margin: 0;
        }
        @media (min-width: 768px) {
            .invoice-title {
                font-size: 24px; /* Larger size for desktop */
            }
        }
        .invoice-details {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        .invoice-info, .customer-info {
            width: 100%;
            margin-bottom: 20px;
        }
        @media (min-width: 768px) {
            .invoice-info, .customer-info {
                width: 48%;
                margin-bottom: 0;
            }
        }
        .section-title {
            font-size: 18px;
            font-weight: bold;
            color: #444;
            margin-bottom: 15px;
            padding-bottom: 5px;
            border-bottom: 2px solid #FFD700;
        }
        .info-item {
            margin-bottom: 8px;
            display: flex;
            flex-wrap: wrap;
        }
        .info-label {
            font-weight: bold;
            width: 120px;
            min-width: 120px;
        }
        .info-value {
            flex: 1;
            word-break: break-word;
        }
        .subscription-table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 30px;
        }
        .subscription-table th {
            background-color: #f5f5f5;
            padding: 12px;
            text-align: left;
            border-bottom: 2px solid #ddd;
        }
        .subscription-table td {
            padding: 12px;
            border-bottom: 1px solid #eee;
        }
        .total-row {
            font-weight: bold;
            background-color: #f9f9f9;
        }
        .features-list {
            margin-top: 20px;
        }
        .features-list li {
            margin-bottom: 8px;
            position: relative;
            padding-left: 25px;
        }
        .features-list li:before {
            content: "✓";
            color: #4CAF50;
            position: absolute;
            left: 0;
            font-weight: bold;
        }
        .footer {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #eee;
            text-align: center;
            color: #777;
            font-size: 14px;
        }
        .thank-you {
            font-size: 18px;
            color: #FFD700;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .highlight {
            color: #FFD700;
            font-weight: bold;
        }
        .payment-method-display {
            display: flex;
            align-items: center;
            margin-top: 5px;
        }
        .payment-method-display i {
            margin-right: 8px;
            font-size: 1.2rem;
            color: #555;
        }
                    </style>
                </head>
                <body>
                    <div class="invoice-container">
                        <div class="header">
                            <img src="https://i.ibb.co/20MHWR6V/Nysa-New-Logo-removebg-preview-1.png" alt="Nysa Logo" class="logo">
                            <div class="invoice-title">SUBSCRIPTION INVOICE</div>
                        </div>
                        
                        <div class="invoice-details">
                            <div class="invoice-info">
                                <div class="section-title">Invoice Details</div>
                                <div class="info-item">
                                    <span class="info-label">Invoice #:</span>
                                    <span class="info-value">NYSA-${Math.floor(Math.random() * 10000)}</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-label">Date Issued:</span>
                                    <span class="info-value">${formattedDate}</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-label">Payment Method:</span>
                                    <div class="info-value">
                                        <div class="payment-method-display">
                                            <i class="${paymentIcon}"></i>
                                            <span>${paymentMethodText}</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="customer-info">
                                <div class="section-title">Customer Details</div>
                                <div class="info-item">
                                    <span class="info-label">Name:</span>
                                    <span class="info-value">${customerData.name}</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-label">Business:</span>
                                    <span class="info-value">${customerData.businessName}</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-label">Email:</span>
                                    <span class="info-value" style="word-break: break-all;">${customerData.email}</span>
                                </div>
                                <div class="info-item">
                                    <span class="info-label">Phone:</span>
                                    <span class="info-value">${customerData.phone}</span>
                                </div>
                                ${customerData.address ? `
                                <div class="info-item">
                                    <span class="info-label">Address:</span>
                                    <span class="info-value">${customerData.address}</span>
                                </div>
                                ` : ''}
                            </div>
                        </div>
                        
                        <div class="section-title">Subscription Details</div>
                        <table class="subscription-table">
                            <thead>
                                <tr>
                                    <th>Description</th>
                                    <th>Details</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>Business Category</td>
                                    <td>${subscriptionDetails.category}</td>
                                </tr>
                                <tr>
                                    <td>Business Type</td>
                                    <td>${subscriptionDetails.subcategory}</td>
                                </tr>
                                <tr>
                                    <td>Business Size</td>
                                    <td>${subscriptionDetails.size}</td>
                                </tr>
                                <tr>
                                    <td>Subscription Plan</td>
                                    <td>${subscriptionDetails.plan}</td>
                                </tr>
                                <tr>
                                    <td>Duration</td>
                                    <td>${subscriptionDetails.months} Month${subscriptionDetails.months > 1 ? 's' : ''}</td>
                                </tr>
                                <tr class="total-row">
                                    <td>Total Amount</td>
                                    <td class="highlight">₹${subscriptionDetails.price.toLocaleString()}</td>
                                </tr>
                            </tbody>
                        </table>
                        
                        <div class="section-title">Included Features</div>
                        <ul class="features-list">
                            ${subscriptionDetails.features.map(feature => `
                                <li>${feature.name} ${feature.description ? `<small style="color: #777;">(${feature.description})</small>` : ''}</li>
                            `).join('')}
                        </ul>
                        
                        <div class="footer">
                            <div class="thank-you">Thank You For Your Business!</div>
                            <div>If you have any questions about this invoice, please contact</div>
                            <div>support@nysa.com | +91 9876543210</div>
                            <div style="margin-top: 15px;">© ${new Date().getFullYear()} Nysa. All rights reserved.</div>
                        </div>
                    </div>
                </body>
                </html>
            `;
        }

        function downloadBill() {
            // Get customer data
            const customerName = document.getElementById('customerName').value || 'Customer Name';
            const customerEmail = document.getElementById('customerEmail').value || 'customer@example.com';
            const customerPhone = document.getElementById('customerPhone').value || 'Not provided';
            const businessName = document.getElementById('businessName').value || 'Business Name';
            const businessAddress = document.getElementById('businessAddress').value || '';
            
            // Get subscription details
            const subcategory = document.querySelector('#subcategorySelector .option-btn.active')?.dataset.subcategory || 'electrician';
            const size = document.querySelector('#sizeSelector .option-btn.active').dataset.size;
            const months = parseInt(document.querySelector('#durationSelector .option-btn.active').dataset.months);
            const plan = document.querySelector('#planSelector .option-btn.active').dataset.plan;
            
            const price = subscriptionData.plans[subcategory][size][plan].price[months];
            const category = subscriptionData.categories.find(c => 
                c.subcategories.some(sc => sc.id === subcategory)
            );
            const subcategoryObj = category.subcategories.find(sc => sc.id === subcategory);
            
            const features = subscriptionData.plans[subcategory][size][plan].features.map(index => {
                return subscriptionData.features[index];
            });
            
            // Prepare data for bill generation
            const customerData = {
                name: customerName,
                email: customerEmail,
                phone: customerPhone,
                businessName: businessName,
                address: businessAddress
            };
            
            const subscriptionDetails = {
                category: category.name,
                subcategory: subcategoryObj.name,
                size: size.charAt(0).toUpperCase() + size.slice(1),
                plan: plan.charAt(0).toUpperCase() + plan.slice(1),
                months: months,
                price: price,
                features: features
            };
            
            // Generate professional bill HTML
            const billHTML = generateProfessionalBillHTML(customerData, subscriptionDetails);
            
            // Create a blob and download link
            const blob = new Blob([billHTML], { type: 'text/html' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `Nysa_Subscription_Invoice_${businessName.replace(/\s+/g, '_')}.html`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }

        function sendEmailWithBill(customerData, subscriptionDetails) {
            // Show sending email status modal
            const emailStatusModal = document.getElementById('emailStatusModal');
            const emailStatusTitle = document.getElementById('emailStatusTitle');
            const emailStatusMessage = document.getElementById('emailStatusMessage');
            const closeEmailModalBtn = document.getElementById('closeEmailModalBtn');
            
            emailStatusModal.style.display = 'flex';
            emailStatusTitle.textContent = 'Sending Email...';
            emailStatusMessage.innerHTML = `
                <div class="loader"></div>
                <p>Please wait while we send the subscription confirmation to ${customerData.email}.</p>
            `;
            closeEmailModalBtn.style.display = 'none';
            
            // In a real application, you would send this data to your backend
            // which would then send the email with the bill attachment
            
            // Simulate email sending with a timeout
            setTimeout(() => {
                // Generate professional bill HTML
                const billHTML = generateProfessionalBillHTML(customerData, subscriptionDetails);
                
                // In a real implementation, you would:
                // 1. Send the billHTML and customer data to your backend
                // 2. Backend would generate a PDF or HTML email with the bill
                // 3. Backend would send the email to the customer
                
                // For demo purposes, we'll just show a success message
                emailStatusTitle.textContent = 'Email Sent Successfully!';
                emailStatusMessage.innerHTML = `
                    <div style="text-align: center;">
                        <i class="fas fa-check-circle" style="font-size: 48px; color: var(--success-color); margin-bottom: 15px;"></i>
                        <p>The subscription confirmation and invoice has been sent to <strong>${customerData.email}</strong>.</p>
                        <p>The customer should receive it shortly.</p>
                    </div>
                `;
                closeEmailModalBtn.style.display = 'block';
                
                // Log the email content for demo purposes
                console.log('Email would be sent to:', customerData.email);
                console.log('Email subject:', `Your Nysa Subscription Invoice for ${customerData.businessName}`);
                console.log('Email body:', `Dear ${customerData.name},\n\nThank you for subscribing to Nysa! Please find attached your subscription invoice.\n\nBest regards,\nThe Nysa Team`);
                console.log('Bill HTML:', billHTML);
                
            }, 3000);
        }

        function confirmSubscription() {
            // Validate form
            const customerName = document.getElementById('customerName').value;
            const customerEmail = document.getElementById('customerEmail').value;
            const customerPhone = document.getElementById('customerPhone').value;
            const businessName = document.getElementById('businessName').value;
            
            if (!customerName || !customerEmail || !customerPhone || !businessName) {
                alert('Please fill in all required customer information.');
                return;
            }
            
            // Validate email format
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(customerEmail)) {
                alert('Please enter a valid email address.');
                return;
            }
            
            // Get subscription details
            const subcategory = document.querySelector('#subcategorySelector .option-btn.active')?.dataset.subcategory || 'electrician';
            const size = document.querySelector('#sizeSelector .option-btn.active').dataset.size;
            const months = parseInt(document.querySelector('#durationSelector .option-btn.active').dataset.months);
            const plan = document.querySelector('#planSelector .option-btn.active').dataset.plan;
            
            const price = subscriptionData.plans[subcategory][size][plan].price[months];
            const category = subscriptionData.categories.find(c => 
                c.subcategories.some(sc => sc.id === subcategory)
            );
            const subcategoryObj = category.subcategories.find(sc => sc.id === subcategory);
            
            const features = subscriptionData.plans[subcategory][size][plan].features.map(index => {
                return subscriptionData.features[index];
            });
            
            // Prepare data for email sending
            const customerData = {
                name: customerName,
                email: customerEmail,
                phone: customerPhone,
                businessName: businessName,
                address: document.getElementById('businessAddress').value
            };
            
            const subscriptionDetails = {
                category: category.name,
                subcategory: subcategoryObj.name,
                size: size.charAt(0).toUpperCase() + size.slice(1),
                plan: plan.charAt(0).toUpperCase() + plan.slice(1),
                months: months,
                price: price,
                features: features
            };
            
            // First send the email with the bill
            sendEmailWithBill(customerData, subscriptionDetails);
            
            // Then show the confirmation modal
            document.getElementById('confirmationModal').style.display = 'flex';
            
            // In a real implementation, you would:
            // 1. Send the subscription data to your backend
            // 2. Backend would process payment and send confirmation email with bill
            // 3. Show success message to user
        }
    </script>
</body>
</html>
