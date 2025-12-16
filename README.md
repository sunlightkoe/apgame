<!公主怎麼了?快來拯救她!>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>愛樂唯：騎士的體內淨化之旅 (計時挑戰)</title>
    <style>
        /* CSS 樣式 */
        :root {
            --color-knight: #6a4c93; 
            --color-clear: #4ea8de; /* 清 */
            --color-adjust: #f48c06; /* 調 */
            --color-supplement: #2a9d8f; /* 補 */
            --color-shape: #f72585; /* 朔 */
            --color-bg: #f8f9fa;
            --color-text: #333;
            --color-timer: #ff5733; 
        }

        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, #a7e9af 0%, #47a0ff 100%);
            color: var(--color-text);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            box-sizing: border-box; 
        }

        .game-container {
            background: white;
            width: 100%;
            max-width: 700px;
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
            overflow: hidden;
            position: relative;
        }

        .header {
            background: var(--color-knight);
            color: white;
            padding: 25px;
            text-align: center;
        }

        .header h1 { margin: 0; font-size: 1.8rem; }
        .header p { margin: 5px 0 0; opacity: 0.9; font-size: 1rem; }

        .progress-bar { height: 8px; background: #ddd; width: 100%; }
        
        .progress-fill {
            height: 100%;
            background: var(--color-shape);
            width: 0%;
            transition: width 0.4s ease;
        }

        .content {
            padding: 30px;
            text-align: center;
            min-height: 350px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .btn {
            background: var(--color-knight);
            color: white;
            border: none;
            padding: 14px 28px;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            margin: 10px;
            transition: transform 0.1s, background 0.2s;
            width: 90%;
            max-width: 350px;
            font-weight: bold;
        }

        .btn:hover { transform: scale(1.03); background: #553c7a; }
        .btn:active { transform: scale(0.98); }

        .option-btn {
            background: var(--color-bg);
            color: var(--color-text);
            border: 2px solid #ddd;
            font-size: 1rem;
        }
        
        .option-btn:hover {
            border-color: var(--color-clear);
            background: #e6f7ff;
        }
        
        /* 難度選擇按鈕樣式 */
        .difficulty-btn {
            background: #f0f0f0;
            color: #333;
            border: 2px solid #ccc;
            padding: 15px;
            margin: 10px;
            width: 80%;
            max-width: 300px;
            font-size: 1.1rem;
            font-weight: 600;
        }
        .difficulty-btn:hover {
            background: #fff;
            border-color: var(--color-knight);
            transform: scale(1.03);
        }

        /* 倒計時顯示樣式 */
        #timerDisplay {
            font-size: 3rem;
            font-weight: 900;
            color: var(--color-timer);
            margin-bottom: 15px;
            min-height: 48px; 
        }
        
        /* 其他樣式 */
        .level-badge {
            background: var(--color-shape);
            color: white;
            padding: 8px 20px;
            border-radius: 20px;
            font-size: 1rem;
            margin-bottom: 20px;
            display: inline-block;
            font-weight: bold;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .question-text {
            font-size: 1.35rem;
            margin-bottom: 30px;
            line-height: 1.6;
            font-weight: 500;
        }
        /* 圖片和敵人資訊的容器樣式 */
        .question-info {
            display: flex;
            flex-wrap: wrap; /* 允許在小螢幕上換行 */
            justify-content: center;
            align-items: center;
            width: 100%;
            margin-bottom: 20px;
            gap: 20px; 
        }
        
        /* 圖片佔位符樣式 */
        #productPlaceholder {
            height: auto;
            width: auto;
            max-width: 150px; 
            max-height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        #productPlaceholder img {
            max-width: 100%;
            max-height: 150px;
            border-radius: 8px;
            object-fit: contain; 
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .enemy-placeholder {
            min-width: 120px;
            text-align: left;
            padding: 10px;
            border-left: 2px solid #eee;
        }
        .enemy-placeholder div {
            font-size: 1.1rem;
            font-weight: bold;
            color: var(--color-knight);
        }
        .enemy-placeholder span {
            font-size: 0.9rem;
            color: #777;
            font-weight: 600;
        }
        
        .feedback {
            display: none;
            margin-top: 25px;
            padding: 20px;
            border-radius: 15px;
            text-align: left;
            width: 100%;
            max-width: 500px;
        }
        .feedback.correct { border: 2px solid var(--color-supplement); color: #006d5b; background: #e0f2f1; }
        .feedback.wrong { border: 2px solid var(--color-shape); color: #721c24; background: #f8d7da; }
        .result-score { font-size: 3.5rem; color: var(--color-knight); font-weight: 900; }
        .result-message { margin-bottom: 35px; color: #555; font-size: 1.1rem; }
        .character-display { font-size: 8rem; margin-bottom: 20px; line-height: 1; }
        .princess-initial { color: #8d4a41; } 
        .princess-final { color: #f72585; animation: pulse 1.5s infinite; } 
        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.05); opacity: 0.8; }
            100% { transform: scale(1); opacity: 1; }
        }
        .hidden { display: none !important; }
        .fade-in { animation: fadeIn 0.5s; }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* 響應式調整 */
        @media (max-width: 600px) {
            .question-info {
                flex-direction: column; /* 小螢幕下圖片和文字垂直排列 */
                gap: 15px;
            }
            .enemy-placeholder {
                border-left: none; /* 移除垂直分隔線 */
                border-top: 2px solid #eee; /* 改為水平分隔線 */
                padding-top: 15px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

<div class="game-container">
    <div class="header">
        <h1>⚔️ 騎士的體內淨化之旅 👸</h1>
        <p>運用【清．調．補．朔】智慧，拯救平衡公主！</p>
    </div>
    
    <div class="progress-bar">
        <div class="progress-fill" id="progressFill"></div>
    </div>

    <div id="startScreen" class="content fade-in">
        <div class="character-display princess-initial">👸🏿</div>
        <h2>【亞健康公主】被困</h2>
        <p>請選擇您的挑戰難度，為公主奪回健康光彩！</p>
        <p style="font-weight: bold; color: var(--color-timer);">⏳ 作答時間：每題 15 秒</p>
        
        <button class="btn difficulty-btn" onclick="startGame('easy')">
            簡單 (10 題 / 100 分) - 虹光之路
        </button>
        <button class="btn difficulty-btn" onclick="startGame('medium')">
            挑戰 (15 題 / 150 分) - 極光之路
        </button>
        <button class="btn difficulty-btn" onclick="startGame('hard')">
            專業 (20 題 / 200 分) - 日光之路
        </button>
    </div>

    <div id="gameScreen" class="content hidden fade-in">
        <div id="timerDisplay">15</div>

        <div id="animationArea" class="character-display knight">⚔️</div>
        <span id="levelBadge" class="level-badge">關卡載入中...</span>
        
        <div class="question-info">
            <div id="productPlaceholder">
                </div>
            <div id="enemyPlaceholder" class="enemy-placeholder">
                </div>
        </div>
        <div id="questionText" class="question-text">題目載入中...</div>
        <div id="optionsContainer" style="width: 100%; display: flex; flex-direction: column; align-items: center;">
            </div>
        
        <div id="feedbackArea" class="feedback">
            <h3 id="feedbackTitle" style="margin-top:0;"></h3>
            <p id="feedbackText" style="margin-bottom:0;"></p>
            <button class="btn" id="nextBtn" onclick="nextQuestion()" style="margin-top: 15px;">下一題</button>
        </div>
    </div>

    <div id="resultScreen" class="content hidden fade-in">
        <div id="finalCharacterDisplay" class="character-display princess-initial">👸🏿</div>
        <h2>闖關結果揭曉！</h2>
        <div class="result-score" id="finalScore">0</div>
        <p class="result-message" id="resultMessage">正在分析您的健康指數...</p>
        <button class="btn" onclick="restartGame()">再次挑戰</button>
    </div>
</div>

<script>
    // --- 配置常數 ---
    const TIMER_LIMIT = 15; 
    const MAX_SCORE_PER_QUESTION = 10;

    // --- 難度配置 ---
    const difficultySettings = {
        'easy': {
            count: 10,
            titlePerfect: "愛樂唯虹光騎士",
            titleGreat: "愛樂唯知識家",
            draw: { 'clear': 3, 'adjust': 3, 'supplement': 2, 'shape': 1, 'final': 1 }
        },
        'medium': {
            count: 15,
            titlePerfect: "愛樂唯極光騎士",
            titleGreat: "愛樂唯菁英",
            draw: { 'clear': 4, 'adjust': 4, 'supplement': 4, 'shape': 2, 'final': 1 }
        },
        'hard': {
            count: 20,
            titlePerfect: "愛樂唯日光騎士",
            titleGreat: "愛樂唯專家",
            draw: { 'clear': 5, 'adjust': 5, 'supplement': 6, 'shape': 2, 'final': 2 }
        }
    };

    // --- 擴充的完整題目庫 (FULL QUESTION BANK) 🚨 已更新產品名稱 ---
    const fullQuestionBank = {
        // --- Level 1: 清 (Auro + Down Bliss) --- 
        'clear': [
            {
                level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",
                product: "Auro 極淨纖果粉", enemy: "宿便怪", animation: "🐛",
                imageFile: "clear2.Jpg", 
                question: "極淨纖果粉中，能幫助維持消化道機能的珍貴草本精華是？",
                options: ["綠咖啡", "望江南和決明子", "膠原蛋白", "維生素 C"],
                correct: 1, explanation: "✅ 正確！**望江南和決明子**等草本精華幫助維持消化道機能，讓排便更順暢。"
            },
            {
                level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",
                product: "Auro 極淨纖果粉", enemy: "積食怪", animation: "⚔️",
                imageFile: "clear2.Jpg", 
                question: "極淨纖果粉中，100%由非基因改造大豆做基底，能幫助營養素吸收的美國專利成分是什麼？",
                options: ["MBP 鈣結合蛋白", "藤黃果 HCA", "AES 綜合酵素", "L-茶胺酸"],
                correct: 2, explanation: "✅ 正確！**AES 綜合酵素**能幫助營養素吸收，減少過度積食的負擔。"
            },
            {
                level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",
                product: "Auro 極淨纖果粉", enemy: "素食疑慮", animation: "🌿",
                imageFile: "clear2.Jpg", 
                question: "極淨纖果粉的素食屬性是屬於哪一類？",
                options: ["全素", "純素", "奶素", "蛋奶素"],
                correct: 2, explanation: "✅ 正確！極淨纖果粉為**奶素**，不適合全素食者。"
            },
            {
                level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",
                product: "Down Bliss 昕悅活力飲", enemy: "精神不濟", animation: "☕",
                imageFile: "clear1.Jpg", 
                question: "昕悅活力飲中，被稱為「巴西國飲」且富含天然咖啡因，能滋補強身、增進效率的成分是？",
                options: ["綠茶萃取", "巴西瓜拿納果", "瑪卡", "薑黃素"],
                correct: 1, explanation: "✅ 正確！**巴西瓜拿納果**能滋補強身、增強體力，富含天然咖啡因可增進效率。"
            },
            {
                level: "第一關：淨化森林 (清)", levelColor: "var(--color-clear)",
                product: "Down Bliss 昕悅活力飲", enemy: "代謝緩慢", animation: "🍊",
                imageFile: "clear1.Jpg", 
                question: "昕悅活力飲中，富含川陳皮素、橘紅素、辛弗林等，幫助促進新陳代謝，適合關注體態管理者的成分是什麼？",
                options: ["專利紅橙萃取", "專利柑橘幼果萃取", "專利黑胡椒萃取", "專利藤黃果萃取"],
                correct: 1, explanation: "✅ 正確！**專利柑橘幼果萃取**富含川陳皮素、橘紅素、辛弗林等，有助於促進新陳代謝，適合關注體態管理者使用。"
            }
        ],
        // --- Level 2: 調 (PurBio) --- 
        'adjust': [
            {
                level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",
                product: "PurBio 澄熙益生菌", enemy: "搞怪軍團 (壞菌)", animation: "🦠",
                imageFile: "adjust.Jpg", 
                question: "PurBio 澄熙益生菌含有幾種具身分履歷的強大菌株，以全方位調整體質？",
                options: ["5 種", "10 種", "17 種", "25 種"],
                correct: 2, explanation: "✅ 正確！**17 種**益菌戰隊能改變細菌叢生態，促進健康維持。"
            },
            {
                level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",
                product: "PurBio 澄熙益生菌", enemy: "胃酸威脅", animation: "🛡️",
                imageFile: "adjust.Jpg", 
                question: "PurBio 澄熙益生菌採用的技術，目的是保護菌種能成功通過胃酸，提高定殖率，請問這是哪種技術？",
                options: ["冷凍乾燥技術", "微粒包覆技術", "超高溫瞬時滅菌", "天然發酵法"],
                correct: 1, explanation: "✅ 正確！**微粒包覆技術**能保護菌種，讓益生菌精準送達腸道。"
            },
             {
                level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",
                product: "PurBio 澄熙益生菌", enemy: "甜味誘惑", animation: "🍎",
                imageFile: "adjust.Jpg", 
                question: "澄熙益生菌的甜味主要來自哪種經美國 FDA 認定為 GRAS 等級的成分？",
                options: ["果寡糖", "木糖醇", "甜菊糖苷", "天然香料"],
                correct: 1, explanation: "✅ 正確！甜味主要來自於**木糖醇**與天然香料。木糖醇熱量低且被美國 FDA 認定為 GRAS 等級。"
            },
             {
                level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",
                product: "PurBio 澄熙益生菌", enemy: "素食疑慮", animation: "🥦",
                imageFile: "adjust.Jpg", 
                question: "關於澄熙益生菌，哪項描述是正確的？",
                options: ["含有蛋奶製品", "為純素可食", "含有動物性成分", "為奶素食品"],
                correct: 1, explanation: "✅ 正確！澄熙益生菌不含動物性成分，不含蛋奶製品，為**純素可食**。"
            },
            {
                level: "第二關：平衡花園 (調)", levelColor: "var(--color-adjust)",
                product: "PurBio 澄熙益生菌", enemy: "用量困惑", animation: "🥄",
                imageFile: "adjust.Jpg", 
                question: "3歲以上兒童建議一天一包，請問成人建議量與加強建議量分別是多少？",
                options: ["成人：每日睡前 1 包；加強：每日睡前 2 包", "成人：每日三餐飯前 1 包；加強：每日三餐飯前 2 包", "成人：每日一餐飯後 1 包；加強：每日兩餐飯後 1 包", "成人：每日 2 包；加強：每日 3 包"],
                correct: 1, explanation: "✅ 正確！成人建議量為**每日三餐飯前 1 包**，加強建議量為**每日三餐飯前 2 包**。"
            }
        ],
        // --- Level 3: 補 (Flor + Etern) --- 
        'supplement': [
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Flor 亮妍嬌源飲", enemy: "乾燥細紋", animation: "💖",
                imageFile: "supplement1.Jpg", 
                question: "亮妍嬌源飲中，一包蘊含多少毫克的魚膠原蛋白，並使用酵素水解技術提高吸收效率？",
                options: ["1,000 毫克", "5,000 毫克", "10,000 毫克", "2,500 毫克"],
                correct: 1, explanation: "✅ 正確！一包亮妍嬌源飲蘊含 **5,000 毫克**高品質魚膠原蛋白，運用酵素水解技術提高身體吸收效率。"
            },
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Etern 恆芯營養粉", enemy: "骨骼健康", animation: "🦴",
                imageFile: "supplement2.Jpg", 
                question: "恆芯營養粉中，來自牛乳萃取物，能輔助維持骨骼健康的活性胜肽成分是什麼？",
                options: ["高鈣乳酪", "牛奶活性胜肽MBP", "酪梨大豆萃取物", "維生素 K2"],
                correct: 1, explanation: "✅ 正確！**牛奶活性胜肽MBP**適合輔助日常營養補充與維持骨骼健康。"
            },
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Flor 亮妍嬌源飲", enemy: "素顏不美", animation: "✨",
                imageFile: "supplement1.Jpg", 
                question: "哪種專利益生菌，擁有 8 項專利與 3 篇期刊發表，是增添肌膚水潤與提升關鍵力的主要成分？",
                options: ["專利燕窩酸益生菌", "專利自產玻尿酸益生菌 (嗜熱鏈球菌)", "嗜酸乳桿菌", "比菲德氏菌"],
                correct: 1, explanation: "✅ 正確！**專利自產玻尿酸益生菌 (嗜熱鏈球菌)** 榮獲國際發明展銀獎，能增添肌膚水潤與提升關鍵力。"
            },
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Etern 恆芯營養粉", enemy: "營養不均", animation: "🏋️",
                imageFile: "supplement2.Jpg", 
                question: "恆芯營養粉的優質「動植物雙蛋白」互補配方是？",
                options: ["酪蛋白＋豌豆蛋白", "乳清蛋白＋大豆蛋白＋白胺酸", "蛋清蛋白＋米蛋白", "魚膠原＋大豆蛋白"],
                correct: 1, explanation: "✅ 正確！**乳清蛋白＋大豆蛋白＋白胺酸**組成的雙蛋白複方，提供優質營養，吸收佳且飽足久。"
            },
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Etern 恆芯營養粉", enemy: "行動力下降", animation: "🌿",
                imageFile: "supplement2.Jpg", 
                question: "恆芯營養粉中，除了鈣和維生素外，還添加了哪兩種植物素材，有助於調節生理機能？",
                options: ["人參、靈芝", "甘藷萃取物、穿心蓮", "枸杞、紅棗", "薑黃、肉桂"],
                correct: 1, explanation: "✅ 正確！**甘藷萃取物**與**穿心蓮**可協助維持健康、調整體質。"
            },
            {
                level: "第三關：能量泉源 (補)", levelColor: "var(--color-supplement)",
                product: "Flor 亮妍嬌源飲", enemy: "甜食渴望", animation: "🍬",
                imageFile: "supplement1.Jpg", 
                question: "亮妍嬌源飲的甜味來自哪種熱量低的代糖，被美國 FDA 認定為 GRAS (最高安全規格)？",
                options: ["阿斯巴甜", "甜菊糖苷", "蔗糖素", "果糖"],
                correct: 1, explanation: "✅ 正確！甜味來自於草本萃取的**甜菊糖苷**，符合最高安全規格GRAS。"
            }
        ],
        // --- Level 4: 朔 (Spork) --- 
        'shape': [
            {
                level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",
                product: "Spork 閃朔蜜桃飲", enemy: "體脂魔王", animation: "🔥",
                imageFile: "shape1.Jpg", 
                question: "閃朔蜜桃飲系列中，哪種成分含有豐富 HCA（羥基檸檬酸），能幫助消化並降低對食物的慾望？",
                options: ["綠咖啡萃取", "藤黃果萃取", "葡萄皮萃取", "兒茶素"],
                correct: 1, explanation: "✅ 正確！**藤黃果萃取物**含有豐富 HCA，是飲食管控的好幫手。"
            },
            {
                level: "第四關：塑形神殿 (朔)", levelColor: "var(--color-shape)",
                product: "Spork 閃朔奶茶飲", // 🚨 修正：朔奶茶飲 改為 閃朔奶茶飲
                enemy: "腹部堆積", animation: "☕",
                imageFile: "shape2.Jpg", 
                question: "閃朔奶茶飲中特有的哪種成分，具有調節生理機能、減少腹部堆積的功效？",
                options: ["綠咖啡萃取物", "藤黃果萃取物", "白藜蘆醇", "川芎萃取物"],
                correct: 3, explanation: "✅ 正確！**川芎萃取物**能調節生理機能，減少腹部堆積，幫助身體輕盈不卡水。"
            }
        ],
        // --- Level 5: 最終智慧 (餐量管理) --- 
        'final': [
             {
                level: "最終關：大師的智慧", levelColor: "var(--color-knight)",
                product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🧘",
                imageFile: "clear1.jpg", // 沿用 clear1 作為代表圖
                question: "愛樂唯餐量管理理念的核心口訣是「吃肉肉減肉肉．喝神飲減肉肉．____________」？",
                options: ["多運動減肉肉", "不用動減肉肉", "少吃澱粉減肉肉", "不吃肉減肉肉"],
                correct: 1, explanation: "✅ 正確！愛樂唯餐量管理口訣為：**吃肉肉減肉肉．喝神飲減肉肉．不用動減肉肉**。"
            }, 
            {
                level: "最終關：大師的智慧", levelColor: "var(--color-knight)",
                product: "愛樂唯餐量管理理念", enemy: "錯誤觀念", animation: "🍽️",
                imageFile: "clear2.Jpg", // 沿用 clear2 作為代表圖
                question: "愛樂唯餐量管理的目標是把健康變簡單，請問下列哪一項是其中關鍵理念？",
                options: ["多樣化的產品線", "產品簡單化更能融入生活", "專注於單一功能", "強調複雜的營養學"],
                correct: 1, explanation: "✅ 正確！產品簡單化更能融入生活，讓忙碌的生活也能輕鬆維持健康。" 
            }
        ]
    };

    let currentQuestions = []; 
    let currentQuestionIndex = 0;
    let score = 0;
    let isAnswering = false;
    let timerInterval = null; 
    let hasAnswered = false; 
    let selectedDifficulty = null; 
    let maxGameScore = 0; 

    // DOM Elements
    const startScreen = document.getElementById('startScreen');
    const gameScreen = document.getElementById('gameScreen');
    const resultScreen = document.getElementById('resultScreen');
    const questionText = document.getElementById('questionText');
    const optionsContainer = document.getElementById('optionsContainer');
    const levelBadge = document.getElementById('levelBadge');
    const feedbackArea = document.getElementById('feedbackArea');
    const feedbackTitle = document.getElementById('feedbackTitle');
    const feedbackText = document.getElementById('feedbackText');
    const nextBtn = document.getElementById('nextBtn');
    const progressFill = document.getElementById('progressFill');
    const productPlaceholder = document.getElementById('productPlaceholder');
    const enemyPlaceholder = document.getElementById('enemyPlaceholder');
    const animationArea = document.getElementById('animationArea');
    const timerDisplay = document.getElementById('timerDisplay'); 


    // --- 輔助函式：陣列隨機洗牌 ---
    function shuffleArray(array) {
        for (let i = array.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            let temp = array[i];
            array[i] = array[j];
            array[j] = temp;
        }
        return array;
    }

    // --- 倒計時邏輯 ---
    function startTimer() {
        let timeLeft = TIMER_LIMIT;
        timerDisplay.textContent = timeLeft;
        timerDisplay.style.color = 'var(--color-timer)';
        
        timerInterval = setInterval(() => {
            timeLeft--;
            timerDisplay.textContent = timeLeft;

            if (timeLeft <= 5) {
                timerDisplay.style.color = '#ff0000';
            } else if (timeLeft <= 10) {
                timerDisplay.style.color = 'var(--color-adjust)';
            }

            if (timeLeft <= 0) {
                clearInterval(timerInterval);
                timerDisplay.textContent = '時間到！';
                if (!hasAnswered) {
                    checkAnswer(-1); 
                }
            }
        }, 1000); 
    }

    // --- 核心：根據難度選擇抽取題目並開始遊戲 ---
    function startGame(difficulty) {
        selectedDifficulty = difficulty;
        const settings = difficultySettings[difficulty];
        
        startScreen.classList.add('hidden');
        gameScreen.classList.remove('hidden');
        
        currentQuestionIndex = 0;
        score = 0;
        currentQuestions = []; 
        maxGameScore = settings.count * MAX_SCORE_PER_QUESTION;

        const drawCounts = settings.draw;
        
        // 1. 根據難度設定，從每個主題庫中隨機抽取題目
        for (const key in drawCounts) {
            const count = drawCounts[key];
            if (fullQuestionBank[key] && Array.isArray(fullQuestionBank[key])) {
                const shuffledBank = shuffleArray([...fullQuestionBank[key]]); 
                currentQuestions.push(...shuffledBank.slice(0, count)); 
            }
        }
        
        // 2. 確保總題庫的順序是隨機的
        currentQuestions = shuffleArray(currentQuestions);

        // 3. 隨機洗牌選項
        currentQuestions = currentQuestions.map(q => {
            const originalOptions = q.options;
            const correctText = originalOptions[q.correct];
            
            const newOptions = shuffleArray([...originalOptions]);
            const newCorrectIndex = newOptions.indexOf(correctText);

            return {
                ...q,
                options: newOptions,
                correct: newCorrectIndex
            };
        });

        // 啟動第一道題目
        showQuestion();
    }
    
    // --- 顯示題目 ---
    function showQuestion() {
        isAnswering = true;
        hasAnswered = false; 
        feedbackArea.style.display = 'none';
        
        const buttons = optionsContainer.querySelectorAll('button');
        buttons.forEach(btn => btn.remove());
        
        if (timerInterval) {
            clearInterval(timerInterval);
        }

        const q = currentQuestions[currentQuestionIndex]; 
        
        // 動態更新 UI
        levelBadge.textContent = `${q.level} (第 ${currentQuestionIndex + 1} 題 / 共 ${currentQuestions.length} 題)`;
        levelBadge.style.backgroundColor = q.levelColor;
        questionText.textContent = q.question;
        
        // 注入圖片
        productPlaceholder.innerHTML = `<img src="${q.imageFile}" alt="${q.product}" onerror="this.onerror=null;this.src='//:0'" />`;
        
        // 注入敵人/問題點資訊 (敵人顯示在圖片右邊)
        enemyPlaceholder.innerHTML = `
            <div>${q.product}</div>
            <span>(敵人/問題點: ${q.enemy})</span>
        `;
        
        // 更新進度條
        const progress = (currentQuestionIndex / currentQuestions.length) * 100;
        progressFill.style.width = `${progress}%`;

        // 渲染選項
        optionsContainer.innerHTML = '';
        q.options.forEach((opt, index) => {
            const btn = document.createElement('button');
            btn.className = 'btn option-btn fade-in';
            btn.textContent = opt;
            btn.onclick = () => checkAnswer(index);
            optionsContainer.appendChild(btn);
        });

        startTimer();
    }

    // --- 檢查答案 ---
    function checkAnswer(selectedIndex) {
        if (!isAnswering && selectedIndex !== -1) return; 
        if (hasAnswered && selectedIndex !== -1) return;

        clearInterval(timerInterval);
        isAnswering = false;
        hasAnswered = true;

        const q = currentQuestions[currentQuestionIndex];
        const isCorrect = selectedIndex === q.correct;
        
        if (selectedIndex === -1) {
             feedbackTitle.textContent = `⏰ 時間到！`;
             feedbackText.innerHTML = `<strong>遺憾！</strong>您未能在 ${TIMER_LIMIT} 秒內作答，本題不計分。正確答案是：${q.options[q.correct]}`;
             feedbackArea.className = `feedback wrong fade-in`;
        } else {
            const buttons = optionsContainer.querySelectorAll('button');
            buttons.forEach((btn, idx) => {
                btn.disabled = true; 
                if (idx === q.correct) {
                    btn.style.backgroundColor = 'var(--color-supplement)'; 
                    btn.style.color = 'white';
                } else if (idx === selectedIndex && !isCorrect) {
                    btn.style.backgroundColor = 'var(--color-shape)'; 
                    btn.style.color = 'white';
                } else {
                    btn.style.opacity = '0.5';
                }
            });

            feedbackArea.style.display = 'block';
            feedbackArea.className = `feedback ${isCorrect ? 'correct' : 'wrong'} fade-in`;
            feedbackTitle.textContent = isCorrect ? `🎉 成功！騎士擊敗了 ${q.enemy}` : `💥 失誤！ ${q.enemy} 暫時擋住了去路`;
            
            if (isCorrect) {
                score += MAX_SCORE_PER_QUESTION;
                feedbackText.innerHTML = `<strong>知識解析：</strong> ${q.explanation}`;
            } else {
                feedbackText.innerHTML = `<strong>錯誤解析：</strong> 答案是 **${q.options[q.correct]}**。<br>${q.explanation}`;
            }
        }
        
        feedbackArea.style.display = 'block';

        if (currentQuestionIndex === currentQuestions.length - 1) {
            nextBtn.textContent = "拯救公主 (查看結果)";
        } else {
            nextBtn.textContent = "繼續前進";
        }
    }

    function nextQuestion() {
        currentQuestionIndex++;
        if (currentQuestionIndex < currentQuestions.length) {
            showQuestion();
        } else {
            showResult();
        }
    }

    function showResult() {
        gameScreen.classList.add('hidden');
        resultScreen.classList.remove('hidden');
        
        const settings = difficultySettings[selectedDifficulty];
        const finalScoreElement = document.getElementById('finalScore');
        const resultMessage = document.getElementById('resultMessage');
        const finalCharacterDisplay = document.getElementById('finalCharacterDisplay');
        
        progressFill.style.width = '100%';

        let title = '';
        if (score === maxGameScore) {
            title = settings.titlePerfect;
            finalCharacterDisplay.textContent = '👸🏼'; 
            finalCharacterDisplay.className = 'character-display princess-final fade-in';
            resultMessage.innerHTML = `恭喜！您以 **${maxGameScore} 分** 滿分，獲得<br>【**${title}**】稱號！公主已恢復光彩！`;
        } 
        else if (score >= maxGameScore * 0.7) {
            title = settings.titleGreat;
            finalCharacterDisplay.textContent = '👸🏽';
            finalCharacterDisplay.className = 'character-display princess-initial fade-in';
            resultMessage.innerHTML = `表現優異！您獲得【**${title}**】稱號！<br>最終得分：${score} 分，公主正在好轉中！`;
        } 
        else {
            title = "養生學徒";
            finalCharacterDisplay.textContent = '👸🏿';
            finalCharacterDisplay.className = 'character-display princess-initial fade-in';
            resultMessage.innerHTML = `您是【**${title}**】！<br>最終得分：${score} 分，公主狀態有改善，但仍需努力！`;
        }

        let currentScore = 0;
        finalScoreElement.textContent = '0';
        const interval = setInterval(() => {
            currentScore += 5;
            if (currentScore >= score) {
                currentScore = score;
                clearInterval(interval);
            }
            finalScoreElement.textContent = currentScore;
        }, 30);
    }

    function restartGame() {
        resultScreen.classList.add('hidden');
        startScreen.classList.remove('hidden');
        if (timerInterval) {
            clearInterval(timerInterval); 
        }
    }
</script>
