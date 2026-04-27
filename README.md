
<html>
<head>
    <title>Fitness Journey</title>
    <style>
        * {
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            background: black;
            color: white;
            min-height: 100vh;
            padding: 30px 20px;
            margin: 0;
        }

        .card {
            max-width: 650px;
            margin: 0 auto;
            background: white;
            border-radius: 24px;
            box-shadow: 0 20px 40px black;
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, white);
            color: black;
            padding: 40px 30px;
            text-align: center;
        }

        .header-icon {
            width: 80px;
            height: 80px;
            background: white;
            border-radius: 50%;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            opacity: 0.2;
        }

        .header h1 {
            font-size: 2.2em;
            margin: 0 0 10px 0;
            font-weight: 300;
            letter-spacing: 1px;
        }

        .subtitle {
            opacity: 0.9;
            font-size: 1.1em;
            margin: 0;
        }

        .form-container {
            padding: 50px 40px;
        }

        .input-group {
            margin-bottom: 28px;
        }

        .input-group.full-width {
            margin-bottom: 35px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: black;
            font-size: 0.95em;
            letter-spacing: 0.5px;
        }

        .input-wrapper {
            position: relative;
        }

        input {
            width: 100%;
            padding: 16px 20px;
            border: 2px solid white;
            border-radius: 16px;
            font-size: 16px;
            background: Gainsboro;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        input:focus {
            outline: none;
            border-color: white;
            background: black;
            box-shadow: 0 0 0 4px LightBlue;
            transform: translateY(-1px);
        }

        .dual-inputs {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .options-group {
            background: white;
            padding: 25px;
            border-radius: 16px;
            border: 2px solid LightGray;
            margin-bottom: 30px;
        }

        .options-title {
            font-weight: 600;
            margin-bottom: 20px;
            color: black;
        }

        .option-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            cursor: pointer;
            padding: 8px 0;
        }

        .option-item input[type="radio"],
        .option-item input[type="checkbox"] {
            width: 20px;
            height: 20px;
            margin-right: 15px;
            accent-color: white;
        }

        .submit-button {
            width: 100%;
            padding: 20px;
            background: linear-gradient(135deg, MediumSeaGreen 0%, SeaGreen 100%);
            color: white;
            border: none;
            border-radius: 16px;
            font-size: 1.15em;
            font-weight: 600;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px LightSeaGreen;
        }

        .submit-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px MediumSeaGreen;
        }

        .designer {
            text-align: center;
            padding: 25px 0;
            color: DarkGray;
            font-size: 0.9em;
            background: white;
            margin-top: 20px;
            border-radius: 12px;
            opacity: 0.1;
        }

        @media (max-width: 700px) {
            .dual-inputs {
                grid-template-columns: 1fr;
            }
            
            .card {
                margin: 10px;
                border-radius: 16px;
            }
            
            .form-container {
                padding: 40px 25px;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="header">
            <div class="header-icon">💪</div>
            <h1>Fitness Journey</h1>
            <p class="subtitle">Track your progress and start building healthier habits today</p>
        </div>

        <div class="form-container">
            <form>
                <div class="input-group dual-inputs">
                    <div class="input-group">
                        <label for="name">Full Name</label>
                        <div class="input-wrapper">
                            <input type="text" id="name" name="name" required>
                        </div>
                    </div>
                    <div class="input-group">
                        <label for="email">Email</label>
                        <div class="input-wrapper">
                            <input type="email" id="email" name="email" required>
                        </div>
                    </div>
                </div>

                <div class="input-group dual-inputs">
                    <div class="input-group">
                        <label for="address">Address</label>
                        <input type="text" id="address" name="address" required>
                    </div>
                    <div class="input-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" name="phone" required>
                    </div>
                </div>

                <div class="input-group">
                    <label>Gender</label>
                    <div class="options-group">
                        <div class="options-title">Select your gender:</div>
                        <label class="option-item">
                            <input type="radio" name="gender" value="male" required>
                            Male
                        </label>
                        <label class="option-item">
                            <input type="radio" name="gender" value="female">
                            Female
                        </label>
                    </div>
                </div>

                <div class="input-group full-width">
                    <label>Your Activities</label>
                    <div class="options-group">
                        <div class="options-title">Choose your favorite activities:</div>
                        <label class="option-item">
                            <input type="checkbox" name="activities" value="running">
                            🏃 Running
                        </label>
                        <label class="option-item">
                            <input type="checkbox" name="activities" value="cycling">
                            🚴 Cycling
                        </label>
                        <label class="option-item">
                            <input type="checkbox" name="activities" value="walking">
                            🚶 Walking
                        </label>
                        <label class="option-item">
                            <input type="checkbox" name="activities" value="weights">
                            🏋️ Weight Training
                        </label>
                        <label class="option-item">
                            <input type="checkbox" name="activities" value="yoga">
                            🧘 Yoga
                        </label>
                    </div>
                </div>

                <button type="submit" class="submit-button">Begin Journey</button>
            </form>
        </div>

        <div class="designer">
            Designed by <strong>Diaz, Brian James J. BSCS</strong>
        </div>
    </div>
</body>
</html>
Diaz, Brian James J.
