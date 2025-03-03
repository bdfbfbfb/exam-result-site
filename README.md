<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="موقع إعلان نتيجة الامتحان - أدخل رقمك لمعرفة نتيجتك بسهولة!">
    <meta name="keywords" content="نتائج الامتحانات, نتيجة الطالب, معرفة النتيجة">
    <meta name="author" content="Exam Results">
    <title>إعلان نتيجة الامتحان</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            text-align: center; 
            padding: 50px; 
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            color: #333;
        }
        h1 {
            color: #fff;
            text-shadow: 2px 2px 5px #000;
        }
        input, button {
            font-size: 1.2em; 
            padding: 10px; 
            margin-top: 10px;
            border-radius: 8px;
            border: none;
        }
        button {
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #result {
            font-size: 1.5em; 
            margin-top: 20px; 
            font-weight: bold;
        }
        .success {
            color: green;
            background: #d4edda;
            padding: 10px;
            border-radius: 8px;
            display: inline-block;
        }
        .fail {
            color: red;
            background: #f8d7da;
            padding: 10px;
            border-radius: 8px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <h1>🎉 إعلان نتيجة الامتحان 🎉</h1>
    <p>أدخل رقمك لمعرفة النتيجة:</p>
    <input type="number" id="studentNumber" placeholder="أدخل رقم الطالب">
    <button onclick="checkResult()">عرض النتيجة</button>
    <div id="result"></div>

    <script>
        function checkResult() {
            const studentNumber = document.getElementById("studentNumber").value;
            const resultDiv = document.getElementById("result");
            
            if (studentNumber == "25") {
                resultDiv.innerHTML = "🎉 مبروك! أنت ناجح ✅ 🎉";
                resultDiv.className = "success";
            } else {
                resultDiv.innerHTML = "😞 للأسف، لم يتم العثور على النتيجة ❌";
                resultDiv.className = "fail";
            }
        }
        
        document.getElementById("studentNumber").addEventListener("keypress", function(event) {
            if (event.key === "Enter") {
                checkResult();
            }
        });
    </script>
</body>
</html>
