<!DOCTYPE html>
<html>
<head>
  <title>Hair Guide | 发型决策助手</title>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    /* 原有CSS样式保持不变 */
    :root { --neon-blue: #00f3ff; --neon-pink: #ff00ff; --bg-dark: #0a0a0a; }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Space Grotesk', sans-serif; min-height: 100vh; background: var(--bg-dark); color: white; overflow-x: hidden; }
    .guide-container { display: flex; flex-direction: column; align-items: center; justify-content: center; min-height: 100vh; padding: 2rem; background: radial-gradient(circle at 50% 50%, #1a1a1a 0%, #0a0a0a 100%); }
    .main-title { text-align: center; margin-bottom: 4rem; position: relative; }
    .main-title h1 { font-size: 3.5rem; letter-spacing: -0.03em; margin-bottom: 1rem; background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    .choice-grid { display: grid; gap: 2rem; width: 100%; max-width: 1200px; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); }
    .choice-card { background: rgba(255, 255, 255, 0.05); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 20px; padding: 2.5rem; text-align: center; backdrop-filter: blur(10px); transition: all 0.3s ease; cursor: pointer; position: relative; overflow: hidden; }
    .choice-card:hover { transform: translateY(-10px); background: rgba(255, 255, 255, 0.1); box-shadow: 0 0 30px rgba(0, 243, 255, 0.2); }
    .choice-card::before { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: linear-gradient(45deg, transparent, var(--neon-blue), transparent, var(--neon-pink), transparent); animation: borderFlow 6s linear infinite; opacity: 0.3; }
    @keyframes borderFlow { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    .choice-card h2 { font-size: 2rem; margin-bottom: 1rem; position: relative; z-index: 1; }
    .choice-card p { color: rgba(255, 255, 255, 0.8); position: relative; z-index: 1; }
    .upload-section { display: none; max-width: 600px; margin: 0 auto; text-align: center; }
    .color-grid { display: grid; gap: 1.5rem; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); width: 100%; max-width: 1400px; padding: 2rem; }
    .color-card { position: relative; height: 320px; border-radius: 24px; overflow: hidden; transition: transform 0.3s ease; cursor: pointer; }
    .color-card:hover { transform: scale(1.03); }
    .color-card::before { content: ''; position: absolute; inset: 0; background: linear-gradient(180deg, rgba(0,0,0,0) 50%, rgba(0,0,0,0.6) 100%); }
    .color-info { position: absolute; bottom: 1.5rem; left: 1.5rem; color: white; text-shadow: 0 2px 4px rgba(0,0,0,0.3); }
    .color-name { font-size: 1.8rem; font-weight: 700; margin-bottom: 0.5rem; }
    .color-tags { display: flex; gap: 0.5rem; flex-wrap: wrap; }
    .color-tag { background: rgba(255,255,255,0.2); padding: 0.3rem 0.8rem; border-radius: 20px; font-size: 0.9rem; backdrop-filter: blur(5px); }
    .search-bar { position: fixed; bottom: 2rem; width: 90%; max-width: 600px; background: rgba(255,255,255,0.1); border-radius: 50px; padding: 0.8rem 1.5rem; backdrop-filter: blur(10px); display: flex; gap: 1rem; }
    .search-bar input { flex: 1; background: transparent; border: none; color: white; font-size: 1.1rem; }
    .search-bar button { background: none; border: none; color: var(--neon-blue); font-size: 1.2rem; cursor: pointer; }
    @media (max-width: 768px) { .main-title h1 { font-size: 2.5rem; } }
  </style>
</head>
<body>
  <!-- 步骤一：类型选择 -->
  <div class="guide-container" id="step1">
    <div class="main-title">
      <h1>CREATE YOUR STYLE</h1>
      <p>选择你的改造方式</p>
    </div>
    <div class="choice-grid">
      <div class="choice-card" onclick="showUploadSection('染发')">
        <h2>🍃 染发灵感</h2>
        <p>寻找惊艳发色方案</p>
      </div>
      <div class="choice-card" onclick="showUploadSection('剪发')">
        <h2>✨ 剪发指南</h2>
        <p>探索最新发型趋势</p>
      </div>
    </div>
  </div>

  <!-- 步骤二：上传界面 -->
  <div class="guide-container" id="step2" style="display: none;">
    <div class="main-title">
      <h1 id="stepTitle">UPLOAD YOUR IDEA</h1>
      <p>上传你的灵感图片</p>
    </div>
    <div class="upload-section">
      <input type="file" id="imageInput" accept="image/*" hidden>
      <label for="imageInput" class="choice-card" style="cursor: pointer;">
        <h2>📸 点击上传</h2>
        <p>支持 JPG/PNG 格式</p>
      </label>
      <div id="preview" style="margin-top: 2rem;"></div>
    </div>
  </div>

  <!-- 步骤三：发色推荐 -->
  <div class="guide-container" id="step3" style="display: none;">
    <div class="main-title">
      <h1 id="colorTitle">TREND COLORS</h1>
      <p>当前流行发色推荐 · 每日更新</p>
    </div>
    <div class="color-grid" id="colorGrid"></div>
    <div class="search-bar">
      <input type="text" placeholder="搜索发色关键词：例如 '雾霾蓝'">
      <button>🔍</button>
    </div>
  </div>

  <script>
    // 小红书风格发色库（图床链接示例）
    const colorData = [
      { 
        name: "冰球冰蓝", 
        image: "https://i.imgur.com/5g3VJjC.png", // 替换为真实图床链接
        tags: ["明星同款", "需漂发", "冷色调"]
      },
      {
        name: "黑茶雾棕",
        image: "https://i.imgur.com/6JZ8gG3.png", // 替换为真实图床链接
        tags: ["自然显白", "通勤必备"]
      },
      {
        name: "霓虹粉紫",
        image: "https://i.imgur.com/Vs6GQkC.png", // 替换为真实图床链接
        tags: ["派对焦点", "渐变可选"]
      },
      {
        name: "鎏金沙金",
        image: "https://i.imgur.com/TPy1gDx.png", // 替换为真实图床链接
        tags: ["暖调质感", "免漂色"]
      },
      {
        name: "赛博霓虹",
        image: "https://i.imgur.com/K3kHnRZ.png", // 替换为真实图床链接
        tags: ["高冷系", "需定期护理"]
      }
    ];

    // 生成色卡
    function generateColorCards() {
      const grid = document.getElementById('colorGrid');
      grid.innerHTML = '';
      const shuffledColors = [...colorData].sort(() => Math.random() - 0.5).concat(colorData, colorData);
      
      shuffledColors.forEach(color => {
        const card = document.createElement('div');
        card.className = 'color-card';
        card.style.background = `url('${color.image}') center/cover`;
        card.innerHTML = `
          <div class="color-info">
            <div class="color-name">${color.name}</div>
            <div class="color-tags">
              ${color.tags.map(tag => `<span class="color-tag">${tag}</span>`).join('')}
            </div>
          </div>
        `;
        grid.appendChild(card);
      });
    }

    // 页面切换逻辑
    function showUploadSection(type) {
      document.getElementById('step1').style.display = 'none';
      if(type === '染发') {
        document.getElementById('step3').style.display = 'block';
        generateColorCards();
        document.body.style.background = 'radial-gradient(circle at 50% 50%, #1a1a1a 0%, #0f0a1a 100%)';
      } else {
        document.getElementById('step2').style.display = 'block';
        document.getElementById('stepTitle').innerHTML = `${type}灵感上传`;
        document.body.style.background = 'radial-gradient(circle at 50% 50%, #1a1a1a 0%, #1a0f0a 100%)';
      }
    }

    // 图片上传预览
    document.getElementById('imageInput').addEventListener('change', function(e) {
      const reader = new FileReader();
      reader.onload = function(e) {
        document.getElementById('preview').innerHTML = `
          <div class="choice-card" style="cursor: default; padding: 0;">
            <img src="${e.target.result}" style="width: 100%; border-radius: 15px;">
          </div>
        `;
      };
      reader.readAsDataURL(this.files[0]);
    });
  </script>
</body>
</html>
