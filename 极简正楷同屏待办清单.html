<!doctype html>
<html lang="zh-CN">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
<title>今日与明日 — 极简正楷待办</title>
<!-- PWA 移动端原生 App 化配置 -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="今日与明日">
<meta name="mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#fcfcfa">
<link id="appleTouchIcon" rel="apple-touch-icon">
<link id="pwaManifest" rel="manifest">
<!-- 引入谷歌云端楷体（LXGW WenKai / Noto Serif SC 作为手机端正楷回退），确保手机与电脑均呈现温润正楷质感 -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #fcfcfa;
    --surface: #ffffff;
    --ink: #1c1c1a;
    --muted: #787872;
    --light: #a8a8a2;
    --line: #ecece6;
    --accent: #2c4c3b;
    --warn: #b45309;
    --warn-bg: #fdf8ee;
    --warn-border: #f3dfb9;
    --danger: #b91c1c;
    --font-kai: "Kaiti SC", "STKaiti", "楷体", "KaiTi", "BiauKai", "DFKai-SB", "Noto Serif SC", serif;
  }

  * {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
  }

  body {
    margin: 0;
    background: var(--bg);
    color: var(--ink);
    font: 15px/1.65 var(--font-kai);
    -webkit-font-smoothing: antialiased;
    padding-bottom: 108px;
  }

  button, input, select {
    font-family: var(--font-kai);
    font-size: inherit;
    color: inherit;
  }

  button {
    cursor: pointer;
    border: 0;
    background: transparent;
  }

  .container {
    max-width: 1280px;
    margin: 0 auto;
    padding: calc(18px + env(safe-area-inset-top)) 18px 24px;
  }

  /* 极简头部：仅保留日期与轻量操作 */
  header {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding-bottom: 14px;
    margin-bottom: 18px;
    border-bottom: 1px solid var(--line);
    gap: 10px;
  }

  .brand-wrap h1 {
    margin: 0;
    font-size: 21px;
    font-weight: 700;
    letter-spacing: 0.06em;
  }

  .brand-wrap p {
    margin: 2px 0 0;
    font-size: 13px;
    color: var(--muted);
  }

  .top-actions {
    display: flex;
    gap: 12px;
    align-items: center;
  }

  .text-link {
    font-size: 13px;
    color: var(--muted);
    padding: 4px 2px;
    border-bottom: 1px solid transparent;
    transition: color .15s, border-color .15s;
  }

  .text-link:hover, .text-link:active {
    color: var(--ink);
    border-bottom-color: var(--ink);
  }

  /* 提前提醒横幅 */
  .alert-banner {
    display: none;
    background: var(--warn-bg);
    border-left: 3px solid var(--warn);
    color: #78350f;
    padding: 9px 14px;
    margin-bottom: 18px;
    font-size: 14px;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
  }

  .alert-banner.show {
    display: flex;
  }

  /* 分区标题：去掉背景块，使用干净留白与文字排版 */
  .section-label {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    margin-bottom: 10px;
  }

  .section-label h2 {
    margin: 0;
    font-size: 14px;
    font-weight: 600;
    color: var(--muted);
    letter-spacing: 0.08em;
  }

  /* 1. 顶部倒计时：极简横向条带 */
  .countdown-strip {
    display: flex;
    gap: 12px;
    overflow-x: auto;
    padding-bottom: 4px;
    margin-bottom: 24px;
    scrollbar-width: none;
  }

  .countdown-strip::-webkit-scrollbar {
    display: none;
  }

  .cd-card {
    flex: 0 0 auto;
    min-width: 195px;
    max-width: 260px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: 8px;
    padding: 10px 14px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 14px;
    position: relative;
  }

  .cd-card.urgent {
    background: var(--warn-bg);
    border-color: var(--warn-border);
  }

  .cd-info {
    min-width: 0;
  }

  .cd-title {
    font-size: 15px;
    font-weight: 600;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  .cd-meta {
    font-size: 12px;
    color: var(--muted);
    margin-top: 2px;
  }

  .cd-card.urgent .cd-meta {
    color: var(--warn);
  }

  .cd-badge {
    text-align: right;
    flex: none;
  }

  .cd-num {
    font-size: 22px;
    font-weight: 700;
    line-height: 1.05;
    color: var(--ink);
  }

  .cd-card.urgent .cd-num {
    color: var(--warn);
  }

  .cd-unit {
    font-size: 11px;
    color: var(--muted);
  }

  .cd-del {
    position: absolute;
    top: 2px;
    right: 5px;
    font-size: 13px;
    color: var(--light);
    padding: 2px 4px;
  }

  .cd-add-card {
    flex: 0 0 auto;
    min-width: 112px;
    border: 1px dashed #d6d6ce;
    border-radius: 8px;
    padding: 10px 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--muted);
    font-size: 13px;
  }

  /* 2. 中部核心区：未来几天同屏看板（去除厚重外框，采用极细线分隔与留白） */
  .days-controls {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .days-board {
    display: flex;
    gap: 16px;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    scroll-behavior: smooth;
    padding-bottom: 8px;
    margin-bottom: 28px;
    scrollbar-width: none;
  }

  .days-board::-webkit-scrollbar {
    display: none;
  }

  .day-col {
    flex: 0 0 80%;
    scroll-snap-align: start;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: 10px;
    padding: 16px;
    min-height: 270px;
    display: flex;
    flex-direction: column;
  }

  .day-col.is-today {
    border-color: #c5d1c9;
  }

  .day-header {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding-bottom: 10px;
    margin-bottom: 6px;
    border-bottom: 1px solid var(--line);
  }

  .day-title-group {
    display: flex;
    align-items: baseline;
    gap: 8px;
  }

  .day-rel {
    font-size: 18px;
    font-weight: 700;
  }

  .day-col.is-today .day-rel {
    color: var(--accent);
  }

  .day-date-sub {
    font-size: 13px;
    color: var(--muted);
  }

  .day-stat {
    font-size: 12px;
    color: var(--muted);
  }

  .task-list {
    flex: 1;
    display: flex;
    flex-direction: column;
  }

  /* 极简任务行：仅保留极细底线与清晰正楷文字 */
  .task-row {
    display: flex;
    align-items: center;
    gap: 6px;
    min-height: 38px;
    padding: 4px 0;
    border-bottom: 1px solid #f4f4ef;
  }

  .task-row:last-child {
    border-bottom: none;
  }

  .check-hit {
    width: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex: none;
    cursor: pointer;
  }

  .check-box {
    width: 16px;
    height: 16px;
    border-radius: 4px;
    border: 1.5px solid #c8c8c0;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all .15s;
  }

  .task-row.done .check-box {
    background: var(--ink);
    border-color: var(--ink);
  }

  .task-row.done .check-box::after {
    content: "";
    width: 4px;
    height: 8px;
    border: solid #fff;
    border-width: 0 1.5px 1.5px 0;
    transform: rotate(45deg) translate(-1px, -1px);
  }

  .prio-dot {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    flex: none;
  }

  .prio-high { background: var(--danger); }
  .prio-normal { background: transparent; }

  .task-name {
    flex: 1;
    font-size: 15px;
    line-height: 1.45;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    cursor: pointer;
  }

  .task-row.done .task-name {
    text-decoration: line-through;
    color: var(--light);
  }

  .row-actions {
    display: flex;
    align-items: center;
    gap: 6px;
    flex: none;
  }

  .tiny-act {
    font-size: 12px;
    color: var(--muted);
    padding: 2px 4px;
  }

  .tiny-act:hover, .tiny-act:active {
    color: var(--ink);
  }

  .day-inline-add {
    margin-top: 8px;
    padding-top: 8px;
    border-top: 1px dashed var(--line);
    display: flex;
    align-items: center;
  }

  .day-inline-add input {
    width: 100%;
    border: none;
    background: transparent;
    font-size: 14px;
    padding: 4px 2px;
    outline: none;
  }

  .day-inline-add input::placeholder {
    color: var(--light);
  }

  /* 3. 底部区：本月总清单（更通透的纸面列表风格） */
  .pool-panel {
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: 10px;
    padding: 18px 16px;
  }

  .pool-header {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding-bottom: 10px;
    margin-bottom: 8px;
    border-bottom: 1px solid var(--line);
    gap: 8px;
  }

  .pool-header h2 {
    margin: 0;
    font-size: 17px;
    font-weight: 700;
  }

  .pool-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 0 28px;
  }

  .pool-item {
    display: flex;
    align-items: center;
    gap: 6px;
    min-height: 42px;
    padding: 4px 0;
    border-bottom: 1px solid #f4f4ef;
  }

  .pool-item:last-child {
    border-bottom: none;
  }

  .pool-text-wrap {
    flex: 1;
    min-width: 0;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .pool-title {
    font-size: 15px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  .pool-item.done .pool-title {
    text-decoration: line-through;
    color: var(--light);
  }

  .pool-tag {
    font-size: 12px;
    color: var(--muted);
    flex: none;
  }

  .assign-btns {
    display: flex;
    gap: 8px;
    flex: none;
  }

  .assign-btn {
    font-size: 13px;
    padding: 3px 6px;
    border-radius: 4px;
    color: var(--muted);
    border: 1px solid var(--line);
    background: var(--bg);
  }

  .assign-btn:hover, .assign-btn:active {
    color: var(--ink);
    border-color: var(--ink);
  }

  /* 4. 底部悬浮拇指输入栏（极简素雅） */
  .bottom-bar {
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(252, 252, 250, 0.96);
    backdrop-filter: blur(8px);
    -webkit-backdrop-filter: blur(8px);
    border-top: 1px solid var(--line);
    padding: 9px 16px calc(9px + env(safe-area-inset-bottom));
    z-index: 30;
  }

  .bottom-inner {
    max-width: 820px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 7px;
  }

  .target-tabs {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 8px;
  }

  .tab-group {
    display: flex;
    gap: 12px;
  }

  .target-pill {
    font-size: 13px;
    padding: 2px 0;
    color: var(--muted);
    border-bottom: 1.5px solid transparent;
    transition: all .15s;
  }

  .target-pill.active {
    color: var(--ink);
    font-weight: 700;
    border-bottom-color: var(--ink);
  }

  .prio-toggle {
    font-size: 12px;
    padding: 2px 8px;
    border-radius: 4px;
    border: 1px solid var(--line);
    color: var(--muted);
  }

  .prio-toggle.active {
    border-color: #fecaca;
    background: #fef2f2;
    color: var(--danger);
    font-weight: 600;
  }

  .input-row {
    display: flex;
    gap: 8px;
  }

  .input-row input {
    flex: 1;
    border: 1px solid var(--line);
    background: var(--surface);
    border-radius: 8px;
    padding: 9px 12px;
    font-size: 15px;
    outline: none;
  }

  .input-row input:focus {
    border-color: var(--ink);
  }

  .send-btn {
    background: var(--ink);
    color: #fff;
    font-size: 14px;
    padding: 0 18px;
    border-radius: 8px;
    flex: none;
  }

  /* 弹窗（新增倒计时 / 导出备份） */
  .modal-mask {
    position: fixed;
    inset: 0;
    background: rgba(28, 28, 26, .35);
    display: none;
    align-items: flex-end;
    justify-content: center;
    z-index: 50;
  }

  .modal-mask.show {
    display: flex;
  }

  .modal-sheet {
    width: 100%;
    max-width: 440px;
    background: var(--surface);
    border-radius: 14px 14px 0 0;
    padding: 22px 20px calc(22px + env(safe-area-inset-bottom));
  }

  .modal-sheet h3 {
    margin: 0 0 14px;
    font-size: 17px;
    font-weight: 700;
  }

  .field {
    margin-bottom: 12px;
  }

  .field label {
    display: block;
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 5px;
  }

  .field input, .field select {
    width: 100%;
    border: 1px solid var(--line);
    border-radius: 8px;
    padding: 9px 11px;
    font-size: 15px;
    background: #fff;
    outline: none;
  }

  .modal-btns {
    display: flex;
    gap: 10px;
    margin-top: 16px;
  }

  .modal-btns button {
    flex: 1;
    padding: 10px;
    border-radius: 8px;
    font-size: 15px;
  }

  .btn-cancel {
    background: #f4f4f0;
    color: var(--ink);
  }

  .btn-primary {
    background: var(--ink);
    color: #fff;
  }

  .toast {
    position: fixed;
    top: 16px;
    left: 50%;
    transform: translateX(-50%) translateY(-16px);
    background: var(--ink);
    color: #fff;
    font-size: 13px;
    padding: 7px 16px;
    border-radius: 99px;
    opacity: 0;
    pointer-events: none;
    transition: all .2s;
    z-index: 60;
  }

  .toast.show {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }

  /* 桌面宽屏适配 */
  @media (min-width: 768px) {
    .container {
      padding: 28px 32px 36px;
    }

    .day-col {
      flex: 1 1 0;
      min-width: 230px;
    }

    .pool-grid {
      grid-template-columns: repeat(2, 1fr);
    }

    .modal-mask {
      align-items: center;
      padding: 16px;
    }

    .modal-sheet {
      border-radius: 12px;
    }
  }
</style>
</head>
<body>

<div class="container">
  <!-- 顶部极简栏 -->
  <header>
    <div class="brand-wrap">
      <h1>今日与明日</h1>
      <p id="todayFullLabel">加载日期中...</p>
    </div>
    <div class="top-actions">
      <button class="text-link" id="installAppBtn">安装App</button>
      <button class="text-link" id="notifyBtn">开启提醒</button>
      <button class="text-link" id="backupBtn">备份</button>
    </div>
  </header>

  <!-- 提前提醒横幅 -->
  <div class="alert-banner" id="alertBanner">
    <div id="alertText"></div>
    <button class="text-link" onclick="document.getElementById('alertBanner').classList.remove('show')">知道了</button>
  </div>

  <!-- 1. 顶部区：重要日程倒计时 -->
  <div class="section-label">
    <h2>重要倒计时</h2>
    <button class="text-link" id="openEventModalBtn">＋ 新建倒计时</button>
  </div>
  <div class="countdown-strip" id="countdownStrip"></div>

  <!-- 2. 中部核心区：未来几天同屏看板 -->
  <div class="section-label">
    <h2>近日日程</h2>
    <div class="days-controls">
      <button class="text-link" id="scrollTodayBtn">回到今天</button>
      <button class="text-link" id="addMoreDayBtn">＋ 多看一天</button>
    </div>
  </div>
  <div class="days-board" id="daysBoard"></div>

  <!-- 3. 底部区：本月总清单 -->
  <section class="pool-panel">
    <div class="pool-header">
      <h2 id="monthPoolTitle">本月总清单</h2>
      <span class="day-stat" id="poolCountBadge">0 项待安排</span>
    </div>
    <div class="pool-grid" id="monthPoolList"></div>
  </section>
</div>

<!-- 底部悬浮拇指输入栏 -->
<div class="bottom-bar">
  <div class="bottom-inner">
    <div class="target-tabs">
      <div class="tab-group" id="targetTabs">
        <button type="button" class="target-pill active" data-target="0">今天</button>
        <button type="button" class="target-pill" data-target="1">明天</button>
        <button type="button" class="target-pill" data-target="2">后天</button>
        <button type="button" class="target-pill" data-target="month">本月总清单</button>
      </div>
      <button type="button" class="prio-toggle" id="prioToggle">重要</button>
    </div>
    <form class="input-row" id="bottomForm">
      <input type="text" id="bottomInput" placeholder="写下待办事项，记入「今天」..." autocomplete="off" required>
      <button type="submit" class="send-btn">记下</button>
    </form>
  </div>
</div>

<!-- 新建倒计时弹窗 -->
<div class="modal-mask" id="eventModal">
  <div class="modal-sheet">
    <h3>新建重要倒计时</h3>
    <form id="eventForm">
      <div class="field">
        <label>事项名称</label>
        <input type="text" id="evName" placeholder="例如：重要客户方案评审会" required maxlength="60">
      </div>
      <div class="field">
        <label>发生日期与时间</label>
        <input type="datetime-local" id="evDate" required>
      </div>
      <div class="field">
        <label>提前几天开始提醒</label>
        <select id="evLead">
          <option value="0">当天提醒</option>
          <option value="1">提前 1 天提醒</option>
          <option value="2" selected>提前 2 天提醒（如后天会议今天提醒）</option>
          <option value="3">提前 3 天提醒</option>
          <option value="7">提前 7 天提醒</option>
        </select>
      </div>
      <div class="modal-btns">
        <button type="button" class="btn-cancel" data-close-modal>取消</button>
        <button type="submit" class="btn-primary">保存</button>
      </div>
    </form>
  </div>
</div>

<!-- 备份与恢复弹窗 -->
<div class="modal-mask" id="backupModal">
  <div class="modal-sheet">
    <h3>数据备份与恢复</h3>
    <p style="font-size:13px;color:var(--muted);margin:0 0 14px;line-height:1.6">
      所有数据默认安全保存在当前设备浏览器本地。你可以导出 JSON 文件备份，或在其他设备导入同步。
    </p>
    <div style="display:flex;flex-direction:column;gap:10px">
      <button type="button" class="btn-primary" style="padding:10px;border-radius:8px" id="exportJsonBtn">导出数据备份 (.json)</button>
      <label class="btn-cancel" style="padding:10px;border-radius:8px;text-align:center;cursor:pointer">
        导入备份文件恢复
        <input type="file" id="importJsonInput" accept="application/json" hidden>
      </label>
      <button type="button" class="btn-cancel" data-close-modal>关闭</button>
    </div>
  </div>
</div>

<!-- 安装为手机 App 引导弹窗 -->
<div class="modal-mask" id="installModal">
  <div class="modal-sheet">
    <h3>安装到手机桌面（像原生 App 一样使用）</h3>
    <p style="font-size:13px;color:var(--muted);margin:0 0 12px;line-height:1.65">
      本网页已内置 <strong>PWA 桌面应用支持</strong>，无需下载安装包，添加到主屏幕后即可全屏独立运行：
    </p>
    <div style="background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:12px;font-size:13px;line-height:1.7;margin-bottom:14px">
      <div style="margin-bottom:8px"><strong>🍎 iPhone / iPad（Safari 浏览器）：</strong><br>点击底部工具栏的 <strong>「分享」图标（方框向上箭头）</strong> → 向下滑动选择 <strong>「添加到主屏幕」</strong>。</div>
      <div><strong>🤖 安卓手机（Chrome / Edge / 系统浏览器）：</strong><br>点击浏览器右上角 <strong>「⋮ 菜单」</strong> → 选择 <strong>「添加到主屏幕」</strong> 或 <strong>「安装应用」</strong>。</div>
    </div>
    <div class="modal-btns">
      <button type="button" class="btn-cancel" data-close-modal>关闭</button>
      <button type="button" class="btn-primary" id="triggerNativeInstallBtn" style="display:none">立即一键安装</button>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
// ... existing code ... -->
  $('backupBtn').onclick = () => $('backupModal').classList.add('show');

  // 动态生成正楷 App 桌面图标与 PWA Manifest
  (function initPWA() {
    try {
      const canvas = document.createElement('canvas');
      canvas.width = 512;
      canvas.height = 512;
      const ctx = canvas.getContext('2d');
      // 温润素纸底色与边框
      ctx.fillStyle = '#fcfcfa';
      ctx.fillRect(0, 0, 512, 512);
      ctx.strokeStyle = '#2c4c3b';
      ctx.lineWidth = 18;
      ctx.strokeRect(36, 36, 440, 440);
      // 居中绘制正楷“今”字徽标
      ctx.fillStyle = '#1c1c1a';
      ctx.font = 'bold 240px "Kaiti SC", "STKaiti", "楷体", "KaiTi", serif';
      ctx.textAlign = 'center';
      ctx.textBaseline = 'middle';
      ctx.fillText('今', 256, 268);

      const iconDataUrl = canvas.toDataURL('image/png');
      $('appleTouchIcon').href = iconDataUrl;

      const manifest = {
        name: '今日与明日 · 极简待办',
        short_name: '今日与明日',
        description: '极简正楷同屏多日待办与倒计时提醒',
        start_url: location.href,
        display: 'standalone',
        background_color: '#fcfcfa',
        theme_color: '#fcfcfa',
        icons: [
          { src: iconDataUrl, sizes: '512x512', type: 'image/png', purpose: 'any maskable' }
        ]
      };
      const manifestBlob = new Blob([JSON.stringify(manifest)], { type: 'application/manifest+json' });
      $('pwaManifest').href = URL.createObjectURL(manifestBlob);
    } catch (e) {}
  })();

  // 监听安卓/桌面端原生 PWA 安装事件
  let deferredPrompt = null;
  window.addEventListener('beforeinstallprompt', e => {
    e.preventDefault();
    deferredPrompt = e;
    $('triggerNativeInstallBtn').style.display = 'block';
  });

  $('installAppBtn').onclick = () => {
    // 若已处于独立 App 模式运行，给予提示
    if (window.matchMedia('(display-mode: standalone)').matches || window.navigator.standalone) {
      toast('当前已处于独立 App 模式运行中');
      return;
    }
    $('installModal').classList.add('show');
  };

  $('triggerNativeInstallBtn').onclick = async () => {
    if (!deferredPrompt) return;
    deferredPrompt.prompt();
    const { outcome } = await deferredPrompt.userChoice;
    if (outcome === 'accepted') {
      toast('正在添加到桌面...');
      $('installModal').classList.remove('show');
    }
    deferredPrompt = null;
  };

  $('exportJsonBtn').onclick = () => {
// ... existing code ... -->