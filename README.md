<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Profile README - Ibrahim Elsayed</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://code.iconify.design/iconify-icon/1.0.7/iconify-icon.min.js"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            inter: ['Inter', 'ui-sans-serif', 'system-ui'],
            bricolage: ['Bricolage Grotesque', 'sans-serif'],
          }
        }
      }
    }
  </script>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Inter', sans-serif; background: #0a0a0a; color: #ffffff; }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #171717; }
    ::-webkit-scrollbar-thumb { background: rgba(168,85,247,0.4); border-radius: 9999px; }

    /* Glass */
    .glass {
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(255,255,255,0.1);
    }

    /* Animations */
    @keyframes fadeSlideIn {
      0% { opacity: 0; transform: translateY(30px); filter: blur(8px); }
      100% { opacity: 1; transform: translateY(0); filter: blur(0); }
    }
    .animate-in { animation: fadeSlideIn 0.6s ease-out both; }
    .delay-1 { animation-delay: 0.1s; }
    .delay-2 { animation-delay: 0.2s; }
    .delay-3 { animation-delay: 0.3s; }
    .delay-4 { animation-delay: 0.4s; }
    .delay-5 { animation-delay: 0.5s; }
    .delay-6 { animation-delay: 0.6s; }

    @keyframes typing {
      0%, 100% { width: 0; }
      30%, 70% { width: 100%; }
    }
    @keyframes blink {
      0%, 100% { border-color: #a855f7; }
      50% { border-color: transparent; }
    }
    .typing-text {
      overflow: hidden;
      white-space: nowrap;
      border-right: 3px solid #a855f7;
      animation: typing 3s ease-in-out infinite, blink 0.8s step-end infinite;
      display: inline-block;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
    }
    .float-anim { animation: float 3s ease-in-out infinite; }
    .float-anim-delay { animation: float 3s ease-in-out 1s infinite; }

    @keyframes pulse-glow {
      0%, 100% { box-shadow: 0 0 20px rgba(168,85,247,0.2); }
      50% { box-shadow: 0 0 40px rgba(168,85,247,0.4); }
    }
    .pulse-glow { animation: pulse-glow 2s ease-in-out infinite; }

    @keyframes shimmer {
      0% { background-position: -200% center; }
      100% { background-position: 200% center; }
    }
    .shimmer {
      background: linear-gradient(90deg, transparent 0%, rgba(168,85,247,0.15) 50%, transparent 100%);
      background-size: 200% 100%;
      animation: shimmer 3s ease-in-out infinite;
    }

    /* GitHub Preview Styles */
    .gh-preview {
      background: #0d1117;
      border: 1px solid #30363d;
      border-radius: 12px;
      overflow: hidden;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
    }
    .gh-header {
      background: #161b22;
      border-bottom: 1px solid #30363d;
      padding: 12px 16px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .gh-dot { width: 12px; height: 12px; border-radius: 50%; }
    .gh-body { padding: 32px 40px; }
    .gh-body h1 { font-size: 28px; font-weight: 600; color: #f0f6fc; border: none; padding: 0; margin: 0; }
    .gh-body h2 { font-size: 22px; font-weight: 600; color: #f0f6fc; border-bottom: 1px solid #30363d; padding-bottom: 8px; margin-top: 28px; margin-bottom: 16px; }
    .gh-body p { color: #c9d1d9; line-height: 1.7; font-size: 15px; margin-bottom: 12px; }
    .gh-body a { color: #58a6ff; text-decoration: none; }
    .gh-body a:hover { text-decoration: underline; }
    .gh-body ul { color: #c9d1d9; padding-left: 24px; margin-bottom: 12px; }
    .gh-body li { margin-bottom: 6px; line-height: 1.6; }
    .gh-body strong { color: #f0f6fc; font-weight: 600; }
    .gh-body hr { border: none; border-top: 1px solid #30363d; margin: 24px 0; }

    .gh-badge {
      display: inline-flex;
      align-items: center;
      height: 28px;
      border-radius: 6px;
      padding: 0 12px;
      font-size: 13px;
      font-weight: 500;
      margin: 2px;
      transition: transform 0.2s, box-shadow 0.2s;
      cursor: pointer;
    }
    .gh-badge:hover { transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.4); }

    .gh-stat-card {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 8px;
      padding: 16px;
      text-align: center;
      transition: all 0.3s;
    }
    .gh-stat-card:hover { border-color: rgba(168,85,247,0.4); box-shadow: 0 0 20px rgba(168,85,247,0.1); }

    .gh-exp-card {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 8px;
      padding: 20px 24px;
      margin-bottom: 16px;
      transition: all 0.3s;
    }
    .gh-exp-card:hover { border-color: rgba(168,85,247,0.3); }

    .gh-tool-icon {
      width: 44px; height: 44px;
      border-radius: 10px;
      display: flex; align-items: center; justify-content: center;
      background: #161b22;
      border: 1px solid #30363d;
      transition: all 0.3s;
      cursor: pointer;
    }
    .gh-tool-icon:hover { transform: translateY(-4px) scale(1.05); border-color: rgba(168,85,247,0.5); box-shadow: 0 8px 24px rgba(0,0,0,0.3); }

    /* Toast */
    .toast {
      position: fixed;
      bottom: 32px;
      left: 50%;
      transform: translateX(-50%) translateY(100px);
      background: linear-gradient(135deg, #7c3aed, #2563eb);
      color: white;
      padding: 14px 28px;
      border-radius: 12px;
      font-weight: 500;
      font-size: 15px;
      z-index: 9999;
      transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1), opacity 0.4s;
      opacity: 0;
      box-shadow: 0 8px 32px rgba(124,58,237,0.4);
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .toast.show { transform: translateX(-50%) translateY(0); opacity: 1; }

    /* Code block */
    .code-block {
      background: #0d1117;
      border: 1px solid #30363d;
      border-radius: 12px;
      overflow: hidden;
      max-height: 400px;
      overflow-y: auto;
    }
    .code-header {
      background: #161b22;
      border-bottom: 1px solid #30363d;
      padding: 10px 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .code-content {
      padding: 20px;
      font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
      font-size: 12.5px;
      line-height: 1.6;
      color: #c9d1d9;
      white-space: pre-wrap;
      word-break: break-all;
      direction: ltr;
      text-align: left;
    }

    /* Gradient border */
    .gradient-border {
      position: relative;
    }
    .gradient-border::before {
      content: '';
      position: absolute;
      inset: -1px;
      border-radius: inherit;
      background: linear-gradient(135deg, rgba(168,85,247,0.4), rgba(37,99,235,0.4), rgba(6,182,212,0.2));
      z-index: -1;
      opacity: 0;
      transition: opacity 0.4s;
    }
    .gradient-border:hover::before { opacity: 1; }

    @media (max-width: 768px) {
      .gh-body { padding: 20px; }
      .gh-body h1 { font-size: 22px; }
      .gh-body h2 { font-size: 18px; }
    }
  </style>
</head>
<body>

  <!-- Background Decorations -->
  <div class="fixed inset-0 overflow-hidden pointer-events-none" aria-hidden="true">
    <div class="absolute top-[-200px] right-[-100px] w-[500px] h-[500px] rounded-full bg-purple-500/10 blur-3xl"></div>
    <div class="absolute bottom-[-200px] left-[-100px] w-[600px] h-[600px] rounded-full bg-blue-500/8 blur-3xl"></div>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] rounded-full bg-purple-500/5 blur-3xl"></div>
  </div>

  <!-- Main Container -->
  <div class="relative z-10 max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-12">

    <!-- Top Bar -->
    <div class="animate-in delay-1 flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 mb-8">
      <div>
        <h1 class="font-bricolage text-2xl sm:text-3xl font-600 tracking-tight">
          <span class="bg-gradient-to-r from-purple-400 via-blue-400 to-cyan-400 bg-clip-text text-transparent">GitHub Profile README</span>
        </h1>
        <p class="text-white/60 text-sm mt-1">معاينة حية قبل ما تنسخها لـ GitHub</p>
      </div>
      <button onclick="copyReadme()" id="copyBtn"
        class="flex items-center gap-2 px-6 py-3 rounded-2xl font-medium text-sm
               bg-gradient-to-r from-purple-600 to-blue-600 hover:from-purple-500 hover:to-blue-500
               text-white shadow-lg shadow-purple-500/25 hover:shadow-purple-500/40
               transition-all duration-300 hover:scale-105 active:scale-95">
        <iconify-icon icon="lucide:copy" width="16"></iconify-icon>
        نسخ كود الـ README
      </button>
    </div>

    <!-- GitHub Preview -->
    <div class="animate-in delay-2 gh-preview gradient-border rounded-2xl overflow-hidden mb-8">

      <!-- Browser Header -->
      <div class="gh-header">
        <div class="gh-dot bg-red-500/80"></div>
        <div class="gh-dot bg-yellow-500/80"></div>
        <div class="gh-dot bg-green-500/80"></div>
        <div class="flex-1 mx-4">
          <div class="bg-[#0d1117] rounded-md px-3 py-1.5 text-xs text-white/40 text-center max-w-sm mx-auto">
            github.com/meshibrahimelsayed
          </div>
        </div>
        <iconify-icon icon="lucide:star" width="14" class="text-white/30"></iconify-icon>
      </div>

      <!-- README Content Preview -->
      <div class="gh-body" dir="ltr" style="text-align: left;">

        <!-- Name & Title -->
        <div style="text-align: center; margin-bottom: 16px;">
          <h1 style="font-size: 28px; margin-bottom: 4px;">
            <span style="background: linear-gradient(90deg, #a855f7, #3b82f6, #06b6d4); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">Ibrahim Elsayed Mohamed</span>
          </h1>
          <p style="font-size: 18px; color: #c9d1d9; margin-bottom: 8px;">Cybersecurity & Network Security Engineer 🛡️</p>
          <p style="font-size: 14px; color: #8b949e;">
            📍 Sharqia, Egypt &nbsp;|&nbsp; 📞 +20 101 773 8269 &nbsp;|&nbsp; ✉️ mesh.ibrahimelsayed@gmail.com
          </p>
        </div>

        <!-- Badges -->
        <div style="text-align: center; margin-bottom: 8px; display: flex; flex-wrap: wrap; justify-content: center; gap: 6px;">
          <a href="#" class="gh-badge" style="background: #1f6feb22; color: #58a6ff; border: 1px solid #1f6feb44;">
            <iconify-icon icon="lucide:globe" width="14" style="margin-right: 4px;"></iconify-icon> Portfolio
          </a>
          <a href="#" class="gh-badge" style="background: #1f6feb22; color: #58a6ff; border: 1px solid #1f6feb44;">
            <iconify-icon icon="lucide:linkedin" width="14" style="margin-right: 4px;"></iconify-icon> LinkedIn
          </a>
          <a href="mailto:mesh.ibrahimelsayed@gmail.com" class="gh-badge" style="background: #da363322; color: #f85149; border: 1px solid #da363344;">
            <iconify-icon icon="lucide:mail" width="14" style="margin-right: 4px;"></iconify-icon> Email
          </a>
        </div>

        <hr>

        <!-- About Me -->
        <h2>👨‍💻 About Me</h2>
        <p>Performance-driven <strong>Computer Science & Software Engineering</strong> student specializing in <strong>Advanced Network Infrastructure</strong> and <strong>System Administration</strong>. Possesses proven hands-on expertise in configuring, securing, and troubleshooting enterprise networks and virtualization platforms.</p>
        <p>Actively advancing into <strong>Cybersecurity domains</strong> (SOC Operations & Penetration Testing) and infrastructure automation.</p>

        <!-- Languages & Tools -->
        <h2>🔧 Languages & Tools</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; margin-bottom: 8px;">
          <!-- Cisco -->
          <div class="gh-tool-icon float-anim" title="Cisco">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="#049FD9"><path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm4.5 15.75h-9v-1.5h9v1.5zm0-3h-9v-1.5h9v1.5zm0-3h-9V8.25h9v1.5z"/></svg>
          </div>
          <!-- Wireshark -->
          <div class="gh-tool-icon float-anim-delay" title="Wireshark">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="#1679A7"><circle cx="12" cy="12" r="10" fill="none" stroke="#1679A7" stroke-width="1.5"/><path d="M8 12c0-2.2 1.8-4 4-4s4 1.8 4 4-1.8 4-4 4" fill="none" stroke="#1679A7" stroke-width="1.5" stroke-linecap="round"/><circle cx="12" cy="12" r="1.5" fill="#1679A7"/></svg>
          </div>
          <!-- Kali Linux -->
          <div class="gh-tool-icon float-anim" title="Kali Linux">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="#557C94"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15l-1-2-2 1 1-2-2-1 2-1-1-2 2 1 1-2 1 2 2-1-1 2 2 1-2 1 1 2-2-1-1 2z"/></svg>
          </div>
          <!-- Linux -->
          <div class="gh-tool-icon float-anim-delay" title="Linux">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="#FCC624"><path d="M12.504 0c-.155 0-.315.008-.48.021-4.226.333-3.105 4.807-3.17 6.298-.076 1.092-.3 1.953-1.05 3.02-.885 1.051-2.127 2.75-2.716 4.521-.278.832-.41 1.684-.287 2.489a.424.424 0 00-.11.135c-.26.268-.45.6-.663.839-.199.199-.485.267-.797.4-.313.136-.658.269-.864.68-.09.189-.136.394-.132.602 0 .199.027.4.055.536.058.399.116.728.04.97-.249.68-.28 1.145-.106 1.484.174.334.535.47.94.601.81.2 1.91.135 2.774.6.926.466 1.866.67 2.616.47.526-.116.97-.464 1.208-.946.587-.003 1.23-.269 2.26-.334.699-.058 1.574.267 2.577.2.025.134.063.198.114.333l.003.003c.391.778 1.113 1.368 1.884 1.43.868.07 1.723-.26 2.456-.631.733-.401 1.385-.862 2.096-.945.26-.033.5-.033.705.006.205.033.4.124.544.268.542.533.457 1.433.55 2.228.03.333.06.653.12.906.06.253.136.476.307.636.238.23.606.272.94.186.335-.086.649-.272.953-.465.604-.399 1.168-.906 1.723-.906h.017c.238 0 .475.1.668.293.193.193.35.46.466.726.232.533.366 1.136.524 1.491.079.177.166.332.297.439.131.107.312.166.516.132.407-.067.665-.383.826-.737.16-.354.22-.776.249-1.178.058-.806.03-1.658.307-2.302.545-1.278.666-2.455.408-3.506-.258-1.051-.863-1.979-1.793-2.784l-.003-.003c-.39-.34-.563-.787-.695-1.353-.133-.566-.227-1.248-.505-1.959-.458-1.181-1.425-2.28-2.828-3.197-1.108-.713-2.363-1.273-3.508-1.628-.3-.094-.574-.175-.834-.247-.244-.068-.48-.126-.715-.174.021-.303.038-.623.038-.95 0-1.276-.153-2.586-.568-3.59-.208-.502-.487-.943-.856-1.247-.37-.304-.836-.463-1.323-.449z"/></svg>
          </div>
          <!-- Python -->
          <div class="gh-tool-icon float-anim" title="Python">
            <svg width="26" height="26" viewBox="0 0 24 24"><path d="M14.25.18l.9.2.73.26.59.3.45.32.34.34.25.34.16.33.1.3.04.26.02.2-.01.13V8.5l-.05.63-.13.55-.21.46-.26.38-.3.31-.33.25-.35.19-.35.14-.33.1-.3.07-.26.04-.21.02H8.77l-.69.05-.59.14-.5.22-.41.27-.33.32-.27.35-.2.36-.15.37-.1.35-.07.32-.04.27-.02.21v3.06H3.17l-.21-.03-.28-.07-.32-.12-.35-.18-.36-.26-.36-.36-.35-.46-.32-.59-.28-.73-.21-.88-.14-1.05-.05-1.23.06-1.22.16-1.04.24-.87.32-.71.36-.57.4-.44.42-.33.42-.24.4-.16.36-.1.32-.05.24-.01h.16l.06.01h8.16v-.83H6.18l-.01-2.75-.02-.37.05-.34.11-.31.17-.28.25-.26.31-.23.38-.2.44-.18.51-.15.58-.12.64-.1.71-.06.77-.04.84-.02 1.27.05zm-6.3 1.98l-.23.33-.08.41.08.41.23.34.33.22.41.09.41-.09.33-.22.23-.34.08-.41-.08-.41-.23-.33-.33-.22-.41-.09-.41.09zm13.09 3.95l.28.06.32.12.35.18.36.27.36.35.35.47.32.59.28.73.21.88.14 1.04.05 1.23-.06 1.23-.16 1.04-.24.86-.32.71-.36.57-.4.45-.42.33-.42.24-.4.16-.36.09-.32.05-.24.02-.16-.01h-8.22v.82h5.84l.01 2.76.02.36-.05.34-.11.31-.17.29-.25.25-.31.24-.38.2-.44.17-.51.15-.58.13-.64.09-.71.07-.77.04-.84.01-1.27-.04-1.07-.14-.9-.2-.73-.25-.59-.3-.45-.33-.34-.34-.25-.34-.16-.33-.1-.3-.04-.25-.02-.2.01-.13v-5.34l.05-.64.13-.54.21-.46.26-.38.3-.32.33-.24.35-.2.35-.14.33-.1.3-.06.26-.04.21-.02.13-.01h5.84l.69-.05.59-.14.5-.21.41-.28.33-.32.27-.35.2-.36.15-.36.1-.35.07-.32.04-.28.02-.21V6.07h2.09l.14.01.21.03zm-6.47 14.25l-.23.33-.08.41.08.41.23.33.33.23.41.08.41-.08.33-.23.23-.33.08-.41-.08-.41-.23-.33-.33-.23-.41-.08-.41.08z" fill="#3776AB"/></svg>
          </div>
          <!-- VMware -->
          <div class="gh-tool-icon float-anim-delay" title="VMware">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="#607078"><path d="M6.39 2.4L2.4 6.39V17.6l3.99 3.99h11.22l3.99-3.99V6.39L17.61 2.4H6.39zm1.27 5.04h8.68
