<亞健康公主變黑變胖了,需要你來拯救!>

<html lang="zh-TW">

<head>

&nbsp;   <meta charset="UTF-8">

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

&nbsp;   <title>愛樂唯：騎士的拯救公主之旅 (計時挑戰)</title>

&nbsp;   <style>

&nbsp;       /\* CSS 樣式 \*/

&nbsp;       :root {

&nbsp;           --color-knight: #6a4c93; 

&nbsp;           --color-clear: #4ea8de; /\* 清 \*/

&nbsp;           --color-adjust: #f48c06; /\* 調 \*/

&nbsp;           --color-supplement: #2a9d8f; /\* 補 \*/

&nbsp;           --color-shape: #f72585; /\* 朔 \*/

&nbsp;           --color-bg: #f8f9fa;

&nbsp;           --color-text: #333;

&nbsp;           --color-timer: #ff5733; 

&nbsp;       }



&nbsp;       body {

&nbsp;           font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;

&nbsp;           background: linear-gradient(135deg, #a7e9af 0%, #47a0ff 100%);

&nbsp;           color: var(--color-text);

&nbsp;           display: flex;

&nbsp;           justify-content: center;

&nbsp;           align-items: center;

&nbsp;           min-height: 100vh;

&nbsp;           margin: 0;

&nbsp;           padding: 20px;

&nbsp;           box-sizing: border-box; 

&nbsp;       }



&nbsp;       .game-container {

&nbsp;           background: white;

&nbsp;           width: 100%;

&nbsp;           max-width: 700px;

&nbsp;           border-radius: 25px;

&nbsp;           box-shadow: 0 15px 35px rgba(0,0,0,0.2);

&nbsp;           overflow: hidden;

&nbsp;           position: relative;

&nbsp;       }



&nbsp;       .header {

&nbsp;           background: var(--color-knight);

&nbsp;           color: white;

&nbsp;           padding: 25px;

&nbsp;           text-align: center;

&nbsp;       }



&nbsp;       .header h1 { margin: 0; font-size: 1.8rem; }

&nbsp;       .header p { margin: 5px 0 0; opacity: 0.9; font-size: 1rem; }



&nbsp;       .progress-bar { height: 8px; background: #ddd; width: 100%; }

&nbsp;       

&nbsp;       .progress-fill {

&nbsp;           height: 100%;

&nbsp;           background: var(--color-shape);

&nbsp;           width: 0%;

&nbsp;           transition: width 0.4s ease;

&nbsp;       }



&nbsp;       .content {

&nbsp;           padding: 30px;

&nbsp;           text-align: center;

&nbsp;           min-height: 350px;

&nbsp;           display: flex;

&nbsp;           flex-direction: column;

&nbsp;           justify-content: center;

&nbsp;           align-items: center;

&nbsp;       }



&nbsp;       .btn {

&nbsp;           background: var(--color-knight);

&nbsp;           color: white;

&nbsp;           border: none;

&nbsp;           padding: 14px 28px;

&nbsp;           border-radius: 50px;

&nbsp;           font-size: 1.1rem;

&nbsp;           cursor: pointer;

&nbsp;           margin: 10px;

&nbsp;           transition: transform 0.1s, background 0.2s;

&nbsp;           width: 90%;

&nbsp;           max-width: 350px;

&nbsp;           font-weight: bold;

&nbsp;       }



&nbsp;       .btn:hover { transform: scale(1.03); background: #553c7a; }

&nbsp;       .btn:active { transform: scale(0.98); }



&nbsp;       .option-btn {

&nbsp;           background: var(--color-bg);

&nbsp;           color: var(--color-text);

&nbsp;           border: 2px solid #ddd;

&nbsp;           font-size: 1rem;

&nbsp;       }

&nbsp;       

&nbsp;       .option-btn:hover {

&nbsp;           border-color: var(--color-clear);

&nbsp;           background: #e6f7ff;

&nbsp;       }

&nbsp;       

&nbsp;       /\* 難度選擇按鈕樣式 \*/

&nbsp;       .difficulty-btn {

&nbsp;           background: #f0f0f0;

&nbsp;           color: #333;

&nbsp;           border: 2px solid #ccc;

&nbsp;           padding: 15px;

&nbsp;           margin: 10px;

&nbsp;           width: 80%;

&nbsp;           max-width: 300px;

&nbsp;           font-size: 1.1rem;

&nbsp;           font-weight: 600;

&nbsp;       }

&nbsp;       .difficulty-btn:hover {

&nbsp;           background: #fff;

&nbsp;           border-color: var(--color-knight);

&nbsp;           transform: scale(1.03);

&nbsp;       }



&nbsp;       /\* 倒計時顯示樣式 \*/

&nbsp;       #timerDisplay {

&nbsp;           font-size: 3rem;

&nbsp;           font-weight: 900;

&nbsp;           color: var(--color-timer);

&nbsp;           margin-bottom: 15px;

&nbsp;           min-height: 48px; 

&nbsp;       }

&nbsp;       

&nbsp;       /\* 其他樣式 \*/

&nbsp;       .level-badge {

&nbsp;           background: var(--color-shape);

&nbsp;           color: white;

&nbsp;           padding: 8px 20px;

&nbsp;           border-radius: 20px;

&nbsp;           font-size: 1rem;

&nbsp;           margin-bottom: 20px;

&nbsp;           display: inline-block;

&nbsp;           font-weight: bold;

&nbsp;           box-shadow: 0 4px 6px rgba(0,0,0,0.1);

&nbsp;       }

&nbsp;       .question-text {

&nbsp;           font-size: 1.35rem;

&nbsp;           margin-bottom: 30px;

&nbsp;           line-height: 1.6;

&nbsp;           font-weight: 500;

&nbsp;       }

&nbsp;       .product-image-placeholder {

&nbsp;           height: 120px;

&nbsp;           width: 120px;

&nbsp;           background: #eee;

&nbsp;           border-radius: 10px;

&nbsp;           margin-bottom: 20px;

&nbsp;           display: flex;

&nbsp;           flex-direction: column;

&nbsp;           align-items: center;

&nbsp;           justify-content: center;

&nbsp;           font-size: 0.8rem;

&nbsp;           color: #777;

&nbsp;           border: 1px dashed #ccc;

&nbsp;           text-align: center;

&nbsp;           padding: 5px;

&nbsp;       }

&nbsp;       .feedback {

&nbsp;           display: none;

&nbsp;           margin-top: 25px;

&nbsp;           padding: 20px;

&nbsp;           border-radius: 15px;

&nbsp;           text-align: left;

&nbsp;           width: 100%;

&nbsp;           max-width: 500px;

&nbsp;       }

&nbsp;       .feedback.correct { border: 2px solid var(--color-supplement); color: #006d5b; background: #e0f2f1; }

&nbsp;       .feedback.wrong { border: 2px solid var(--color-shape); color: #721c24; background: #f8d7da; }

&nbsp;       .result-score { font-size: 3.5rem; color: var(--color-knight); font-weight: 900; }

&nbsp;       .result-message { margin-bottom: 35px; color: #555; font-size: 1.1rem; }

&nbsp;       .character-display { font-size: 8rem; margin-bottom: 20px; line-height: 1; }

&nbsp;       .princess-initial { color: #8d4a41; } 

&nbsp;       .princess-final { color: #f72585; animation: pulse 1.5s infinite; } 

&nbsp;       @keyframes pulse {

&nbsp;           0% { transform: scale(1); opacity: 1; }

&nbsp;           50% { transform: scale(1.05); opacity: 0.8; }

&nbsp;           100% { transform: scale(1); opacity: 1; }

&nbsp;       }

&nbsp;       .hidden { display: none !important; }

&nbsp;       .fade-in { animation: fadeIn 0.5s; }

&nbsp;       @keyframes fadeIn {

&nbsp;           from { opacity: 0; transform: translateY(15px); }

&nbsp;           to { opacity: 1; transform: translateY(0); }

&nbsp;       }

&nbsp;   </style>

</head>

<body>



<div class="game-container">

&nbsp;   <div class="header">

&nbsp;       <h1>⚔️ 騎士的體內淨化之旅 👸</h1>

&nbsp;       <p>運用【清．調．補．朔】智慧，拯救平衡公主！</p>

&nbsp;   </div>

&nbsp;   

&nbsp;   <div class="progress-bar">

&nbsp;       <div class="progress-fill" id="progressFill"></div>

&nbsp;   </div>



&nbsp;   <div id="startScreen" class="content fade-in">

&nbsp;       <div class="character-display princess-initial">👸🏿</div>

&nbsp;       <h2>【亞健康公主】被困</h2>

&nbsp;       <p>請選擇您的挑戰難度，為公主奪回健康光彩！</p>

&nbsp;       <p style="font-weight: bold; color: var(--color-timer);">⏳ 作答時間：每題 15 秒</p>

&nbsp;       

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('easy')">

&nbsp;           簡單 (10 題 / 100 分) - 虹光之路

&nbsp;       </button>

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('medium')">

&nbsp;           挑戰 (15 題 / 150 分) - 極光之路

&nbsp;       </button>

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('hard')">

&nbsp;           專業 (20 題 / 200 分) - 日光之路

&nbsp;       </button>

&nbsp;   </div>



&nbsp;   <div id="gameScreen" class="content hidden fade-in">

&nbsp;       <div id="timerDisplay">15</div>



&nbsp;       <div id="animationArea" class="character-display knight">⚔️</div>

&nbsp;       <span id="levelBadge" class="level-badge">關卡載入中...</span>

&nbsp;       

&nbsp;       <div id="productPlaceholder" class="product-image-placeholder">

&nbsp;           \[產品圖片佔位 - 可替換為產品圖 URL]

&nbsp;       </div>



&nbsp;       <div id="questionText" class="question-text">題目載入中...</div>

&nbsp;       <div id="optionsContainer" style="width: 100%; display: flex; flex-direction: column; align-items: center;">

&nbsp;           </div>

&nbsp;       

&nbsp;       <div id="feedbackArea" class="feedback">

&nbsp;           <h3 id="feedbackTitle" style="margin-top:0;"></h3>

&nbsp;           <p id="feedbackText" style="margin-bottom:0;"></p>

&nbsp;           <button class="btn" id="nextBtn" onclick="nextQuestion()" style="margin-top: 15px;">下一題</button>

&nbsp;       </div>

&nbsp;   </div>



&nbsp;   <div id="resultScreen" class="content hidden fade-in">

&nbsp;       <div id="finalCharacterDisplay" class="character-display princess-initial">👸🏿</div>

&nbsp;       <h2>闖關結果揭曉！</h2>

&nbsp;       <div class="result-score" id="finalScore">0</div>

&nbsp;       <p class="result-message" id="resultMessage">正在分析您的健康指數...</p>

&nbsp;       <button class="btn" onclick="restartGame()">再次挑戰</button>

&nbsp;   </div>

</div>



<script>

&nbsp;   // --- 配置常數 ---

&nbsp;   const TIMER\_LIMIT = 15; // 倒數計時改為 15 秒

&nbsp;   const MAX\_SCORE\_PER\_QUESTION = 10;



&nbsp;   // --- 難度配置 ---

&nbsp;   const difficultySettings = {

&nbsp;       'easy': {

&nbsp;           count: 10,

&nbsp;           titlePerfect: "愛樂唯虹光騎士",

&nbsp;           titleGreat: "愛樂唯知識家",

&nbsp;           draw: { 'clear': 3, 'adjust': 3, 'supplement': 2, 'shape': 1, 'final': 1 }

&nbsp;       },

&nbsp;       'medium': {

&nbsp;           count: 15,

&nbsp;           titlePerfect: "愛樂唯極光騎士",

&nbsp;           titleGreat: "愛樂唯菁英",

&nbsp;           draw: { 'clear': 4, 'adjust': 4, 'supplement': 4, 'shape': 2, 'final': 1 }

&nbsp;       },

&nbsp;       'hard': {

&nbsp;           count: 20,

&nbsp;           titlePerfect: "愛樂唯日光騎士",

&nbsp;           titleGreat: "愛樂唯專家",

&nbsp;           // 專業級：從每個分類多抽，確保總數達到 20 題

&nbsp;           draw: { 'clear': 5, 'adjust': 5, 'supplement': 6, 'shape': 2, 'final': 2 }

&nbsp;       }

&nbsp;   };

&nbsp;   // 範例：請在您的程式碼中找到類似的產品定義

&nbsp;   "PuraBio": {

&nbsp;       name: "澄熙益生菌 PurαBio",

&nbsp;       \[cite\_start]description: "17種益菌菌株為您及家人打造完美防護，維持消化道機能，改變細菌叢生態。", // \[cite: 58, 59] (根據您的文件)

&nbsp;       // 🚨 新增圖片路徑欄位

&nbsp;       image: "澄熙益生菌-DM-2.jpg" 

&nbsp;   },

&nbsp;   "Auro": {

&nbsp;       name: "極淨纖果粉 Auro α",

&nbsp;       \[cite\_start]description: "結合了草本植物、複合纖維和專利酵素，能讓排便順暢。", // \[cite: 32] (根據您的文件)

&nbsp;       // 🚨 新增圖片路徑欄位

&nbsp;       image: "極淨纖果粉DM-4.jpg" 

&nbsp;   },

&nbsp;   // 請依照此格式，將所有產品都加入對應的圖片檔名

&nbsp;   "Flora": {

&nbsp;       name: "亮妍嬌源飲 Florα",

&nbsp;       \[cite\_start]description: "彈力潤澤的青春肌密，一包蘊含5,000毫克膠原蛋白，專為30+以上設計配方。", // \[cite: 78, 79] (根據您的文件)

&nbsp;       image: "Adobe Express - file (1).png" 

&nbsp;   },

&nbsp;   "Eterna": {

&nbsp;       name: "恆芯營養粉 Eterna",

&nbsp;       \[cite\_start]description: "專為日常補養、熟齡保健打造的營養複方，提供「喝的營養照護方案」。", // \[cite: 115] (根據您的文件)

&nbsp;       image: "ALFAWISE\_網站恆芯-02-scaled.jpg" 

&nbsp;   },

&nbsp;   "Spark": {

&nbsp;       name: "閃朔蜜桃飲 Spαrk",

&nbsp;       \[cite\_start]description: "獨家代謝配方，激發身體潛能，加速新陳代謝，減少對食物的渴望。", // \[cite: 129] (根據您的文件)

&nbsp;       image: "閃朔蜜桃飲3.jpg" 

&nbsp;   },

&nbsp;   "DawnBliss": {

&nbsp;       name: "昕悅活力飲 DαwnBliss",

&nbsp;       \[cite\_start]description: "維持整天活力的美體飲品，蘊含花青素與維生素B，喚醒身體、調節機能。", // \[cite: 4] (根據您的文件)

&nbsp;       image: "Adobe Express - file (1).png" 

&nbsp;   }

};

&nbsp;   // --- 擴充的完整題目庫 (FULL QUESTION BANK) ---

&nbsp;   // 總共 20 題 (清x5, 調x5, 補x6, 朔x2, Final x2)

&nbsp;   const fullQuestionBank = {

&nbsp;       // --- Level 1: 清 (Auro + Down Bliss) --- 

&nbsp;       'clear': \[

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "宿便怪", animation: "🐛",

&nbsp;               question: "極淨纖果粉中，能幫助維持消化道機能的珍貴草本精華是？",

&nbsp;               options: \["綠咖啡", "望江南和決明子", "膠原蛋白", "維生素 C"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*望江南和決明子\*\*等草本精華幫助維持消化道機能，讓排便更順暢。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "積食怪", animation: "⚔️",

&nbsp;               question: "極淨纖果粉中，100%由非基因改造大豆做基底，能幫助營養素吸收的美國專利成分是什麼？",

&nbsp;               options: \["MBP 鈣結合蛋白", "藤黃果 HCA", "AES 綜合酵素", "L-茶胺酸"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*AES 綜合酵素\*\*能幫助營養素吸收，減少過度積食的負擔。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "素食疑慮", animation: "🌿",

&nbsp;               question: "極淨纖果粉的素食屬性是屬於哪一類？",

&nbsp;               options: \["全素", "純素", "奶素", "蛋奶素"],

&nbsp;               correct: 2, explanation: "✅ 正確！極淨纖果粉為\*\*奶素\*\*，不適合全素食者。"

&nbsp;           },

&nbsp;           // \*\*更新題：昕悅活力飲 - 能量成分\*\*

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Down Bliss 昕悅活力飲", enemy: "精神不濟", animation: "☕",

&nbsp;               question: "昕悅活力飲中，被稱為「巴西國飲」且富含天然咖啡因，能滋補強身、增進效率的成分是？",

&nbsp;               options: \["綠茶萃取", "巴西瓜拿納果", "瑪卡", "薑黃素"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*巴西瓜拿納果\*\*能滋補強身、增強體力，富含天然咖啡因可增進效率。"

&nbsp;           },

&nbsp;           // \*\*新增題：昕悅活力飲 - 代謝成分\*\*

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Down Bliss 昕悅活力飲", enemy: "代謝緩慢", animation: "🍊",

&nbsp;               question: "昕悅活力飲中，富含川陳皮素、橘紅素、辛弗林等，幫助促進新陳代謝，適合關注體態管理者的成分是什麼？",

&nbsp;               options: \["專利紅橙萃取", "專利柑橘幼果萃取", "專利黑胡椒萃取", "專利藤黃果萃取"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*專利柑橘幼果萃取\*\*富含川陳皮素、橘紅素、辛弗林等，有助於促進新陳代謝。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 2: 調 (PurBio) --- 

&nbsp;       'adjust': \[

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "搞怪軍團 (壞菌)", animation: "🦠",

&nbsp;               question: "PurBio 澄熙益生菌含有幾種具身分履歷的強大菌株，以全方位調整體質？",

&nbsp;               options: \["5 種", "10 種", "17 種", "25 種"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*17 種\*\*益菌戰隊能改變細菌叢生態，促進健康維持。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "胃酸威脅", animation: "🛡️",

&nbsp;               question: "PurBio 澄熙益生菌採用的技術，目的是保護菌種能成功通過胃酸，提高定殖率，請問這是哪種技術？",

&nbsp;               options: \["冷凍乾燥技術", "微粒包覆技術", "超高溫瞬時滅菌", "天然發酵法"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*微粒包覆技術\*\*能保護菌種，讓益生菌精準送達腸道。"

&nbsp;           },

&nbsp;            {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "甜味誘惑", animation: "🍎",

&nbsp;               question: "澄熙益生菌的甜味主要來自哪種經美國 FDA 認定為 GRAS 等級的成分？",

&nbsp;               options: \["果寡糖", "木糖醇", "甜菊糖苷", "天然香料"],

&nbsp;               correct: 1, explanation: "✅ 正確！甜味主要來自於\*\*木糖醇\*\*與天然香料。木糖醇熱量低且被美國 FDA 認定為 GRAS 等級。"

&nbsp;           },

&nbsp;            {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "素食疑慮", animation: "🥦",

&nbsp;               question: "關於澄熙益生菌，哪項描述是正確的？",

&nbsp;               options: \["含有蛋奶製品", "為純素可食", "含有動物性成分", "為奶素食品"],

&nbsp;               correct: 1, explanation: "✅ 正確！澄熙益生菌不含動物性成分，不含蛋奶製品，為\*\*純素可食\*\*。"

&nbsp;           },

&nbsp;           // \*\*新增題：澄熙益生菌 - 用量\*\*

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "用量困惑", animation: "🥄",

&nbsp;               question: "3歲以上兒童建議一天一包，請問成人建議量與加強建議量分別是多少？",

&nbsp;               options: \["成人：每日睡前 1 包；加強：每日睡前 2 包", "成人：每日三餐飯前 1 包；加強：每日三餐飯前 2 包", "成人：每日一餐飯後 1 包；加強：每日兩餐飯後 1 包", "成人：每日 2 包；加強：每日 3 包"],

&nbsp;               correct: 1, explanation: "✅ 正確！成人建議量為\*\*每日三餐飯前 1 包\*\*，加強建議量為\*\*每日三餐飯前 2 包\*\*。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 3: 補 (Flor + Etern) --- 

&nbsp;       'supplement': \[

&nbsp;           // Flor 亮妍嬌源飲 

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "乾燥細紋", animation: "💖",

&nbsp;               question: "亮妍嬌源飲中，一包蘊含多少毫克的魚膠原蛋白，並使用酵素水解技術提高吸收效率？",

&nbsp;               options: \["1,000 毫克", "5,000 毫克", "10,000 毫克", "2,500 毫克"],

&nbsp;               correct: 1, explanation: "✅ 正確！一包亮妍嬌源飲蘊含 \*\*5,000 毫克\*\*高品質魚膠原蛋白。"

&nbsp;           },

&nbsp;           // Etern 恆芯營養粉 

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "骨骼健康", animation: "🦴",

&nbsp;               question: "恆芯營養粉中，來自牛乳萃取物，能輔助維持骨骼健康的活性胜肽成分是什麼？",

&nbsp;               options: \["高鈣乳酪", "牛奶活性胜肽MBP", "酪梨大豆萃取物", "維生素 K2"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*牛奶活性胜肽MBP\*\*適合輔助日常營養補充與維持骨骼健康。"

&nbsp;           },

&nbsp;           // 亮妍嬌源飲

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "素顏不美", animation: "✨",

&nbsp;               question: "哪種專利益生菌，擁有 8 項專利與 3 篇期刊發表，是增添肌膚水潤與提升關鍵力的主要成分？",

&nbsp;               options: \["專利燕窩酸益生菌", "嗜酸乳桿菌", "專利自產玻尿酸益生菌 (嗜熱鏈球菌)", "比菲德氏菌"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*專利自產玻尿酸益生菌 (嗜熱鏈球菌)\*\* 榮獲國際發明展銀獎，能增添肌膚水潤與提升關鍵力。"

&nbsp;           },

&nbsp;           // 恆芯營養粉

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "營養不均", animation: "🏋️",

&nbsp;               question: "恆芯營養粉的優質「動植物雙蛋白」互補配方是？",

&nbsp;               options: \["酪蛋白＋豌豆蛋白", "乳清蛋白＋大豆蛋白＋白胺酸", "蛋清蛋白＋米蛋白", "魚膠原＋大豆蛋白"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*乳清蛋白＋大豆蛋白＋白胺酸\*\*組成的雙蛋白複方，提供優質營養，吸收佳且飽足久。"

&nbsp;           },

&nbsp;           // \*\*新增題：恆芯營養粉 - 草本成分\*\*

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "行動力下降", animation: "🌿",

&nbsp;               question: "恆芯營養粉中，除了鈣和維生素外，還添加了哪兩種植物素材，有助於調節生理機能？",

&nbsp;               options: \["人參、靈芝", "枸杞、紅棗", "甘藷萃取物、穿心蓮", "薑黃、肉桂"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*甘藷萃取物\*\*與\*\*穿心蓮\*\*是常見的植物素材，可協助維持健康、調整體質。"

&nbsp;           },

&nbsp;           // \*\*新增題：亮妍嬌源飲 - 甜味\*\*

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "甜食渴望", animation: "🍬",

&nbsp;               question: "亮妍嬌源飲的甜味來自哪種熱量低的代糖，被美國 FDA 認定為 GRAS (最高安全規格)？",

&nbsp;               options: \["阿斯巴甜", "甜菊糖苷", "蔗糖素", "果糖"],

&nbsp;               correct: 1, explanation: "✅ 正確！甜味來自於草本萃取的\*\*甜菊糖苷\*\*，甜度高熱量低，符合最高安全規格。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 4: 朔 (Spork) --- 

&nbsp;       'shape': \[

&nbsp;           {

&nbsp;               level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",

&nbsp;               product: "Spork 閃朔蜜桃飲", enemy: "體脂魔王", animation: "🔥",

&nbsp;               question: "閃朔蜜桃飲系列中，哪種成分含有豐富 HCA（羥基檸檬酸），能幫助消化並降低對食物的慾望？",

&nbsp;               options: \["綠咖啡萃取", "藤黃果萃取", "葡萄皮萃取", "兒茶素"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*藤黃果萃取物\*\*含有豐富 HCA，是飲食管控的好幫手。"

&nbsp;           },

&nbsp;           // 朔奶茶飲

&nbsp;           {

&nbsp;               level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",

&nbsp;               product: "Spork 朔奶茶飲", enemy: "腹部堆積", animation: "☕",

&nbsp;               question: "朔奶茶飲中特有的哪種成分，具有調節生理機能、減少腹部堆積的功效？",

&nbsp;               options: \["綠咖啡萃取物", "藤黃果萃取物", "白藜蘆醇", "川芎萃取物"],

&nbsp;               correct: 3, explanation: "✅ 正確！\*\*川芎萃取物\*\*能調節生理機能，幫助身體輕盈不卡水。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 5: 最終智慧 (餐量管理) --- 

&nbsp;       'final': \[

&nbsp;            // \*\*修正後的題目 (原遺漏逗號)\*\*

&nbsp;            {

&nbsp;               level: "最終關：大師的智慧", levelColor: "var(--color-knight)",

&nbsp;               product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🧘",

&nbsp;               question: "愛樂唯餐量管理理念的核心口訣是「吃肉肉減肉肉．喝神飲減肉肉．\_\_\_\_\_\_\_\_\_\_\_\_」？",

&nbsp;               options: \["多運動減肉肉", "不用動減肉肉", "少吃澱粉減肉肉", "不吃肉減肉肉"],

&nbsp;               correct: 1, explanation: "✅ 正確！愛樂唯餐量管理口訣為：\*\*吃肉肉減肉肉．喝神飲減肉肉．不用動減肉肉\*\*。"

&nbsp;           }, // <--- 關鍵修復：這裡補上了逗號 (,)

&nbsp;           {

&nbsp;               level: "最終關：大師的智慧", levelColor: "var(--color-knight)",

&nbsp;               product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🍽️",

&nbsp;               question: "愛樂唯餐量管理的目標是把健康變簡單，請問下列哪一項是其中關鍵理念？",

&nbsp;               options: \["多樣化的產品線", "產品簡單化更能融入生活", "專注於單一功能", "強調複雜的營養學"],

&nbsp;               correct: 1, explanation: "✅ 正確！產品簡單化更能融入生活，讓忙碌的生活也能輕鬆維持健康。" 

&nbsp;           }

&nbsp;       ]

&nbsp;   };



&nbsp;   let currentQuestions = \[]; 

&nbsp;   let currentQuestionIndex = 0;

&nbsp;   let score = 0;

&nbsp;   let isAnswering = false;

&nbsp;   let timerInterval = null; 

&nbsp;   let hasAnswered = false; 

&nbsp;   let selectedDifficulty = null; 

&nbsp;   let maxGameScore = 0; 



&nbsp;   // DOM Elements

&nbsp;   const startScreen = document.getElementById('startScreen');

&nbsp;   const gameScreen = document.getElementById('gameScreen');

&nbsp;   const resultScreen = document.getElementById('resultScreen');

&nbsp;   const questionText = document.getElementById('questionText');

&nbsp;   const optionsContainer = document.getElementById('optionsContainer');

&nbsp;   const levelBadge = document.getElementById('levelBadge');

&nbsp;   const feedbackArea = document.getElementById('feedbackArea');

&nbsp;   const feedbackTitle = document.getElementById('feedbackTitle');

&nbsp;   const feedbackText = document.getElementById('feedbackText');

&nbsp;   const nextBtn = document.getElementById('nextBtn');

&nbsp;   const progressFill = document.getElementById('progressFill');

&nbsp;   const productPlaceholder = document.getElementById('productPlaceholder');

&nbsp;   const animationArea = document.getElementById('animationArea');

&nbsp;   const timerDisplay = document.getElementById('timerDisplay'); 





&nbsp;   // --- 輔助函式：陣列隨機洗牌 ---

&nbsp;   function shuffleArray(array) {

&nbsp;       for (let i = array.length - 1; i > 0; i--) {

&nbsp;           const j = Math.floor(Math.random() \* (i + 1));

&nbsp;           let temp = array\[i];

&nbsp;           array\[i] = array\[j];

&nbsp;           array\[j] = temp;

&nbsp;       }

&nbsp;       return array;

&nbsp;   }



&nbsp;   // --- 倒計時邏輯 ---

&nbsp;   function startTimer() {

&nbsp;       let timeLeft = TIMER\_LIMIT;

&nbsp;       timerDisplay.textContent = timeLeft;

&nbsp;       timerDisplay.style.color = 'var(--color-timer)';

&nbsp;       

&nbsp;       timerInterval = setInterval(() => {

&nbsp;           timeLeft--;

&nbsp;           timerDisplay.textContent = timeLeft;



&nbsp;           if (timeLeft <= 5) {

&nbsp;               // 剩下 5 秒開始變紅色警示

&nbsp;               timerDisplay.style.color = '#ff0000';

&nbsp;           } else if (timeLeft <= 10) {

&nbsp;                // 剩下 10 秒變黃色警示

&nbsp;               timerDisplay.style.color = 'var(--color-adjust)';

&nbsp;           }





&nbsp;           if (timeLeft <= 0) {

&nbsp;               clearInterval(timerInterval);

&nbsp;               timerDisplay.textContent = '時間到！';

&nbsp;               // 如果時間到還沒作答，強制執行 checkAnswer (傳入 -1 代表未作答)

&nbsp;               if (!hasAnswered) {

&nbsp;                   checkAnswer(-1); 

&nbsp;               }

&nbsp;           }

&nbsp;       }, 1000); // 每秒執行

&nbsp;   }



&nbsp;   // --- 核心變動：根據難度選擇抽取題目並開始遊戲 ---

&nbsp;   function startGame(difficulty) {

&nbsp;       selectedDifficulty = difficulty;

&nbsp;       const settings = difficultySettings\[difficulty];

&nbsp;       

&nbsp;       // 畫面切換

&nbsp;       startScreen.classList.add('hidden');

&nbsp;       gameScreen.classList.remove('hidden');

&nbsp;       

&nbsp;       currentQuestionIndex = 0;

&nbsp;       score = 0;

&nbsp;       currentQuestions = \[]; 

&nbsp;       maxGameScore = settings.count \* MAX\_SCORE\_PER\_QUESTION;



&nbsp;       // 1. 根據難度設定，從每個主題庫中隨機抽取題目

&nbsp;       const drawCounts = settings.draw;

&nbsp;       

&nbsp;       for (const key in drawCounts) {

&nbsp;           const count = drawCounts\[key];

&nbsp;           const shuffledBank = shuffleArray(\[...fullQuestionBank\[key]]); 

&nbsp;           currentQuestions.push(...shuffledBank.slice(0, count)); 

&nbsp;       }

&nbsp;       

&nbsp;       // 確保總題庫的順序是隨機的

&nbsp;       currentQuestions = shuffleArray(currentQuestions);





&nbsp;       // 2. 隨機洗牌選項

&nbsp;       currentQuestions = currentQuestions.map(q => {

&nbsp;           const originalOptions = q.options;

&nbsp;           const correctText = originalOptions\[q.correct];

&nbsp;           

&nbsp;           const newOptions = shuffleArray(\[...originalOptions]);

&nbsp;           const newCorrectIndex = newOptions.indexOf(correctText);



&nbsp;           return {

&nbsp;               ...q,

&nbsp;               options: newOptions,

&nbsp;               correct: newCorrectIndex

&nbsp;           };

&nbsp;       });



&nbsp;       showQuestion();

&nbsp;   }

&nbsp;   

&nbsp;   // --- 顯示題目 ---

&nbsp;   function showQuestion() {

&nbsp;       isAnswering = true;

&nbsp;       hasAnswered = false; // 重設作答狀態

&nbsp;       feedbackArea.style.display = 'none';

&nbsp;       

&nbsp;       const buttons = optionsContainer.querySelectorAll('button');

&nbsp;       buttons.forEach(btn => btn.remove());

&nbsp;       

&nbsp;       // 清除前一題的計時器 (如果有)

&nbsp;       if (timerInterval) {

&nbsp;           clearInterval(timerInterval);

&nbsp;       }



&nbsp;       const q = currentQuestions\[currentQuestionIndex]; 

&nbsp;       

&nbsp;       // 動態更新 UI

&nbsp;       levelBadge.textContent = `${q.level} (第 ${currentQuestionIndex + 1} 題 / 共 ${currentQuestions.length} 題)`;

&nbsp;       levelBadge.style.backgroundColor = q.levelColor;

&nbsp;       questionText.textContent = q.question;

&nbsp;       

&nbsp;       animationArea.textContent = q.animation;

&nbsp;       // 產品圖片佔位符，顯示產品名稱和敵人

&nbsp;       productPlaceholder.innerHTML = `<div style="font-size: 0.9rem; font-weight: bold; color: ${q.levelColor};">${q.product}</div><div style="font-size: 0.7rem; color: #777;">(敵人/問題點: ${q.enemy})</div>`;

&nbsp;       

&nbsp;       // 更新進度條

&nbsp;       const progress = (currentQuestionIndex / currentQuestions.length) \* 100;

&nbsp;       progressFill.style.width = `${progress}%`;



&nbsp;       // 渲染選項

&nbsp;       optionsContainer.innerHTML = '';

&nbsp;       q.options.forEach((opt, index) => {

&nbsp;           const btn = document.createElement('button');

&nbsp;           btn.className = 'btn option-btn fade-in';

&nbsp;           btn.textContent = opt;

&nbsp;           btn.onclick = () => checkAnswer(index);

&nbsp;           optionsContainer.appendChild(btn);

&nbsp;       });



&nbsp;       // 啟動計時器

&nbsp;       startTimer();

&nbsp;   }



&nbsp;   // --- 檢查答案 (處理時間到未作答) ---

&nbsp;   function checkAnswer(selectedIndex) {

&nbsp;       if (!isAnswering \&\& selectedIndex !== -1) return; 

&nbsp;       if (hasAnswered \&\& selectedIndex !== -1) return;



&nbsp;       // 立即停止計時器

&nbsp;       clearInterval(timerInterval);

&nbsp;       isAnswering = false;

&nbsp;       hasAnswered = true;



&nbsp;       const q = currentQuestions\[currentQuestionIndex];

&nbsp;       const isCorrect = selectedIndex === q.correct;

&nbsp;       

&nbsp;       // 如果是時間到且未作答

&nbsp;       if (selectedIndex === -1) {

&nbsp;            feedbackTitle.textContent = `⏰ 時間到！`;

&nbsp;            feedbackText.innerHTML = `<strong>遺憾！</strong>您未能在 ${TIMER\_LIMIT} 秒內作答，本題不計分。正確答案是：${q.options\[q.correct]}`;

&nbsp;            feedbackArea.className = `feedback wrong fade-in`;

&nbsp;       } else {

&nbsp;           // 正常作答

&nbsp;           const buttons = optionsContainer.querySelectorAll('button');

&nbsp;           buttons.forEach((btn, idx) => {

&nbsp;               btn.disabled = true; // 禁用所有按鈕

&nbsp;               if (idx === q.correct) {

&nbsp;                   btn.style.backgroundColor = 'var(--color-supplement)'; 

&nbsp;                   btn.style.color = 'white';

&nbsp;               } else if (idx === selectedIndex \&\& !isCorrect) {

&nbsp;                   btn.style.backgroundColor = 'var(--color-shape)'; 

&nbsp;                   btn.style.color = 'white';

&nbsp;               } else {

&nbsp;                   btn.style.opacity = '0.5';

&nbsp;               }

&nbsp;           });



&nbsp;           feedbackArea.style.display = 'block';

&nbsp;           feedbackArea.className = `feedback ${isCorrect ? 'correct' : 'wrong'} fade-in`;

&nbsp;           feedbackTitle.textContent = isCorrect ? `🎉 成功！騎士擊敗了 ${q.enemy}` : `💥 失誤！ ${q.enemy} 暫時擋住了去路`;

&nbsp;           

&nbsp;           if (isCorrect) {

&nbsp;               score += MAX\_SCORE\_PER\_QUESTION;

&nbsp;               feedbackText.innerHTML = `<strong>知識解析：</strong> ${q.explanation}`;

&nbsp;           } else {

&nbsp;               feedbackText.innerHTML = `<strong>錯誤解析：</strong> 答案是 \*\*${q.options\[q.correct]}\*\*。<br>${q.explanation}`;

&nbsp;           }

&nbsp;       }

&nbsp;       

&nbsp;       // 確保結果顯示

&nbsp;       feedbackArea.style.display = 'block';



&nbsp;       if (currentQuestionIndex === currentQuestions.length - 1) {

&nbsp;           nextBtn.textContent = "拯救公主 (查看結果)";

&nbsp;       } else {

&nbsp;           nextBtn.textContent = "繼續前進";

&nbsp;       }

&nbsp;   }



&nbsp;   function nextQuestion() {

&nbsp;       currentQuestionIndex++;

&nbsp;       if (currentQuestionIndex < currentQuestions.length) {

&nbsp;           showQuestion();

&nbsp;       } else {

&nbsp;           showResult();

&nbsp;       }

&nbsp;   }



&nbsp;   function showResult() {

&nbsp;       gameScreen.classList.add('hidden');

&nbsp;       resultScreen.classList.remove('hidden');

&nbsp;       

&nbsp;       const settings = difficultySettings\[selectedDifficulty];

&nbsp;       const finalScoreElement = document.getElementById('finalScore');

&nbsp;       const resultMessage = document.getElementById('resultMessage');

&nbsp;       const finalCharacterDisplay = document.getElementById('finalCharacterDisplay');

&nbsp;       

&nbsp;       progressFill.style.width = '100%';



&nbsp;       let title = '';

&nbsp;       // 滿分 (100%)

&nbsp;       if (score === maxGameScore) {

&nbsp;           title = settings.titlePerfect;

&nbsp;           finalCharacterDisplay.textContent = '👸🏼'; 

&nbsp;           finalCharacterDisplay.className = 'character-display princess-final fade-in';

&nbsp;           resultMessage.innerHTML = `恭喜！您以 \*\*${maxGameScore} 分\*\* 滿分，獲得<br>【\*\*${title}\*\*】稱號！公主已恢復光彩！`;

&nbsp;       } 

&nbsp;       // 高分 (≥ 70%)

&nbsp;       else if (score >= maxGameScore \* 0.7) {

&nbsp;           title = settings.titleGreat;

&nbsp;           finalCharacterDisplay.textContent = '👸🏽';

&nbsp;           finalCharacterDisplay.className = 'character-display princess-initial fade-in';

&nbsp;           resultMessage.innerHTML = `表現優異！您獲得【\*\*${title}\*\*】稱號！<br>最終得分：${score} 分，公主正在好轉中！`;

&nbsp;       } 

&nbsp;       // 及格以下 (< 70%)

&nbsp;       else {

&nbsp;           title = "養生學徒";

&nbsp;           finalCharacterDisplay.textContent = '👸🏿';

&nbsp;           finalCharacterDisplay.className = 'character-display princess-initial fade-in';

&nbsp;           resultMessage.innerHTML = `您是【\*\*${title}\*\*】，知識還需磨練！<br>最終得分：${score} 分，公主狀態有改善，但仍需努力！`;

&nbsp;       }



&nbsp;       // 分數動畫

&nbsp;       let currentScore = 0;

&nbsp;       finalScoreElement.textContent = '0';

&nbsp;       const interval = setInterval(() => {

&nbsp;           currentScore += 5;

&nbsp;           if (currentScore >= score) {

&nbsp;               currentScore = score;

&nbsp;               clearInterval(interval);

&nbsp;           }

&nbsp;           finalScoreElement.textContent = currentScore;

&nbsp;       }, 30);

&nbsp;   }



&nbsp;   function restartGame() {

&nbsp;       resultScreen.classList.add('hidden');

&nbsp;       startScreen.classList.remove('hidden');

&nbsp;       if (timerInterval) {

&nbsp;           clearInterval(timerInterval); // 確保重新開始時清除計時器

&nbsp;       }

&nbsp;   }

</script>



</body>

</html>



<html lang="zh-TW">

<head>

&nbsp;   <meta charset="UTF-8">

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

&nbsp;   <title>愛樂唯：騎士的拯救公主之旅 (計時挑戰)</title>

&nbsp;   <style>

&nbsp;       /\* CSS 樣式 \*/

&nbsp;       :root {

&nbsp;           --color-knight: #6a4c93; 

&nbsp;           --color-clear: #4ea8de; /\* 清 \*/

&nbsp;           --color-adjust: #f48c06; /\* 調 \*/

&nbsp;           --color-supplement: #2a9d8f; /\* 補 \*/

&nbsp;           --color-shape: #f72585; /\* 朔 \*/

&nbsp;           --color-bg: #f8f9fa;

&nbsp;           --color-text: #333;

&nbsp;           --color-timer: #ff5733; 

&nbsp;       }



&nbsp;       body {

&nbsp;           font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;

&nbsp;           background: linear-gradient(135deg, #a7e9af 0%, #47a0ff 100%);

&nbsp;           color: var(--color-text);

&nbsp;           display: flex;

&nbsp;           justify-content: center;

&nbsp;           align-items: center;

&nbsp;           min-height: 100vh;

&nbsp;           margin: 0;

&nbsp;           padding: 20px;

&nbsp;           box-sizing: border-box; 

&nbsp;       }



&nbsp;       .game-container {

&nbsp;           background: white;

&nbsp;           width: 100%;

&nbsp;           max-width: 700px;

&nbsp;           border-radius: 25px;

&nbsp;           box-shadow: 0 15px 35px rgba(0,0,0,0.2);

&nbsp;           overflow: hidden;

&nbsp;           position: relative;

&nbsp;       }



&nbsp;       .header {

&nbsp;           background: var(--color-knight);

&nbsp;           color: white;

&nbsp;           padding: 25px;

&nbsp;           text-align: center;

&nbsp;       }



&nbsp;       .header h1 { margin: 0; font-size: 1.8rem; }

&nbsp;       .header p { margin: 5px 0 0; opacity: 0.9; font-size: 1rem; }



&nbsp;       .progress-bar { height: 8px; background: #ddd; width: 100%; }

&nbsp;       

&nbsp;       .progress-fill {

&nbsp;           height: 100%;

&nbsp;           background: var(--color-shape);

&nbsp;           width: 0%;

&nbsp;           transition: width 0.4s ease;

&nbsp;       }



&nbsp;       .content {

&nbsp;           padding: 30px;

&nbsp;           text-align: center;

&nbsp;           min-height: 350px;

&nbsp;           display: flex;

&nbsp;           flex-direction: column;

&nbsp;           justify-content: center;

&nbsp;           align-items: center;

&nbsp;       }



&nbsp;       .btn {

&nbsp;           background: var(--color-knight);

&nbsp;           color: white;

&nbsp;           border: none;

&nbsp;           padding: 14px 28px;

&nbsp;           border-radius: 50px;

&nbsp;           font-size: 1.1rem;

&nbsp;           cursor: pointer;

&nbsp;           margin: 10px;

&nbsp;           transition: transform 0.1s, background 0.2s;

&nbsp;           width: 90%;

&nbsp;           max-width: 350px;

&nbsp;           font-weight: bold;

&nbsp;       }



&nbsp;       .btn:hover { transform: scale(1.03); background: #553c7a; }

&nbsp;       .btn:active { transform: scale(0.98); }



&nbsp;       .option-btn {

&nbsp;           background: var(--color-bg);

&nbsp;           color: var(--color-text);

&nbsp;           border: 2px solid #ddd;

&nbsp;           font-size: 1rem;

&nbsp;       }

&nbsp;       

&nbsp;       .option-btn:hover {

&nbsp;           border-color: var(--color-clear);

&nbsp;           background: #e6f7ff;

&nbsp;       }

&nbsp;       

&nbsp;       /\* 難度選擇按鈕樣式 \*/

&nbsp;       .difficulty-btn {

&nbsp;           background: #f0f0f0;

&nbsp;           color: #333;

&nbsp;           border: 2px solid #ccc;

&nbsp;           padding: 15px;

&nbsp;           margin: 10px;

&nbsp;           width: 80%;

&nbsp;           max-width: 300px;

&nbsp;           font-size: 1.1rem;

&nbsp;           font-weight: 600;

&nbsp;       }

&nbsp;       .difficulty-btn:hover {

&nbsp;           background: #fff;

&nbsp;           border-color: var(--color-knight);

&nbsp;           transform: scale(1.03);

&nbsp;       }



&nbsp;       /\* 倒計時顯示樣式 \*/

&nbsp;       #timerDisplay {

&nbsp;           font-size: 3rem;

&nbsp;           font-weight: 900;

&nbsp;           color: var(--color-timer);

&nbsp;           margin-bottom: 15px;

&nbsp;           min-height: 48px; 

&nbsp;       }

&nbsp;       

&nbsp;       /\* 其他樣式 \*/

&nbsp;       .level-badge {

&nbsp;           background: var(--color-shape);

&nbsp;           color: white;

&nbsp;           padding: 8px 20px;

&nbsp;           border-radius: 20px;

&nbsp;           font-size: 1rem;

&nbsp;           margin-bottom: 20px;

&nbsp;           display: inline-block;

&nbsp;           font-weight: bold;

&nbsp;           box-shadow: 0 4px 6px rgba(0,0,0,0.1);

&nbsp;       }

&nbsp;       .question-text {

&nbsp;           font-size: 1.35rem;

&nbsp;           margin-bottom: 30px;

&nbsp;           line-height: 1.6;

&nbsp;           font-weight: 500;

&nbsp;       }

&nbsp;       .product-image-placeholder {

&nbsp;           height: 120px;

&nbsp;           width: 120px;

&nbsp;           background: #eee;

&nbsp;           border-radius: 10px;

&nbsp;           margin-bottom: 20px;

&nbsp;           display: flex;

&nbsp;           flex-direction: column;

&nbsp;           align-items: center;

&nbsp;           justify-content: center;

&nbsp;           font-size: 0.8rem;

&nbsp;           color: #777;

&nbsp;           border: 1px dashed #ccc;

&nbsp;           text-align: center;

&nbsp;           padding: 5px;

&nbsp;       }

&nbsp;       .feedback {

&nbsp;           display: none;

&nbsp;           margin-top: 25px;

&nbsp;           padding: 20px;

&nbsp;           border-radius: 15px;

&nbsp;           text-align: left;

&nbsp;           width: 100%;

&nbsp;           max-width: 500px;

&nbsp;       }

&nbsp;       .feedback.correct { border: 2px solid var(--color-supplement); color: #006d5b; background: #e0f2f1; }

&nbsp;       .feedback.wrong { border: 2px solid var(--color-shape); color: #721c24; background: #f8d7da; }

&nbsp;       .result-score { font-size: 3.5rem; color: var(--color-knight); font-weight: 900; }

&nbsp;       .result-message { margin-bottom: 35px; color: #555; font-size: 1.1rem; }

&nbsp;       .character-display { font-size: 8rem; margin-bottom: 20px; line-height: 1; }

&nbsp;       .princess-initial { color: #8d4a41; } 

&nbsp;       .princess-final { color: #f72585; animation: pulse 1.5s infinite; } 

&nbsp;       @keyframes pulse {

&nbsp;           0% { transform: scale(1); opacity: 1; }

&nbsp;           50% { transform: scale(1.05); opacity: 0.8; }

&nbsp;           100% { transform: scale(1); opacity: 1; }

&nbsp;       }

&nbsp;       .hidden { display: none !important; }

&nbsp;       .fade-in { animation: fadeIn 0.5s; }

&nbsp;       @keyframes fadeIn {

&nbsp;           from { opacity: 0; transform: translateY(15px); }

&nbsp;           to { opacity: 1; transform: translateY(0); }

&nbsp;       }

&nbsp;   </style>

</head>

<body>



<div class="game-container">

&nbsp;   <div class="header">

&nbsp;       <h1>⚔️ 騎士的體內淨化之旅 👸</h1>

&nbsp;       <p>運用【清．調．補．朔】智慧，拯救平衡公主！</p>

&nbsp;   </div>

&nbsp;   

&nbsp;   <div class="progress-bar">

&nbsp;       <div class="progress-fill" id="progressFill"></div>

&nbsp;   </div>



&nbsp;   <div id="startScreen" class="content fade-in">

&nbsp;       <div class="character-display princess-initial">👸🏿</div>

&nbsp;       <h2>【亞健康公主】被困</h2>

&nbsp;       <p>請選擇您的挑戰難度，為公主奪回健康光彩！</p>

&nbsp;       <p style="font-weight: bold; color: var(--color-timer);">⏳ 作答時間：每題 15 秒</p>

&nbsp;       

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('easy')">

&nbsp;           簡單 (10 題 / 100 分) - 虹光之路

&nbsp;       </button>

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('medium')">

&nbsp;           挑戰 (15 題 / 150 分) - 極光之路

&nbsp;       </button>

&nbsp;       <button class="btn difficulty-btn" onclick="startGame('hard')">

&nbsp;           專業 (20 題 / 200 分) - 日光之路

&nbsp;       </button>

&nbsp;   </div>



&nbsp;   <div id="gameScreen" class="content hidden fade-in">

&nbsp;       <div id="timerDisplay">15</div>



&nbsp;       <div id="animationArea" class="character-display knight">⚔️</div>

&nbsp;       <span id="levelBadge" class="level-badge">關卡載入中...</span>

&nbsp;       

&nbsp;       <div id="productPlaceholder" class="product-image-placeholder">

&nbsp;           \[產品圖片佔位 - 可替換為產品圖 URL]

&nbsp;       </div>



&nbsp;       <div id="questionText" class="question-text">題目載入中...</div>

&nbsp;       <div id="optionsContainer" style="width: 100%; display: flex; flex-direction: column; align-items: center;">

&nbsp;           </div>

&nbsp;       

&nbsp;       <div id="feedbackArea" class="feedback">

&nbsp;           <h3 id="feedbackTitle" style="margin-top:0;"></h3>

&nbsp;           <p id="feedbackText" style="margin-bottom:0;"></p>

&nbsp;           <button class="btn" id="nextBtn" onclick="nextQuestion()" style="margin-top: 15px;">下一題</button>

&nbsp;       </div>

&nbsp;   </div>



&nbsp;   <div id="resultScreen" class="content hidden fade-in">

&nbsp;       <div id="finalCharacterDisplay" class="character-display princess-initial">👸🏿</div>

&nbsp;       <h2>闖關結果揭曉！</h2>

&nbsp;       <div class="result-score" id="finalScore">0</div>

&nbsp;       <p class="result-message" id="resultMessage">正在分析您的健康指數...</p>

&nbsp;       <button class="btn" onclick="restartGame()">再次挑戰</button>

&nbsp;   </div>

</div>



<script>

&nbsp;   // --- 配置常數 ---

&nbsp;   const TIMER\_LIMIT = 15; // 倒數計時改為 15 秒

&nbsp;   const MAX\_SCORE\_PER\_QUESTION = 10;



&nbsp;   // --- 難度配置 ---

&nbsp;   const difficultySettings = {

&nbsp;       'easy': {

&nbsp;           count: 10,

&nbsp;           titlePerfect: "愛樂唯虹光騎士",

&nbsp;           titleGreat: "愛樂唯知識家",

&nbsp;           draw: { 'clear': 3, 'adjust': 3, 'supplement': 2, 'shape': 1, 'final': 1 }

&nbsp;       },

&nbsp;       'medium': {

&nbsp;           count: 15,

&nbsp;           titlePerfect: "愛樂唯極光騎士",

&nbsp;           titleGreat: "愛樂唯菁英",

&nbsp;           draw: { 'clear': 4, 'adjust': 4, 'supplement': 4, 'shape': 2, 'final': 1 }

&nbsp;       },

&nbsp;       'hard': {

&nbsp;           count: 20,

&nbsp;           titlePerfect: "愛樂唯日光騎士",

&nbsp;           titleGreat: "愛樂唯專家",

&nbsp;           // 專業級：從每個分類多抽，確保總數達到 20 題

&nbsp;           draw: { 'clear': 5, 'adjust': 5, 'supplement': 6, 'shape': 2, 'final': 2 }

&nbsp;       }

&nbsp;   };

&nbsp;   // 範例：請在您的程式碼中找到類似的產品定義

&nbsp;   "PuraBio": {

&nbsp;       name: "澄熙益生菌 PurαBio",

&nbsp;       \[cite\_start]description: "17種益菌菌株為您及家人打造完美防護，維持消化道機能，改變細菌叢生態。", // \[cite: 58, 59] (根據您的文件)

&nbsp;       // 🚨 新增圖片路徑欄位

&nbsp;       image: "澄熙益生菌-DM-2.jpg" 

&nbsp;   },

&nbsp;   "Auro": {

&nbsp;       name: "極淨纖果粉 Auro α",

&nbsp;       \[cite\_start]description: "結合了草本植物、複合纖維和專利酵素，能讓排便順暢。", // \[cite: 32] (根據您的文件)

&nbsp;       // 🚨 新增圖片路徑欄位

&nbsp;       image: "極淨纖果粉DM-4.jpg" 

&nbsp;   },

&nbsp;   // 請依照此格式，將所有產品都加入對應的圖片檔名

&nbsp;   "Flora": {

&nbsp;       name: "亮妍嬌源飲 Florα",

&nbsp;       \[cite\_start]description: "彈力潤澤的青春肌密，一包蘊含5,000毫克膠原蛋白，專為30+以上設計配方。", // \[cite: 78, 79] (根據您的文件)

&nbsp;       image: "Adobe Express - file (1).png" 

&nbsp;   },

&nbsp;   "Eterna": {

&nbsp;       name: "恆芯營養粉 Eterna",

&nbsp;       \[cite\_start]description: "專為日常補養、熟齡保健打造的營養複方，提供「喝的營養照護方案」。", // \[cite: 115] (根據您的文件)

&nbsp;       image: "ALFAWISE\_網站恆芯-02-scaled.jpg" 

&nbsp;   },

&nbsp;   "Spark": {

&nbsp;       name: "閃朔蜜桃飲 Spαrk",

&nbsp;       \[cite\_start]description: "獨家代謝配方，激發身體潛能，加速新陳代謝，減少對食物的渴望。", // \[cite: 129] (根據您的文件)

&nbsp;       image: "閃朔蜜桃飲3.jpg" 

&nbsp;   },

&nbsp;   "DawnBliss": {

&nbsp;       name: "昕悅活力飲 DαwnBliss",

&nbsp;       \[cite\_start]description: "維持整天活力的美體飲品，蘊含花青素與維生素B，喚醒身體、調節機能。", // \[cite: 4] (根據您的文件)

&nbsp;       image: "Adobe Express - file (1).png" 

&nbsp;   }

};

&nbsp;   // --- 擴充的完整題目庫 (FULL QUESTION BANK) ---

&nbsp;   // 總共 20 題 (清x5, 調x5, 補x6, 朔x2, Final x2)

&nbsp;   const fullQuestionBank = {

&nbsp;       // --- Level 1: 清 (Auro + Down Bliss) --- 

&nbsp;       'clear': \[

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "宿便怪", animation: "🐛",

&nbsp;               question: "極淨纖果粉中，能幫助維持消化道機能的珍貴草本精華是？",

&nbsp;               options: \["綠咖啡", "望江南和決明子", "膠原蛋白", "維生素 C"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*望江南和決明子\*\*等草本精華幫助維持消化道機能，讓排便更順暢。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "積食怪", animation: "⚔️",

&nbsp;               question: "極淨纖果粉中，100%由非基因改造大豆做基底，能幫助營養素吸收的美國專利成分是什麼？",

&nbsp;               options: \["MBP 鈣結合蛋白", "藤黃果 HCA", "AES 綜合酵素", "L-茶胺酸"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*AES 綜合酵素\*\*能幫助營養素吸收，減少過度積食的負擔。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Auro 極淨纖果粉", enemy: "素食疑慮", animation: "🌿",

&nbsp;               question: "極淨纖果粉的素食屬性是屬於哪一類？",

&nbsp;               options: \["全素", "純素", "奶素", "蛋奶素"],

&nbsp;               correct: 2, explanation: "✅ 正確！極淨纖果粉為\*\*奶素\*\*，不適合全素食者。"

&nbsp;           },

&nbsp;           // \*\*更新題：昕悅活力飲 - 能量成分\*\*

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Down Bliss 昕悅活力飲", enemy: "精神不濟", animation: "☕",

&nbsp;               question: "昕悅活力飲中，被稱為「巴西國飲」且富含天然咖啡因，能滋補強身、增進效率的成分是？",

&nbsp;               options: \["綠茶萃取", "巴西瓜拿納果", "瑪卡", "薑黃素"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*巴西瓜拿納果\*\*能滋補強身、增強體力，富含天然咖啡因可增進效率。"

&nbsp;           },

&nbsp;           // \*\*新增題：昕悅活力飲 - 代謝成分\*\*

&nbsp;           {

&nbsp;               level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",

&nbsp;               product: "Down Bliss 昕悅活力飲", enemy: "代謝緩慢", animation: "🍊",

&nbsp;               question: "昕悅活力飲中，富含川陳皮素、橘紅素、辛弗林等，幫助促進新陳代謝，適合關注體態管理者的成分是什麼？",

&nbsp;               options: \["專利紅橙萃取", "專利柑橘幼果萃取", "專利黑胡椒萃取", "專利藤黃果萃取"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*專利柑橘幼果萃取\*\*富含川陳皮素、橘紅素、辛弗林等，有助於促進新陳代謝。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 2: 調 (PurBio) --- 

&nbsp;       'adjust': \[

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "搞怪軍團 (壞菌)", animation: "🦠",

&nbsp;               question: "PurBio 澄熙益生菌含有幾種具身分履歷的強大菌株，以全方位調整體質？",

&nbsp;               options: \["5 種", "10 種", "17 種", "25 種"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*17 種\*\*益菌戰隊能改變細菌叢生態，促進健康維持。"

&nbsp;           },

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "胃酸威脅", animation: "🛡️",

&nbsp;               question: "PurBio 澄熙益生菌採用的技術，目的是保護菌種能成功通過胃酸，提高定殖率，請問這是哪種技術？",

&nbsp;               options: \["冷凍乾燥技術", "微粒包覆技術", "超高溫瞬時滅菌", "天然發酵法"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*微粒包覆技術\*\*能保護菌種，讓益生菌精準送達腸道。"

&nbsp;           },

&nbsp;            {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "甜味誘惑", animation: "🍎",

&nbsp;               question: "澄熙益生菌的甜味主要來自哪種經美國 FDA 認定為 GRAS 等級的成分？",

&nbsp;               options: \["果寡糖", "木糖醇", "甜菊糖苷", "天然香料"],

&nbsp;               correct: 1, explanation: "✅ 正確！甜味主要來自於\*\*木糖醇\*\*與天然香料。木糖醇熱量低且被美國 FDA 認定為 GRAS 等級。"

&nbsp;           },

&nbsp;            {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "素食疑慮", animation: "🥦",

&nbsp;               question: "關於澄熙益生菌，哪項描述是正確的？",

&nbsp;               options: \["含有蛋奶製品", "為純素可食", "含有動物性成分", "為奶素食品"],

&nbsp;               correct: 1, explanation: "✅ 正確！澄熙益生菌不含動物性成分，不含蛋奶製品，為\*\*純素可食\*\*。"

&nbsp;           },

&nbsp;           // \*\*新增題：澄熙益生菌 - 用量\*\*

&nbsp;           {

&nbsp;               level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",

&nbsp;               product: "PurBio 澄熙益生菌", enemy: "用量困惑", animation: "🥄",

&nbsp;               question: "3歲以上兒童建議一天一包，請問成人建議量與加強建議量分別是多少？",

&nbsp;               options: \["成人：每日睡前 1 包；加強：每日睡前 2 包", "成人：每日三餐飯前 1 包；加強：每日三餐飯前 2 包", "成人：每日一餐飯後 1 包；加強：每日兩餐飯後 1 包", "成人：每日 2 包；加強：每日 3 包"],

&nbsp;               correct: 1, explanation: "✅ 正確！成人建議量為\*\*每日三餐飯前 1 包\*\*，加強建議量為\*\*每日三餐飯前 2 包\*\*。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 3: 補 (Flor + Etern) --- 

&nbsp;       'supplement': \[

&nbsp;           // Flor 亮妍嬌源飲 

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "乾燥細紋", animation: "💖",

&nbsp;               question: "亮妍嬌源飲中，一包蘊含多少毫克的魚膠原蛋白，並使用酵素水解技術提高吸收效率？",

&nbsp;               options: \["1,000 毫克", "5,000 毫克", "10,000 毫克", "2,500 毫克"],

&nbsp;               correct: 1, explanation: "✅ 正確！一包亮妍嬌源飲蘊含 \*\*5,000 毫克\*\*高品質魚膠原蛋白。"

&nbsp;           },

&nbsp;           // Etern 恆芯營養粉 

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "骨骼健康", animation: "🦴",

&nbsp;               question: "恆芯營養粉中，來自牛乳萃取物，能輔助維持骨骼健康的活性胜肽成分是什麼？",

&nbsp;               options: \["高鈣乳酪", "牛奶活性胜肽MBP", "酪梨大豆萃取物", "維生素 K2"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*牛奶活性胜肽MBP\*\*適合輔助日常營養補充與維持骨骼健康。"

&nbsp;           },

&nbsp;           // 亮妍嬌源飲

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "素顏不美", animation: "✨",

&nbsp;               question: "哪種專利益生菌，擁有 8 項專利與 3 篇期刊發表，是增添肌膚水潤與提升關鍵力的主要成分？",

&nbsp;               options: \["專利燕窩酸益生菌", "嗜酸乳桿菌", "專利自產玻尿酸益生菌 (嗜熱鏈球菌)", "比菲德氏菌"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*專利自產玻尿酸益生菌 (嗜熱鏈球菌)\*\* 榮獲國際發明展銀獎，能增添肌膚水潤與提升關鍵力。"

&nbsp;           },

&nbsp;           // 恆芯營養粉

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "營養不均", animation: "🏋️",

&nbsp;               question: "恆芯營養粉的優質「動植物雙蛋白」互補配方是？",

&nbsp;               options: \["酪蛋白＋豌豆蛋白", "乳清蛋白＋大豆蛋白＋白胺酸", "蛋清蛋白＋米蛋白", "魚膠原＋大豆蛋白"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*乳清蛋白＋大豆蛋白＋白胺酸\*\*組成的雙蛋白複方，提供優質營養，吸收佳且飽足久。"

&nbsp;           },

&nbsp;           // \*\*新增題：恆芯營養粉 - 草本成分\*\*

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Etern 恆芯營養粉", enemy: "行動力下降", animation: "🌿",

&nbsp;               question: "恆芯營養粉中，除了鈣和維生素外，還添加了哪兩種植物素材，有助於調節生理機能？",

&nbsp;               options: \["人參、靈芝", "枸杞、紅棗", "甘藷萃取物、穿心蓮", "薑黃、肉桂"],

&nbsp;               correct: 2, explanation: "✅ 正確！\*\*甘藷萃取物\*\*與\*\*穿心蓮\*\*是常見的植物素材，可協助維持健康、調整體質。"

&nbsp;           },

&nbsp;           // \*\*新增題：亮妍嬌源飲 - 甜味\*\*

&nbsp;           {

&nbsp;               level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",

&nbsp;               product: "Flor 亮妍嬌源飲", enemy: "甜食渴望", animation: "🍬",

&nbsp;               question: "亮妍嬌源飲的甜味來自哪種熱量低的代糖，被美國 FDA 認定為 GRAS (最高安全規格)？",

&nbsp;               options: \["阿斯巴甜", "甜菊糖苷", "蔗糖素", "果糖"],

&nbsp;               correct: 1, explanation: "✅ 正確！甜味來自於草本萃取的\*\*甜菊糖苷\*\*，甜度高熱量低，符合最高安全規格。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 4: 朔 (Spork) --- 

&nbsp;       'shape': \[

&nbsp;           {

&nbsp;               level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",

&nbsp;               product: "Spork 閃朔蜜桃飲", enemy: "體脂魔王", animation: "🔥",

&nbsp;               question: "閃朔蜜桃飲系列中，哪種成分含有豐富 HCA（羥基檸檬酸），能幫助消化並降低對食物的慾望？",

&nbsp;               options: \["綠咖啡萃取", "藤黃果萃取", "葡萄皮萃取", "兒茶素"],

&nbsp;               correct: 1, explanation: "✅ 正確！\*\*藤黃果萃取物\*\*含有豐富 HCA，是飲食管控的好幫手。"

&nbsp;           },

&nbsp;           // 朔奶茶飲

&nbsp;           {

&nbsp;               level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",

&nbsp;               product: "Spork 朔奶茶飲", enemy: "腹部堆積", animation: "☕",

&nbsp;               question: "朔奶茶飲中特有的哪種成分，具有調節生理機能、減少腹部堆積的功效？",

&nbsp;               options: \["綠咖啡萃取物", "藤黃果萃取物", "白藜蘆醇", "川芎萃取物"],

&nbsp;               correct: 3, explanation: "✅ 正確！\*\*川芎萃取物\*\*能調節生理機能，幫助身體輕盈不卡水。"

&nbsp;           }

&nbsp;       ],

&nbsp;       // --- Level 5: 最終智慧 (餐量管理) --- 

&nbsp;       'final': \[

&nbsp;            // \*\*修正後的題目 (原遺漏逗號)\*\*

&nbsp;            {

&nbsp;               level: "最終關：大師的智慧", levelColor: "var(--color-knight)",

&nbsp;               product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🧘",

&nbsp;               question: "愛樂唯餐量管理理念的核心口訣是「吃肉肉減肉肉．喝神飲減肉肉．\_\_\_\_\_\_\_\_\_\_\_\_」？",

&nbsp;               options: \["多運動減肉肉", "不用動減肉肉", "少吃澱粉減肉肉", "不吃肉減肉肉"],

&nbsp;               correct: 1, explanation: "✅ 正確！愛樂唯餐量管理口訣為：\*\*吃肉肉減肉肉．喝神飲減肉肉．不用動減肉肉\*\*。"

&nbsp;           }, // <--- 關鍵修復：這裡補上了逗號 (,)

&nbsp;           {

&nbsp;               level: "最終關：大師的智慧", levelColor: "var(--color-knight)",

&nbsp;               product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🍽️",

&nbsp;               question: "愛樂唯餐量管理的目標是把健康變簡單，請問下列哪一項是其中關鍵理念？",

&nbsp;               options: \["多樣化的產品線", "產品簡單化更能融入生活", "專注於單一功能", "強調複雜的營養學"],

&nbsp;               correct: 1, explanation: "✅ 正確！產品簡單化更能融入生活，讓忙碌的生活也能輕鬆維持健康。" 

&nbsp;           }

&nbsp;       ]

&nbsp;   };



&nbsp;   let currentQuestions = \[]; 

&nbsp;   let currentQuestionIndex = 0;

&nbsp;   let score = 0;

&nbsp;   let isAnswering = false;

&nbsp;   let timerInterval = null; 

&nbsp;   let hasAnswered = false; 

&nbsp;   let selectedDifficulty = null; 

&nbsp;   let maxGameScore = 0; 



&nbsp;   // DOM Elements

&nbsp;   const startScreen = document.getElementById('startScreen');

&nbsp;   const gameScreen = document.getElementById('gameScreen');

&nbsp;   const resultScreen = document.getElementById('resultScreen');

&nbsp;   const questionText = document.getElementById('questionText');

&nbsp;   const optionsContainer = document.getElementById('optionsContainer');

&nbsp;   const levelBadge = document.getElementById('levelBadge');

&nbsp;   const feedbackArea = document.getElementById('feedbackArea');

&nbsp;   const feedbackTitle = document.getElementById('feedbackTitle');

&nbsp;   const feedbackText = document.getElementById('feedbackText');

&nbsp;   const nextBtn = document.getElementById('nextBtn');

&nbsp;   const progressFill = document.getElementById('progressFill');

&nbsp;   const productPlaceholder = document.getElementById('productPlaceholder');

&nbsp;   const animationArea = document.getElementById('animationArea');

&nbsp;   const timerDisplay = document.getElementById('timerDisplay'); 





&nbsp;   // --- 輔助函式：陣列隨機洗牌 ---

&nbsp;   function shuffleArray(array) {

&nbsp;       for (let i = array.length - 1; i > 0; i--) {

&nbsp;           const j = Math.floor(Math.random() \* (i + 1));

&nbsp;           let temp = array\[i];

&nbsp;           array\[i] = array\[j];

&nbsp;           array\[j] = temp;

&nbsp;       }

&nbsp;       return array;

&nbsp;   }



&nbsp;   // --- 倒計時邏輯 ---

&nbsp;   function startTimer() {

&nbsp;       let timeLeft = TIMER\_LIMIT;

&nbsp;       timerDisplay.textContent = timeLeft;

&nbsp;       timerDisplay.style.color = 'var(--color-timer)';

&nbsp;       

&nbsp;       timerInterval = setInterval(() => {

&nbsp;           timeLeft--;

&nbsp;           timerDisplay.textContent = timeLeft;



&nbsp;           if (timeLeft <= 5) {

&nbsp;               // 剩下 5 秒開始變紅色警示

&nbsp;               timerDisplay.style.color = '#ff0000';

&nbsp;           } else if (timeLeft <= 10) {

&nbsp;                // 剩下 10 秒變黃色警示

&nbsp;               timerDisplay.style.color = 'var(--color-adjust)';

&nbsp;           }





&nbsp;           if (timeLeft <= 0) {

&nbsp;               clearInterval(timerInterval);

&nbsp;               timerDisplay.textContent = '時間到！';

&nbsp;               // 如果時間到還沒作答，強制執行 checkAnswer (傳入 -1 代表未作答)

&nbsp;               if (!hasAnswered) {

&nbsp;                   checkAnswer(-1); 

&nbsp;               }

&nbsp;           }

&nbsp;       }, 1000); // 每秒執行

&nbsp;   }



&nbsp;   // --- 核心變動：根據難度選擇抽取題目並開始遊戲 ---

&nbsp;   function startGame(difficulty) {

&nbsp;       selectedDifficulty = difficulty;

&nbsp;       const settings = difficultySettings\[difficulty];

&nbsp;       

&nbsp;       // 畫面切換

&nbsp;       startScreen.classList.add('hidden');

&nbsp;       gameScreen.classList.remove('hidden');

&nbsp;       

&nbsp;       currentQuestionIndex = 0;

&nbsp;       score = 0;

&nbsp;       currentQuestions = \[]; 

&nbsp;       maxGameScore = settings.count \* MAX\_SCORE\_PER\_QUESTION;



&nbsp;       // 1. 根據難度設定，從每個主題庫中隨機抽取題目

&nbsp;       const drawCounts = settings.draw;

&nbsp;       

&nbsp;       for (const key in drawCounts) {

&nbsp;           const count = drawCounts\[key];

&nbsp;           const shuffledBank = shuffleArray(\[...fullQuestionBank\[key]]); 

&nbsp;           currentQuestions.push(...shuffledBank.slice(0, count)); 

&nbsp;       }

&nbsp;       

&nbsp;       // 確保總題庫的順序是隨機的

&nbsp;       currentQuestions = shuffleArray(currentQuestions);





&nbsp;       // 2. 隨機洗牌選項

&nbsp;       currentQuestions = currentQuestions.map(q => {

&nbsp;           const originalOptions = q.options;

&nbsp;           const correctText = originalOptions\[q.correct];

&nbsp;           

&nbsp;           const newOptions = shuffleArray(\[...originalOptions]);

&nbsp;           const newCorrectIndex = newOptions.indexOf(correctText);



&nbsp;           return {

&nbsp;               ...q,

&nbsp;               options: newOptions,

&nbsp;               correct: newCorrectIndex

&nbsp;           };

&nbsp;       });



&nbsp;       showQuestion();

&nbsp;   }

&nbsp;   

&nbsp;   // --- 顯示題目 ---

&nbsp;   function showQuestion() {

&nbsp;       isAnswering = true;

&nbsp;       hasAnswered = false; // 重設作答狀態

&nbsp;       feedbackArea.style.display = 'none';

&nbsp;       

&nbsp;       const buttons = optionsContainer.querySelectorAll('button');

&nbsp;       buttons.forEach(btn => btn.remove());

&nbsp;       

&nbsp;       // 清除前一題的計時器 (如果有)

&nbsp;       if (timerInterval) {

&nbsp;           clearInterval(timerInterval);

&nbsp;       }



&nbsp;       const q = currentQuestions\[currentQuestionIndex]; 

&nbsp;       

&nbsp;       // 動態更新 UI

&nbsp;       levelBadge.textContent = `${q.level} (第 ${currentQuestionIndex + 1} 題 / 共 ${currentQuestions.length} 題)`;

&nbsp;       levelBadge.style.backgroundColor = q.levelColor;

&nbsp;       questionText.textContent = q.question;

&nbsp;       

&nbsp;       animationArea.textContent = q.animation;

&nbsp;       // 產品圖片佔位符，顯示產品名稱和敵人

&nbsp;       productPlaceholder.innerHTML = `<div style="font-size: 0.9rem; font-weight: bold; color: ${q.levelColor};">${q.product}</div><div style="font-size: 0.7rem; color: #777;">(敵人/問題點: ${q.enemy})</div>`;

&nbsp;       

&nbsp;       // 更新進度條

&nbsp;       const progress = (currentQuestionIndex / currentQuestions.length) \* 100;

&nbsp;       progressFill.style.width = `${progress}%`;



&nbsp;       // 渲染選項

&nbsp;       optionsContainer.innerHTML = '';

&nbsp;       q.options.forEach((opt, index) => {

&nbsp;           const btn = document.createElement('button');

&nbsp;           btn.className = 'btn option-btn fade-in';

&nbsp;           btn.textContent = opt;

&nbsp;           btn.onclick = () => checkAnswer(index);

&nbsp;           optionsContainer.appendChild(btn);

&nbsp;       });



&nbsp;       // 啟動計時器

&nbsp;       startTimer();

&nbsp;   }



&nbsp;   // --- 檢查答案 (處理時間到未作答) ---

&nbsp;   function checkAnswer(selectedIndex) {

&nbsp;       if (!isAnswering \&\& selectedIndex !== -1) return; 

&nbsp;       if (hasAnswered \&\& selectedIndex !== -1) return;



&nbsp;       // 立即停止計時器

&nbsp;       clearInterval(timerInterval);

&nbsp;       isAnswering = false;

&nbsp;       hasAnswered = true;



&nbsp;       const q = currentQuestions\[currentQuestionIndex];

&nbsp;       const isCorrect = selectedIndex === q.correct;

&nbsp;       

&nbsp;       // 如果是時間到且未作答

&nbsp;       if (selectedIndex === -1) {

&nbsp;            feedbackTitle.textContent = `⏰ 時間到！`;

&nbsp;            feedbackText.innerHTML = `<strong>遺憾！</strong>您未能在 ${TIMER\_LIMIT} 秒內作答，本題不計分。正確答案是：${q.options\[q.correct]}`;

&nbsp;            feedbackArea.className = `feedback wrong fade-in`;

&nbsp;       } else {

&nbsp;           // 正常作答

&nbsp;           const buttons = optionsContainer.querySelectorAll('button');

&nbsp;           buttons.forEach((btn, idx) => {

&nbsp;               btn.disabled = true; // 禁用所有按鈕

&nbsp;               if (idx === q.correct) {

&nbsp;                   btn.style.backgroundColor = 'var(--color-supplement)'; 

&nbsp;                   btn.style.color = 'white';

&nbsp;               } else if (idx === selectedIndex \&\& !isCorrect) {

&nbsp;                   btn.style.backgroundColor = 'var(--color-shape)'; 

&nbsp;                   btn.style.color = 'white';

&nbsp;               } else {

&nbsp;                   btn.style.opacity = '0.5';

&nbsp;               }

&nbsp;           });



&nbsp;           feedbackArea.style.display = 'block';

&nbsp;           feedbackArea.className = `feedback ${isCorrect ? 'correct' : 'wrong'} fade-in`;

&nbsp;           feedbackTitle.textContent = isCorrect ? `🎉 成功！騎士擊敗了 ${q.enemy}` : `💥 失誤！ ${q.enemy} 暫時擋住了去路`;

&nbsp;           

&nbsp;           if (isCorrect) {

&nbsp;               score += MAX\_SCORE\_PER\_QUESTION;

&nbsp;               feedbackText.innerHTML = `<strong>知識解析：</strong> ${q.explanation}`;

&nbsp;           } else {

&nbsp;               feedbackText.innerHTML = `<strong>錯誤解析：</strong> 答案是 \*\*${q.options\[q.correct]}\*\*。<br>${q.explanation}`;

&nbsp;           }

&nbsp;       }

&nbsp;       

&nbsp;       // 確保結果顯示

&nbsp;       feedbackArea.style.display = 'block';



&nbsp;       if (currentQuestionIndex === currentQuestions.length - 1) {

&nbsp;           nextBtn.textContent = "拯救公主 (查看結果)";

&nbsp;       } else {

&nbsp;           nextBtn.textContent = "繼續前進";

&nbsp;       }

&nbsp;   }



&nbsp;   function nextQuestion() {

&nbsp;       currentQuestionIndex++;

&nbsp;       if (currentQuestionIndex < currentQuestions.length) {

&nbsp;           showQuestion();

&nbsp;       } else {

&nbsp;           showResult();

&nbsp;       }

&nbsp;   }



&nbsp;   function showResult() {

&nbsp;       gameScreen.classList.add('hidden');

&nbsp;       resultScreen.classList.remove('hidden');

&nbsp;       

&nbsp;       const settings = difficultySettings\[selectedDifficulty];

&nbsp;       const finalScoreElement = document.getElementById('finalScore');

&nbsp;       const resultMessage = document.getElementById('resultMessage');

&nbsp;       const finalCharacterDisplay = document.getElementById('finalCharacterDisplay');

&nbsp;       

&nbsp;       progressFill.style.width = '100%';



&nbsp;       let title = '';

&nbsp;       // 滿分 (100%)

&nbsp;       if (score === maxGameScore) {

&nbsp;           title = settings.titlePerfect;

&nbsp;           finalCharacterDisplay.textContent = '👸🏼'; 

&nbsp;           finalCharacterDisplay.className = 'character-display princess-final fade-in';

&nbsp;           resultMessage.innerHTML = `恭喜！您以 \*\*${maxGameScore} 分\*\* 滿分，獲得<br>【\*\*${title}\*\*】稱號！公主已恢復光彩！`;

&nbsp;       } 

&nbsp;       // 高分 (≥ 70%)

&nbsp;       else if (score >= maxGameScore \* 0.7) {

&nbsp;           title = settings.titleGreat;

&nbsp;           finalCharacterDisplay.textContent = '👸🏽';

&nbsp;           finalCharacterDisplay.className = 'character-display princess-initial fade-in';

&nbsp;           resultMessage.innerHTML = `表現優異！您獲得【\*\*${title}\*\*】稱號！<br>最終得分：${score} 分，公主正在好轉中！`;

&nbsp;       } 

&nbsp;       // 及格以下 (< 70%)

&nbsp;       else {

&nbsp;           title = "養生學徒";

&nbsp;           finalCharacterDisplay.textContent = '👸🏿';

&nbsp;           finalCharacterDisplay.className = 'character-display princess-initial fade-in';

&nbsp;           resultMessage.innerHTML = `您是【\*\*${title}\*\*】，知識還需磨練！<br>最終得分：${score} 分，公主狀態有改善，但仍需努力！`;

&nbsp;       }



&nbsp;       // 分數動畫

&nbsp;       let currentScore = 0;

&nbsp;       finalScoreElement.textContent = '0';

&nbsp;       const interval = setInterval(() => {

&nbsp;           currentScore += 5;

&nbsp;           if (currentScore >= score) {

&nbsp;               currentScore = score;

&nbsp;               clearInterval(interval);

&nbsp;           }

&nbsp;           finalScoreElement.textContent = currentScore;

&nbsp;       }, 30);

&nbsp;   }



&nbsp;   function restartGame() {

&nbsp;       resultScreen.classList.add('hidden');

&nbsp;       startScreen.classList.remove('hidden');

&nbsp;       if (timerInterval) {

&nbsp;           clearInterval(timerInterval); // 確保重新開始時清除計時器

&nbsp;       }

&nbsp;   }

</script>



</body>

</html>



