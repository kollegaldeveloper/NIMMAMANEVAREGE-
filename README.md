<div class="logo-container">
    <div class="bike-animation">🛵💨</div>
    
    <h1 class="kannada-logo">ನಿಮ್ಮ ಮನೆವರೆಗೆ</h1>
    
    <p class="english-sub">NIMMAMANEVAREGE</p>
</div>

<style>
    .logo-container {
        text-align: center;
        background-color: #000; /* Black Background */
        padding: 40px;
    }

    .kannada-logo {
        color: #d4af37; /* Gold Font */
        font-size: 3rem;
        font-weight: bold;
        margin: 10px 0;
        text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
    }

    .english-sub {
        color: #d4af37;
        letter-spacing: 5px;
        font-size: 0.9rem;
        opacity: 0.8;
    }

    /* Animation for the delivery icon */
    .bike-animation {
        font-size: 2.5rem;
        animation: drive 3s infinite linear;
        display: inline-block;
    }

    @keyframes drive {
        0% { transform: translateX(-100px); opacity: 0; }
        50% { transform: translateX(0px); opacity: 1; }
        100% { transform: translateX(100px); opacity: 0; }
    }
</style>
<!DOCTYPE html>
<html lang="kn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ನಿಮ್ಮ ಮನೆವರೆಗೆ | Namma Kollegala</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        body { font-family: 'Poppins', sans-serif; background-color: #f8fafc; }
        .gradient-brand { background: linear-gradient(135deg, #f59e0b 0%, #ef4444 100%); }
        .card-shadow { box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1); }
    </style>
</head>
<body class="pb-10">

    <header class="gradient-brand text-white py-8 px-6 text-center rounded-b-[40px] shadow-lg">
        <h1 class="text-4xl font-bold mb-2">ನಿಮ್ಮ ಮನೆವರೆಗೆ</h1>
        <p class="italic opacity-90">"ಕೊಲೆಗಾಲದ ರುಚಿ, ನಿಮ್ಮ ಬಾಗಿಲಿಗೆ - Fast, Fresh, & Friendly"</p>
    </header>

    <main class="max-w-md mx-auto px-4 mt-8">
        
        <div class="flex gap-4 mb-8">
            <button onclick="showSection('pickdrop')" id="btn-pd" class="flex-1 py-3 rounded-2xl bg-orange-500 text-white font-bold shadow-md transition-all">
                <i class="fas fa-motorcycle mr-2"></i> Pick & Drop
            </button>
            <button onclick="showSection('food')" id="btn-food" class="flex-1 py-3 rounded-2xl bg-white text-gray-600 font-bold shadow-md transition-all">
                <i class="fas fa-utensils mr-2"></i> Home Food
            </button>
        </div>

        <section id="pickdrop-section" class="space-y-4">
            <div class="bg-white p-6 rounded-3xl card-shadow border border-orange-100">
                <h2 class="text-xl font-bold text-gray-800 mb-4 border-b pb-2">📦 Pick & Drop Service</h2>
                
                <div class="space-y-4">
                    <button onclick="getLocation('pd-loc')" class="w-full bg-blue-50 text-blue-600 py-2 rounded-lg text-sm font-medium border border-blue-100">
                        <i class="fas fa-location-arrow mr-2"></i> Auto-Capture My Location
                    </button>
                    <input id="pd-loc" type="text" placeholder="Current Location" class="w-full p-3 rounded-xl border border-gray-200 focus:ring-2 focus:ring-orange-400 outline-none">
                    <input id="pd-dest" type="text" placeholder="Destination Address" class="w-full p-3 rounded-xl border border-gray-200 focus:ring-2 focus:ring-orange-400 outline-none">
                    
                    <div class="bg-orange-50 p-3 rounded-xl">
                        <p class="text-xs text-orange-700 font-bold uppercase">Estimated Price</p>
                        <p id="pd-price" class="text-2xl font-bold text-orange-600">₹ 0.00</p>
                    </div>

                    <input id="pd-name" type="text" placeholder="Your Name" class="w-full p-3 rounded-xl border border-gray-200 outline-none">
                    <input id="pd-phone" type="tel" placeholder="Mobile Number" class="w-full p-3 rounded-xl border border-gray-200 outline-none">
                    <textarea id="pd-notes" placeholder="Special Instructions (Optional)" class="w-full p-3 rounded-xl border border-gray-200 outline-none h-20"></textarea>

                    <button onclick="sendWhatsApp('pd')" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-4 rounded-2xl transition-all shadow-lg flex justify-center items-center gap-2">
                        <i class="fab fa-whatsapp text-xl"></i> Order via WhatsApp
                    </button>
                </div>
            </div>
        </section>

        <section id="food-section" class="hidden space-y-4 text-center">
            <h2 class="text-2xl font-black text-gray-800">NAMMA KOLLEGALA</h2>
            <p class="text-gray-500 -mt-2 mb-4">Healthy home-cooked meals delivered</p>
            
            <div class="bg-white p-6 rounded-3xl card-shadow border border-red-100 text-left">
                <div class="space-y-4">
                    <input id="f-name" type="text" placeholder="Your Name" class="w-full p-3 rounded-xl border border-gray-200 outline-none">
                    <input id="f-phone" type="tel" placeholder="Mobile Number" class="w-full p-3 rounded-xl border border-gray-200 outline-none">
                    <textarea id="f-items" placeholder="Items you want to order..." class="w-full p-3 rounded-xl border border-gray-200 outline-none h-24"></textarea>
                    
                    <button onclick="getLocation('f-loc')" class="w-full bg-blue-50 text-blue-600 py-2 rounded-lg text-sm font-medium border border-blue-100">
                        <i class="fas fa-location-dot mr-2"></i> Capture Delivery Location
                    </button>
                    <input id="f-loc" type="text" placeholder="Location Details" class="w-full p-3 rounded-xl border border-gray-200 outline-none">

                    <div class="bg-red-50 p-3 rounded-xl">
                        <p class="text-xs text-red-700 font-bold uppercase">Delivery Fee (from Choudeshwari Rd)</p>
                        <p id="f-price" class="text-2xl font-bold text-red-600">₹ 0.00</p>
                    </div>

                    <button onclick="sendWhatsApp('food')" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-4 rounded-2xl transition-all shadow-lg flex justify-center items-center gap-2">
                        <i class="fab fa-whatsapp text-xl"></i> Order Now
                    </button>
                </div>
            </div>
        </section>

        <div id="payment-box" class="mt-8 hidden bg-slate-900 text-white p-6 rounded-3xl text-center">
            <h3 class="font-bold mb-4">Complete Your Payment</h3>
            <a id="upi-link" href="upi://pay?pa=9448167849@ptyes&pn=NimmaManevarege&cu=INR" class="inline-block bg-white text-slate-900 px-8 py-3 rounded-full font-bold">
                Pay via UPI <i class="fas fa-arrow-right ml-2"></i>
            </a>
        </div>

    </main>

    <script>
        const HUB_LAT = 12.1585; // Approx for Choudeshwari Kalyanmantapa, Kollegala
        const HUB_LON = 77.1115;

        function showSection(type) {
            const pdSec = document.getElementById('pickdrop-section');
            const fSec = document.getElementById('food-section');
            const btnPd = document.getElementById('btn-pd');
            const btnFood = document.getElementById('btn-food');

            if(type === 'pickdrop') {
                pdSec.classList.remove('hidden');
                fSec.classList.add('hidden');
                btnPd.className = "flex-1 py-3 rounded-2xl bg-orange-500 text-white font-bold shadow-md";
                btnFood.className = "flex-1 py-3 rounded-2xl bg-white text-gray-600 font-bold shadow-md";
            } else {
                fSec.classList.remove('hidden');
                pdSec.classList.add('hidden');
                btnFood.className = "flex-1 py-3 rounded-2xl bg-orange-500 text-white font-bold shadow-md";
                btnPd.className = "flex-1 py-3 rounded-2xl bg-white text-gray-600 font-bold shadow-md";
            }
        }

        function getLocation(inputId) {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition((pos) => {
                    const lat = pos.coords.latitude;
                    const lon = pos.coords.longitude;
                    document.getElementById(inputId).value = `${lat.toFixed(4)}, ${lon.toFixed(4)}`;
                    calculatePrice(lat, lon, inputId === 'pd-loc' ? 'pd-price' : 'f-price');
                });
            } else {
                alert("Geolocation is not supported by this browser.");
            }
        }

        function calculatePrice(lat, lon, priceDisplayId) {
            // Simplified distance math
            const dist = Math.sqrt(Math.pow(lat - HUB_LAT, 2) + Math.pow(lon - HUB_LON, 2)) * 111;
            let price = 30;
            if (dist > 2) price = 40;
            if (dist > 3) price = 50;
            if (dist > 4) price = 60;
            if (dist > 5) price = 75; // Extra buffer
            
            document.getElementById(priceDisplayId).innerText = `₹ ${price}`;
            window.lastPrice = price;
        }

        function sendWhatsApp(type) {
            let message = "";
            const phone = "9448167849";
            
            if(type === 'pd') {
                message = `*New Pick & Drop Order*%0A` +
                          `Name: ${document.getElementById('pd-name').value}%0A` +
                          `Phone: ${document.getElementById('pd-phone').value}%0A` +
                          `From: ${document.getElementById('pd-loc').value}%0A` +
                          `To: ${document.getElementById('pd-dest').value}%0A` +
                          `Price: ${document.getElementById('pd-price').innerText}%0A` +
                          `Notes: ${document.getElementById('pd-notes').value}`;
            } else {
                message = `*New Food Order*%0A` +
                          `Name: ${document.getElementById('f-name').value}%0A` +
                          `Items: ${document.getElementById('f-items').value}%0A` +
                          `Location: ${document.getElementById('f-loc').value}%0A` +
                          `Total: ${document.getElementById('f-price').innerText}`;
            }

            document.getElementById('payment-box').classList.remove('hidden');
            const upiUrl = `upi://pay?pa=9448167849@ptyes&pn=NimmaManevarege&am=${window.lastPrice || ''}&cu=INR`;
            document.getElementById('upi-link').href = upiUrl;

            window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
        }
    </script>
</body>
</html>
<div class="location-container" style="max-width: 400px; font-family: sans-serif;">
    <label style="display: block; margin-bottom: 8px; font-weight: bold;">Current Location</label>
    
    <div style="position: relative; display: flex; gap: 5px;">
        <input type="text" id="location-bar" placeholder="Fetching location..." 
               style="width: 100%; padding: 12px; border: 2px solid #ddd; border-radius: 8px; outline: none;">
        
        <button onclick="getCurrentLocation()" 
                style="background: #ff5722; color: white; border: none; padding: 10px 15px; border-radius: 8px; cursor: pointer;">
            <span id="btn-text">📍</span>
        </button>
    </div>
    
    <p id="status" style="font-size: 12px; color: #666; margin-top: 5px;"></p>
</div>

<script>
function getCurrentLocation() {
    const locationInput = document.getElementById('location-bar');
    const status = document.getElementById('status');
    const btnText = document.getElementById('btn-text');

    if (!navigator.geolocation) {
        status.textContent = "Geolocation is not supported by your browser";
        return;
    }

    status.textContent = "Locating...";
    btnText.textContent = "⏳"; // Loading state

    navigator.geolocation.getCurrentPosition(
        // Success Callback
        (position) => {
            const lat = position.coords.latitude;
            const lng = position.coords.longitude;
            
            // This puts the Lat/Lng in the bar
            locationInput.value = `Lat: ${lat.toFixed(4)}, Lng: ${lng.toFixed(4)}`;
            status.textContent = "Location captured successfully!";
            btnText.textContent = "📍";
            
            // OPTIONAL: Call your price calculation function here
            // calculatePrice(lat, lng); 
        },
        // Error Callback
        (error) => {
            btnText.textContent = "📍";
            switch(error.code) {
                case error.PERMISSION_DENIED:
                    status.textContent = "Please allow location access in your settings.";
                    break;
                case error.POSITION_UNAVAILABLE:
                    status.textContent = "Location info is unavailable.";
                    break;
                case error.TIMEOUT:
                    status.textContent = "Request timed out.";
                    break;
            }
        }
    );
}

// Auto-run when the page loads
window.onload = getCurrentLocation;
</script>
<!DOCTYPE html>
<html lang="kn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ನಿಮ್ಮ ಮನೆವರೆಗೆ | Delivery</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap');
        body { font-family: 'Poppins', sans-serif; background: #fdf2f2; }
        .glass-card { background: rgba(255, 255, 255, 0.95); backdrop-filter: blur(10px); border-radius: 2rem; }
        .accent-gradient { background: linear-gradient(135deg, #FF4B2B 0%, #FF416C 100%); }
    </style>
</head>
<body class="bg-gray-50 min-h-screen pb-10">

    <header class="accent-gradient text-white pt-10 pb-20 px-6 rounded-b-[50px] text-center shadow-xl">
        <h1 class="text-5xl font-extrabold mb-3">ನಿಮ್ಮ ಮನೆವರೆಗೆ</h1>
        <p class="text-lg opacity-90 italic">"Fastest delivery in Kollegala - Freshness at your doorstep!"</p>
    </header>

    <main class="max-w-md mx-auto px-4 -mt-12">
        
        <div class="flex bg-white p-2 rounded-full shadow-lg mb-8">
            <button onclick="toggleTab('pd')" id="pd-tab" class="flex-1 py-3 rounded-full bg-red-500 text-white font-bold transition-all">
                <i class="fas fa-motorcycle mr-2"></i> Pick & Drop
            </button>
            <button onclick="toggleTab('food')" id="food-tab" class="flex-1 py-3 rounded-full text-gray-500 font-bold transition-all">
                <i class="fas fa-hamburger mr-2"></i> Home Food
            </button>
        </div>

        <div id="pd-section" class="glass-card p-6 shadow-2xl border border-white">
            <h2 class="text-2xl font-bold text-gray-800 mb-4">Pick & Drop Service</h2>
            
            <div class="space-y-4">
                <div class="relative">
                    <input id="pd-start" type="text" placeholder="Current Location" class="w-full p-4 pr-12 rounded-2xl bg-gray-100 border-none focus:ring-2 focus:ring-red-400">
                    <button onclick="autoCapture('pd-start', 'pd-price')" class="absolute right-4 top-4 text-red-500"><i class="fas fa-crosshairs"></i></button>
                </div>
                
                <input id="pd-dest" type="text" placeholder="Destination Location" class="w-full p-4 rounded-2xl bg-gray-100 border-none focus:ring-2 focus:ring-red-400">
                
                <div class="bg-red-50 p-4 rounded-2xl flex justify-between items-center">
                    <span class="font-bold text-gray-700">Estimated Price:</span>
                    <span id="pd-price-display" class="text-2xl font-black text-red-600">₹0</span>
                </div>

                <hr class="my-4">
                <input id="pd-name" type="text" placeholder="Your Name" class="w-full p-4 rounded-2xl bg-gray-100 border-none">
                <input id="pd-phone" type="tel" placeholder="Mobile Number" class="w-full p-4 rounded-2xl bg-gray-100 border-none">
                <textarea id="pd-msg" placeholder="Special Instructions" class="w-full p-4 rounded-2xl bg-gray-100 border-none h-24"></textarea>

                <button onclick="submitOrder('pd')" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-4 rounded-2xl shadow-lg flex justify-center items-center gap-2 text-lg">
                    <i class="fab fa-whatsapp text-2xl"></i> Send to WhatsApp
                </button>
            </div>
        </div>

        <div id="food-section" class="hidden glass-card p-6 shadow-2xl border border-white">
            <h2 class="text-3xl font-black text-center text-gray-800 mb-2">NAMMA KOLLEGALA</h2>
            <p class="text-center text-gray-500 mb-6 italic">"Home cooked love, delivered with care"</p>
            
            <div class="space-y-4">
                <input id="f-name" type="text" placeholder="Your Name" class="w-full p-4 rounded-2xl bg-gray-100 border-none">
                <input id="f-phone" type="tel" placeholder="Mobile Number" class="w-full p-4 rounded-2xl bg-gray-100 border-none">
                <textarea id="f-items" placeholder="List items you want to order..." class="w-full p-4 rounded-2xl bg-gray-100 border-none h-24"></textarea>
                
                <div class="relative">
                    <input id="f-loc" type="text" placeholder="Auto capturing location..." class="w-full p-4 pr-12 rounded-2xl bg-gray-100 border-none">
                    <button onclick="autoCapture('f-loc', 'f-price')" class="absolute right-4 top-4 text-orange-500"><i class="fas fa-location-arrow"></i></button>
                </div>

                <div class="bg-orange-50 p-4 rounded-2xl flex justify-between items-center">
                    <span class="font-bold text-gray-700">Delivery Fee:</span>
                    <span id="f-price-display" class="text-2xl font-black text-orange-600">₹0</span>
                </div>

                <button onclick="submitOrder('food')" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-4 rounded-2xl shadow-lg flex justify-center items-center gap-2 text-lg">
                    <i class="fab fa-whatsapp text-2xl"></i> Order via WhatsApp
                </button>
            </div>
        </div>

        <div id="payment-area" class="hidden mt-6 p-6 glass-card border-2 border-dashed border-red-300 text-center">
            <p class="text-gray-600 mb-4 font-semibold">Ready to Pay?</p>
            <a id="upi-btn" href="#" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full font-bold shadow-blue-200 shadow-xl">
                <i class="fas fa-mobile-alt mr-2"></i> Pay Now (UPI)
            </a>
        </div>

    </main>

    <script>
        // Central Point: Shree Choudeshwari Kalyanmantapa Road
        const CENTER_LAT = 12.1585; 
        const CENTER_LON = 77.1115;
        let currentPrice = 0;

        function toggleTab(type) {
            const pdTab = document.getElementById('pd-tab');
            const foodTab = document.getElementById('food-tab');
            const pdSec = document.getElementById('pd-section');
            const foodSec = document.getElementById('food-section');

            if(type === 'pd') {
                pdSec.classList.remove('hidden'); foodSec.classList.add('hidden');
                pdTab.className = "flex-1 py-3 rounded-full bg-red-500 text-white font-bold transition-all";
                foodTab.className = "flex-1 py-3 rounded-full text-gray-500 font-bold transition-all";
            } else {
                foodSec.classList.remove('hidden'); pdSec.classList.add('hidden');
                foodTab.className = "flex-1 py-3 rounded-full bg-red-500 text-white font-bold transition-all";
                pdTab.className = "flex-1 py-3 rounded-full text-gray-500 font-bold transition-all";
            }
        }

        function autoCapture(inputId, priceId) {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition((pos) => {
                    const lat = pos.coords.latitude;
                    const lon = pos.coords.longitude;
                    document.getElementById(inputId).value = `📍 Pos: ${lat.toFixed(4)}, ${lon.toFixed(4)}`;
                    
                    // Logic to calculate distance from Center
                    const dist = Math.sqrt(Math.pow(lat - CENTER_LAT, 2) + Math.pow(lon - CENTER_LON, 2)) * 111;
                    
                    let price = 30; // 1-2km
                    if (dist > 2) price = 40; // 2-3km
                    if (dist > 3) price = 50; // 3-4km
                    if (dist > 4) price = 60; // 4-5km
                    
                    currentPrice = price;
                    const displayId = inputId.includes('pd') ? 'pd-price-display' : 'f-price-display';
                    document.getElementById(displayId).innerText = `₹${price}`;
                });
            }
        }

        function submitOrder(type) {
            const phone = "9448167849";
            let msg = "";

            if(type === 'pd') {
                msg = `*PICK & DROP ORDER*%0AName: ${document.getElementById('pd-name').value}%0APhone: ${document.getElementById('pd-phone').value}%0AFrom: ${document.getElementById('pd-start').value}%0ATo: ${document.getElementById('pd-dest').value}%0AInstructions: ${document.getElementById('pd-msg').value}%0APrice: ₹${currentPrice}`;
            } else {
                msg = `*HOME FOOD ORDER*%0A_NAMMA KOLLEGALA_%0AName: ${document.getElementById('f-name').value}%0APhone: ${document.getElementById('f-phone').value}%0AItems: ${document.getElementById('f-items').value}%0ALocation: ${document.getElementById('f-loc').value}%0ADelivery Fee: ₹${currentPrice}`;
            }

            // Show Payment Button
            document.getElementById('payment-area').classList.remove('hidden');
            document.getElementById('upi-btn').href = `upi://pay?pa=9448167849@ptyes&pn=NimmaManevarege&am=${currentPrice}&cu=INR`;

            window.open(`https://wa.me/${phone}?text=${msg}`, '_blank');
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="kn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ನಿಮ್ಮ ಮನೆವರೆಗೆ | Namma Kollegala</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: #0f172a;
            color: white;
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
        }

        .btn-gradient {
            background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
            transition: transform 0.2s;
        }

        .btn-gradient:active {
            transform: scale(0.95);
        }

        .section-tab {
            cursor: pointer;
            transition: all 0.3s;
        }

        .active-tab {
            background: #f59e0b;
            color: black;
            box-shadow: 0 0 20px rgba(245, 158, 11, 0.4);
        }

        .animate-float {
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body class="pb-10">

    <header class="text-center py-10 px-4">
        <h1 class="text-5xl font-bold text-amber-500 mb-2">ನಿಮ್ಮ ಮನೆವರೆಗೆ</h1>
        <p class="text-gray-400 italic">"ರುಚಿಯಾದ ಅಡುಗೆ, ವೇಗವಾದ ಸೇವೆ - ನಿಮ್ಮ ಮನೆ ಬಾಗಿಲಿಗೆ"</p>
    </header>

    <div class="flex justify-center gap-4 mb-8 px-4">
        <div id="tab-pick" onclick="switchSection('pick')" class="section-tab active-tab flex items-center gap-2 px-6 py-4 rounded-2xl font-bold">
            <i data-lucide="bike" class="w-6 h-6"></i> Pick & Drop
        </div>
        <div id="tab-food" onclick="switchSection('food')" class="section-tab glass-card flex items-center gap-2 px-6 py-4 rounded-2xl font-bold">
            <i data-lucide="utensils" class="w-6 h-6"></i> Home Food
        </div>
    </div>

    <main class="max-w-md mx-auto px-4">
        
        <section id="section-pick" class="glass-card p-6 mb-6">
            <div class="flex items-center gap-3 mb-6">
                <div class="bg-amber-500 p-3 rounded-full animate-float">
                    <i data-lucide="package" class="text-black"></i>
                </div>
                <h2 class="text-xl font-semibold">Pick & Drop Service</h2>
            </div>

            <div class="space-y-4">
                <div>
                    <label class="block text-sm text-gray-400 mb-1">Pickup Location</label>
                    <div class="relative">
                        <input type="text" id="pick-origin" placeholder="Fetching location..." class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 pr-10 outline-none focus:border-amber-500">
                        <button onclick="getLocation('pick-origin')" class="absolute right-3 top-3 text-amber-500">
                            <i data-lucide="map-pin" class="w-5 h-5"></i>
                        </button>
                    </div>
                </div>

                <div>
                    <label class="block text-sm text-gray-400 mb-1">Destination</label>
                    <input type="text" id="pick-dest" placeholder="Where to drop?" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none focus:border-amber-500">
                </div>

                <div class="bg-slate-900 p-4 rounded-xl border border-dashed border-amber-500/30">
                    <p class="text-sm text-gray-400">Estimated Price</p>
                    <p class="text-2xl font-bold text-amber-500" id="pick-price">₹ --</p>
                    <p class="text-[10px] text-gray-500 mt-1">1-2km: 30 | 2-3km: 40 | 3-4km: 50 | 4-5km: 60</p>
                </div>

                <div class="space-y-3 pt-4 border-t border-slate-700">
                    <input type="text" id="pick-name" placeholder="Your Name" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none">
                    <input type="tel" id="pick-phone" placeholder="Mobile Number" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none">
                    <textarea id="pick-instr" placeholder="Special Instructions (Optional)" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none h-20"></textarea>
                </div>

                <button onclick="sendWhatsApp('pick')" class="btn-gradient w-full py-4 rounded-xl font-bold text-black flex items-center justify-center gap-2">
                    <i data-lucide="send"></i> Order via WhatsApp
                </button>
            </div>
        </section>

        <section id="section-food" class="hidden glass-card p-6 mb-6">
            <div class="text-center mb-6">
                <p class="text-amber-500 italic mb-1">"ಹೋಟೆಲ್ ಹರ್ಷ ವತಿಯಿಂದ ನೇರವಾಗಿ ನಿಮ್ಮ ಮನೆಗೆ"</p>
                <h2 class="text-3xl font-black tracking-tighter text-white">NAMMA KOLLEGALA</h2>
            </div>

            <div class="space-y-4">
                <input type="text" id="food-name" placeholder="Full Name" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none">
                <input type="tel" id="food-phone" placeholder="Mobile Number" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none">
                <textarea id="food-items" placeholder="List items you want (e.g. 2 Idli, 1 Vada)" class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 outline-none h-24"></textarea>
                
                <div class="relative">
                    <label class="block text-sm text-gray-400 mb-1">Your Delivery Location</label>
                    <input type="text" id="food-loc" placeholder="Auto capturing..." class="w-full bg-slate-800 border border-slate-700 rounded-lg p-3 pr-10 outline-none">
                    <button onclick="getLocation('food-loc')" class="absolute right-3 top-9 text-green-500">
                        <i data-lucide="navigation" class="w-5 h-5"></i>
                    </button>
                </div>

                <div class="bg-slate-900 p-4 rounded-xl border border-dashed border-green-500/30">
                    <p class="text-sm text-gray-400">Delivery Charge (from Choudeshwari Road)</p>
                    <p class="text-2xl font-bold text-green-500" id="food-price">₹ --</p>
                </div>

                <div class="bg-amber-900/20 p-4 rounded-xl border border-amber-500/20">
                    <p class="text-xs text-amber-500 font-bold mb-2">PAYMENT METHOD</p>
                    <a href="upi://pay?pa=9448167849@ptyes&pn=NammaKollegala&cu=INR" class="flex items-center justify-center gap-2 bg-white text-black py-2 rounded-lg font-bold text-sm">
                        <i data-lucide="smartphone"></i> Pay via UPI (9448167849@ptyes)
                    </a>
                </div>

                <button onclick="sendWhatsApp('food')" class="btn-gradient w-full py-4 rounded-xl font-bold text-black flex items-center justify-center gap-2 mt-4">
                    <i data-lucide="message-circle"></i> Place Order via WhatsApp
                </button>
            </div>
        </section>

        <footer class="text-center text-xs text-gray-500 mt-10 space-y-2">
            <p>© 2025 ನಿಮ್ಮ ಮನೆವರೆಗೆ | ನಮ್ಮ ಕೊಳ್ಳೇಗಾಲ ನಮ್ಮ ಹೆಮ್ಮೆ</p>
            <p>Experience authentic cuisine delivered to your doorstep. Our mission is to bring the taste of Kollegala to your home with premium quality.</p>
        </footer>
    </main>

    <script>
        // Initialize Icons
        lucide.createIcons();

        // Section Switching
        function switchSection(type) {
            const pickSection = document.getElementById('section-pick');
            const foodSection = document.getElementById('section-food');
            const pickTab = document.getElementById('tab-pick');
            const foodTab = document.getElementById('tab-food');

            if (type === 'pick') {
                pickSection.classList.remove('hidden');
                foodSection.classList.add('hidden');
                pickTab.classList.add('active-tab');
                foodTab.classList.remove('active-tab');
            } else {
                pickSection.classList.add('hidden');
                foodSection.classList.remove('hidden');
                pickTab.classList.remove('active-tab');
                foodTab.classList.add('active-tab');
            }
        }

        // Location Logic (Mock Distance for demo)
        function getLocation(inputId) {
            const input = document.getElementById(inputId);
            input.value = "Locating...";
            
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition((position) => {
                    const lat = position.coords.latitude;
                    const lon = position.coords.longitude;
                    input.value = `📍 Current Location (${lat.toFixed(4)}, ${lon.toFixed(4)})`;
                    
                    // Simulate price based on distance logic
                    // In a real app, use Google Distance Matrix API
                    const randomDist = Math.floor(Math.random() * 5) + 1; 
                    calculatePrice(randomDist, inputId.includes('pick') ? 'pick-price' : 'food-price');
                }, () => {
                    input.value = "Kollegala Main Town";
                    calculatePrice(2, inputId.includes('pick') ? 'pick-price' : 'food-price');
                });
            }
        }

        function calculatePrice(km, displayId) {
            let price = 30;
            if (km > 1) price = 30;
            if (km > 2) price = 40;
            if (km > 3) price = 50;
            if (km > 4) price = 60;
            document.getElementById(displayId).innerText = `₹ ${price}`;
        }

        // WhatsApp Integration
        function sendWhatsApp(type) {
            const phone = "9448167849";
            let message = "";

            if (type === 'pick') {
                const name = document.getElementById('pick-name').value;
                const pPhone = document.getElementById('pick-phone').value;
                const origin = document.getElementById('pick-origin').value;
                const dest = document.getElementById('pick-dest').value;
                const price = document.getElementById('pick-price').innerText;
                const instr = document.getElementById('pick-instr').value;

                message = `*PICK & DROP ORDER*%0A` +
                          `Name: ${name}%0A` +
                          `Phone: ${pPhone}%0A` +
                          `From: ${origin}%0A` +
                          `To: ${dest}%0A` +
                          `Price: ${price}%0A` +
                          `Notes: ${instr}`;
            } else {
                const name = document.getElementById('food-name').value;
                const fPhone = document.getElementById('food-phone').value;
                const items = document.getElementById('food-items').value;
                const loc = document.getElementById('food-loc').value;
                const price = document.getElementById('food-price').innerText;

                message = `*HOME FOOD ORDER*%0A` +
                          `Name: ${name}%0A` +
                          `Phone: ${fPhone}%0A` +
                          `Items: ${items}%0A` +
                          `Location: ${loc}%0A` +
                          `Delivery: ${price}`;
            }

            window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
        }
    </script>
</body>
</html>
