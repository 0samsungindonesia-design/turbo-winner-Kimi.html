<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kimi PS3 PKG Manager</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@300;500;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Rajdhani', sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
            overflow-x: hidden;
            color: #fff;
        }
        
        /* Animated Background Particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 0;
        }
        
        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: rgba(0, 150, 255, 0.5);
            border-radius: 50%;
            animation: float 20s infinite linear;
            box-shadow: 0 0 10px rgba(0, 150, 255, 0.8);
        }
        
        @keyframes float {
            from { transform: translateY(100vh) translateX(0); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            to { transform: translateY(-100vh) translateX(100px); opacity: 0; }
        }
        
        /* PS3 Wave Background */
        .wave-container {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 40%;
            z-index: 0;
            opacity: 0.3;
        }
        
        .wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 200%;
            height: 100%;
            background: linear-gradient(45deg, transparent 30%, rgba(0, 100, 200, 0.1) 50%, transparent 70%);
            animation: wave-move 15s ease-in-out infinite;
        }
        
        @keyframes wave-move {
            0%, 100% { transform: translateX(0) translateY(0); }
            50% { transform: translateX(-50%) translateY(-20px); }
        }
        
        /* Main Container */
        .container {
            position: relative;
            z-index: 1;
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header - XMB Style */
        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 30px;
            background: linear-gradient(90deg, rgba(0,0,0,0.8) 0%, rgba(20,20,40,0.6) 100%);
            border-bottom: 2px solid #00d4ff;
            backdrop-filter: blur(10px);
            margin-bottom: 40px;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 10px 40px rgba(0, 212, 255, 0.2);
        }
        
        .logo-section {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .ps3-logo {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #1a1a1a 0%, #333 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 36px;
            font-weight: 700;
            color: #00d4ff;
            border: 3px solid #00d4ff;
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.8);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 30px rgba(0, 212, 255, 0.5); }
            50% { box-shadow: 0 0 50px rgba(0, 212, 255, 0.8); }
        }
        
        .title-section h1 {
            font-size: 48px;
            font-weigh
