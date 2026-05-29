<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OurHandbook - Hisab Kitab</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', sans-serif; }
        body { background: #0A2240; color: #fff; padding: 10px; }
        .container { max-width: 600px; margin: auto; }
        .header { text-align: center; padding: 15px; background: #00D26A; border-radius: 10px; margin-bottom: 15px; }
        .header h1 { font-size: 24px; color: #0A2240; }
        .card { background: #132D4F; padding: 15px; border-radius: 10px; margin-bottom: 15px; }
        .total { display: flex; justify-content: space-between; text-align: center; }
        .total div h3 { color: #00D26A; font-size: 18px; }
        .total div p { font-size: 14px; opacity: 0.8; }
        input, select, button { width: 100%; padding: 12px; margin: 6px 0; border: none; border-radius: 8px; font-size: 16px; }
        input, select { background: #0A2240; color: #fff; border: 1px solid #00D26A; }
        button { background: #00D26A; color: #0A2240; font-weight: bold; cursor: pointer; }
        button:active { opacity: 0.8; }
        table { width: 100%; border-collapse: collapse; margin-top: 10px; font-size: 14px; }
        th, td { padding: 8px; text-align: left; border-bottom: 1px solid #0A2240; }
        th { background: #00D26A; color: #0A2240; }
        .delete-btn { background: #ff4d4d; color: white; padding: 5px 10px; font-size: 12px; width: auto; }
        .filter-row { display: flex; gap: 8px; }
        .filter-row select { flex: 1; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📘 OurHandbook</h1>
            <p>Apna Hisab Kitab</p>
        </div>

        <div class="card total">
            <div>
                <p>Aaj ki Bikri</p>
                <h3 id="totalBikri">₹0</h3>
            </div>
            <div>
                <p>Aaj ka Kharcha</p>
                <h3 id="totalKharcha">₹0</h3>
            </div>
            <div>
                <p>Udhaar Baaki</p>
                <h3 id="totalUdhaar">₹0</h3>
            </div>
        </div>

        <div class="card">
            <h3>Nayi Entry Jodein</h3>
            <input type="text" id="party" placeholder="Party/Customer Name">
            <input type="text" id="item" placeholder="Vivran / Item">
            <input type="number" id="amount" placeholder="Amount ₹">
            <select id="type">
                <option value="Bikri">Bikri</option>
                <option value="Kharcha">Kharcha</option>
                <option value="Udhaar Diya">Udhaar Diya</option>
                <option value="Jama Hua">Jama Hua</option>
