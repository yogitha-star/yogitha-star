<!-- dark.svg -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="100%" height="100%">
  <defs>
    <!-- Fonts -->
    <style>
      @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&amp;family=Inter:wght@400;500;600;700;800&amp;display=swap');
      
      .font-mono { font-family: 'JetBrains Mono', monospace; }
      .font-sans { font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
      
      /* Dark Theme Specific Styles */
      .bg-main { fill: #030712; }
      .panel-bg { fill: #0f172a; fill-opacity: 0.6; }
      .text-primary { fill: #f8fafc; }
      .text-secondary { fill: #94a3b8; }
      .text-muted { fill: #64748b; }
      .text-accent-cyan { fill: #22d3ee; }
      .text-accent-purple { fill: #a855f7; }
      .border-glow { stroke: rgba(255, 255, 255, 0.12); }
      .glass-card { fill: #1e293b; fill-opacity: 0.4; stroke: rgba(255, 255, 255, 0.08); }
      .pill-bg { fill: #1e293b; fill-opacity: 0.6; stroke: rgba(255, 255, 255, 0.1); }
      
      /* Animations */
      @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-8px); }
      }
      @keyframes pulse-slow {
        0%, 100% { opacity: 0.4; }
        50% { opacity: 0.8; }
      }
      .floating { animation: float 6s ease-in-out infinite; }
      .pulsing { animation: pulse-slow 4s ease-in-out infinite; }
    </style>

    <!-- Glowing Filters -->
    <filter id="glow-cyan" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="8" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
    
    <filter id="glow-purple" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="12" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
    
    <filter id="shadow-card" x="-10%" y="-10%" width="120%" height="120%">
      <feDropShadow dx="0" dy="12" stdDeviation="16" flood-color="#000000" flood-opacity="0.5"/>
    </filter>

    <!-- Gradients -->
    <linearGradient id="grad-accent-dark" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7C3AED" />
      <stop offset="50%" stop-color="#22D3EE" />
      <stop offset="100%" stop-color="#10B981" />
    </linearGradient>

    <linearGradient id="grad-border-dark" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.8">
        <animate attributeName="stop-color" values="#7C3AED;#22D3EE;#10B981;#7C3AED" dur="10s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" stop-color="#22D3EE" stop-opacity="0.3">
        <animate attributeName="stop-color" values="#22D3EE;#10B981;#7C3AED;#22D3EE" dur="10s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#10B981" stop-opacity="0.8">
        <animate attributeName="stop-color" values="#10B981;#7C3AED;#22D3EE;#10B981" dur="10s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <radialGradient id="blob-cyan" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.25"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="blob-purple" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.25"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>

    <!-- Dynamic Scanline Pattern -->
    <pattern id="scanlines" width="100" height="4" patternUnits="userSpaceOnUse">
      <line x1="0" y1="0" x2="100" y2="0" stroke="#000000" stroke-opacity="0.3" stroke-width="1.5" />
    </pattern>

    <!-- Terminal Clipping -->
    <clipPath id="left-panel-clip">
      <rect x="30" y="30" width="418" height="550" rx="16" />
    </clipPath>
    <clipPath id="right-panel-clip">
      <rect x="472" y="30" width="678" height="550" rx="16" />
    </clipPath>
    <clipPath id="ascii-clip">
      <rect x="50" y="90" width="378" height="460" />
    </clipPath>
  </defs>

  <!-- ================= BACKGROUND LAYER ================= -->
  <rect width="1180" height="610" rx="24" class="bg-main" />

  <!-- Animated Ambient Background Blobs -->
  <circle cx="150" cy="150" r="250" fill="url(#blob-purple)" class="pulsing">
    <animateTransform attributeName="transform" type="translate" values="0,0; 50,30; 0,0" dur="12s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1000" cy="450" r="300" fill="url(#blob-cyan)" class="pulsing">
    <animateTransform attributeName="transform" type="translate" values="0,0; -40,-50; 0,0" dur="15s" repeatCount="indefinite"/>
  </circle>

  <!-- Background Grid Lines -->
  <g stroke="#ffffff" stroke-opacity="0.03" stroke-width="1">
    <path d="M 0,61 L 1180,61 M 0,122 L 1180,122 M 0,183 L 1180,183 M 0,244 L 1180,244 M 0,305 L 1180,305 M 0,366 L 1180,366 M 0,427 L 1180,427 M 0,488 L 1180,488 M 0,549 L 1180,549" />
    <path d="M 118,0 L 118,610 M 236,0 L 236,610 M 354,0 L 354,610 M 472,0 L 472,610 M 590,0 L 590,610 M 708,0 L 708,610 M 826,0 L 826,610 M 944,0 L 944,610 M 1062,0 L 1062,610" />
  </g>

  <!-- Floating Particles -->
  <g fill="#22d3ee" opacity="0.4">
    <circle cx="100" cy="120" r="1.5">
      <animate attributeName="cy" values="120;100;120" dur="4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.2;0.8;0.2" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1100" cy="200" r="2">
      <animate attributeName="cy" values="200;170;200" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;1;0.3" dur="6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="550" cy="520" r="1.5">
      <animate attributeName="cy" values="520;500;520" dur="5s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- Outer Border Shimmer -->
  <rect x="1" y="1" width="1178" height="608" rx="23" fill="none" stroke="url(#grad-border-dark)" stroke-width="2" opacity="0.7" />

  <!-- ================= LEFT PANEL (CYBER TERMINAL & ASCII) ================= -->
  <g filter="url(#shadow-card)">
    <!-- Panel Glass Base -->
    <rect x="30" y="30" width="418" height="550" rx="16" class="panel-bg" />
    <rect x="30" y="30" width="418" height="550" rx="16" fill="none" class="border-glow" />
  </g>

  <!-- Terminal Header -->
  <g clip-path="url(#left-panel-clip)">
    <rect x="30" y="30" width="418" height="40" fill="#0f172a" fill-opacity="0.8" />
    <line x1="30" y1="70" x2="448" y2="70" stroke="rgba(255,255,255,0.08)" stroke-width="1" />
    <!-- Window Controls -->
    <circle cx="52" cy="50" r="5" fill="#ef4444" opacity="0.8"/>
    <circle cx="68" cy="50" r="5" fill="#f59e0b" opacity="0.8"/>
    <circle cx="84" cy="50" r="5" fill="#10b981" opacity="0.8"/>
    <!-- Terminal Title -->
    <text x="239" y="54" class="font-mono text-muted" font-size="11" text-anchor="middle" letter-spacing="1">profile_matrix.sh</text>
  </g>

  <!-- ASCII Art Portrait with Line-by-Line Reveal & Float Effect -->
  <g clip-path="url(#ascii-clip)">
    <!-- Floating wrapper for ASCII art -->
    <g class="floating">
      <!-- Glow under overlay for Cyberpunk effect -->
      <rect x="60" y="100" width="358" height="430" fill="url(#grad-accent-dark)" opacity="0.08" filter="url(#glow-purple)" />
      
      <!-- ASCII Art Lines (Cyan to Purple Gradient Applied via Fill) -->
      <g class="font-mono" font-size="10" font-weight="bold" fill="url(#grad-accent-dark)" letter-spacing="1.2">
        <!-- Line Reveals via SMIL Clip/Opacity Animation -->
        <text x="55" y="120" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.2s" fill="freeze" />
          ████████████████████████████████████
        </text>
        <text x="55" y="133" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.3s" fill="freeze" />
          ██████████████▀▀▀▀▀▀▀███████████████
        </text>
        <text x="55" y="146" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.4s" fill="freeze" />
          ██████████▀              ▀██████████
        </text>
        <text x="55" y="159" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.5s" fill="freeze" />
          ████████▀    ▄▄▄    ▄▄▄    ▀████████
        </text>
        <text x="55" y="172" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.6s" fill="freeze" />
          ███████    █ prime █  █  dev  █    ███████
        </text>
        <text x="55" y="185" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.7s" fill="freeze" />
          ███████    ▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀    ███████
        </text>
        <text x="55" y="198" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.8s" fill="freeze" />
          ████████▄      ▄▄▄▄▄▄      ▄████████
        </text>
        <text x="55" y="211" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.9s" fill="freeze" />
          ██████████▄  ▀▀  ██  ▀▀  ▄██████████
        </text>
        <text x="55" y="224" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.0s" fill="freeze" />
          ████████████▄▄        ▄▄████████████
        </text>
        <text x="55" y="237" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.1s" fill="freeze" />
          ████████████████████████████████████
        </text>
        
        <!-- Code / System Status Readout under Portrait -->
        <g font-size="9" fill="#94a3b8" opacity="0.8">
          <text x="55" y="270" fill="#22d3ee">> INITIALIZING CORE PROCESSES...</text>
          <text x="55" y="288">> LOADING SYSTEM ARCHITECTURE [OK]</text>
          <text x="55" y="306">> MOUNTING NEURAL PIPELINES [OK]</text>
          <text x="55" y="324">> STACK: TS, NEXT.JS, RUST, PY</text>
          <text x="55" y="342">> STATUS: READY TO BUILD</text>
        </g>

        <!-- Dynamic Simulated Code Block -->
        <g font-size="8" fill="#64748b">
          <text x="55" y="375"><tspan fill="#a855f7">const</tspan> developer = {</text>
          <text x="70" y="390">name: <tspan fill="#10b981">'Senior Architect'</tspan>,</text>
          <text x="70" y="405">mindset: <tspan fill="#10b981">'Always Building'</tspan>,</text>
          <text x="70" y="420">coffeeToCode: <tspan fill="#f59e0b">Infinity</tspan></text>
          <text x="55" y="435">};</text>
        </g>
      </g>
    </g>

    <!-- Scanline Sweep Effect over Terminal -->
    <rect x="30" y="70" width="418" height="510" fill="url(#scanlines)" pointer-events="none" opacity="0.3"/>
    <rect x="30" y="70" width="418" height="20" fill="url(#grad-accent-dark)" opacity="0.15">
      <animate attributeName="y" values="70;560;70" dur="8s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- Terminal Footer / Prompt -->
  <g clip-path="url(#left-panel-clip)">
    <rect x="30" y="540" width="418" height="40" fill="#0f172a" fill-opacity="0.9" />
    <line x1="30" y1="540" x2="448" y2="540" stroke="rgba(255,255,255,0.08)" stroke-width="1" />
    <text x="45" y="565" class="font-mono" font-size="11" fill="#10b981">sys@kernel:~$</text>
    <text x="145" y="565" class="font-mono text-secondary" font-size="11">./run_profile --live</text>
    <rect x="285" y="553" width="7" height="14" fill="#22d3ee">
      <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- ================= RIGHT PANEL (MAIN HERO CONTENT) ================= -->
  <g filter="url(#shadow-card)">
    <rect x="472" y="30" width="678" height="550" rx="16" class="panel-bg" />
    <rect x="472" y="30" width="678" height="550" rx="16" fill="none" class="border-glow" />
  </g>

  <!-- Glass Refraction Light Sweep -->
  <path d="M 472 30 L 700 30 L 472 250 Z" fill="#ffffff" opacity="0.02" clip-path="url(#right-panel-clip)"/>

  <!-- HERO HEADER SECTION -->
  <g transform="translate(512, 75)">
    <!-- Greeting Badge -->
    <g>
      <rect x="0" y="0" width="96" height="26" rx="13" fill="#1e293b" fill-opacity="0.8" stroke="rgba(255,255,255,0.1)"/>
      <circle cx="12" cy="13" r="4" fill="#10b981">
        <animate attributeName="r" values="3;5;3" dur="2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.6;1;0.6" dur="2s" repeatCount="indefinite"/>
      </circle>
      <text x="24" y="17" class="font-mono text-primary" font-size="11" font-weight="500">Hi, there <tspan font-size="12">👋</tspan></text>
    </g>

    <!-- Main Name Title -->
    <text x="0" y="68" class="font-sans text-primary" font-size="44" font-weight="800" letter-spacing="-1">
      I'm <tspan fill="url(#grad-accent-dark)">ALEX RIVERS</tspan>
    </text>

    <!-- Infinite Typing / Erasing Role Subtitle -->
    <g transform="translate(0, 102)">
      <text x="0" y="0" class="font-mono text-secondary" font-size="20" font-weight="500">
        <!-- SVG SMIL Typing Loop Simulation -->
        <tspan fill="#22d3ee">&gt;</tspan> 
        <tspan fill="#f8fafc">
          <animate attributeName="kfill" dur="12s" repeatCount="indefinite" />
          <!-- Animated text via discrete values swapping -->
          <animate attributeName="textContent" 
                   values="Frontend Engineer; Full Stack Developer; Open Source Contributor; UI/UX Architect; AI Systems Engineer; Frontend Engineer" 
                   keyTimes="0; 0.2; 0.4; 0.6; 0.8; 1"
                   dur="12s" 
                   repeatCount="indefinite" />
        </tspan>
      </text>
      <!-- Blinking Typing Cursor -->
      <rect x="340" y="-16" width="10" height="22" fill="#22d3ee">
        <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite"/>
      </rect>
    </g>
  </g>

  <!-- PROFILE INFO SECTION (Sequential Reveal Fade Up) -->
  <g transform="translate(512, 225)">
    <!-- Info Item 1: Location -->
    <g transform="translate(0, 0)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.4s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="0,15; 0,0" dur="0.5s" begin="0.4s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#1e293b"/>
      <path d="M12 6C9.2 6 7 8.2 7 11C7 14.8 12 19 12 19C12 19 17 14.8 17 11C17 8.2 14.8 6 12 6ZM12 12.5C11.2 12.5 10.5 11.8 10.5 11C10.5 10.2 11.2 9.5 12 9.5C12.8 9.5 13.5 10.2 13.5 11C13.5 11.8 12.8 12.5 12 12.5Z" fill="#22d3ee"/>
      <text x="32" y="16" class="font-sans text-secondary" font-size="13"><tspan class="text-muted">Based in:</tspan> San Francisco, CA / Remote</text>
    </g>

    <!-- Info Item 2: Focus -->
    <g transform="translate(280, 0)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.6s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="280,15; 280,0" dur="0.5s" begin="0.6s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#1e293b"/>
      <path d="M12 4V1 4ZM12 20V23 20ZM4 12H1 4ZM20 12H23 20ZM6.3 6.3L4.2 4.2 6.3 6.3ZM17.7 17.7L19.8 19.8 17.7 17.7ZM6.3 17.7L4.2 19.8 6.3 17.7ZM17.7 6.3L19.8 4.2 17.7 6.3Z" stroke="#a855f7" stroke-width="2" stroke-linecap="round"/>
      <text x="32" y="16" class="font-sans text-secondary" font-size="13"><tspan class="text-muted">Focus:</tspan> Design Systems &amp; WebGL</text>
    </g>

    <!-- Info Item 3: Education -->
    <g transform="translate(0, 36)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.8s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="0,51; 0,36" dur="0.5s" begin="0.8s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#1e293b"/>
      <path d="M5 13.18V17.18L12 21L19 17.18V13.18L12 17L5 13.18ZM12 3L1 9L12 15L21 10.09V17H23V9L12 3Z" fill="#10b981"/>
      <text x="32" y="16" class="font-sans text-secondary" font-size="13"><tspan class="text-muted">Edu:</tspan> B.S. Computer Science, Stanford</text>
    </g>

    <!-- Info Item 4: Portfolio/Status -->
    <g transform="translate(280, 36)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="1.0s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="280,51; 280,36" dur="0.5s" begin="1.0s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#1e293b"/>
      <path d="M3.9 12C3.9 10.29 5.29 8.9 7 8.9H11V10.9H7C6.39 10.9 5.9 11.39 5.9 12C5.9 12.61 6.39 13.1 7 13.1H11V15.1H7C5.29 15.1 3.9 13.71 3.9 12ZM8 13H16V11H8V13ZM17 8.9H13V10.9H17C17.61 10.9 18.1 11.39 18.1 12C18.1 12.61 17.61 13.1 17 13.1H13V15.1H17C18.71 15.1 20.1 13.71 20.1 12C20.1 10.29 18.71 8.9 17 8.9Z" fill="#f59e0b"/>
      <text x="32" y="16" class="font-sans text-secondary" font-size="13"><tspan class="text-muted">Portfolio:</tspan> alexrivers.dev</text>
    </g>
  </g>

  <!-- Divider Line -->
  <line x1="512" y1="315" x2="1110" y2="315" stroke="rgba(255,255,255,0.08)" stroke-width="1" />

  <!-- SKILLS SECTION (Glowing Glass Pills) -->
  <g transform="translate(512, 335)">
    <text x="0" y="14" class="font-mono text-muted" font-size="11" font-weight="600" letter-spacing="1">TECHNICAL STACK &amp; CAPABILITIES</text>
    
    <!-- Pills Grid - Row 1 -->
    <g transform="translate(0, 28)">
      <!-- React -->
      <g transform="translate(0, 0)">
        <rect width="78" height="28" rx="14" class="pill-bg"/>
        <text x="39" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">React</text>
      </g>
      <!-- Next.js -->
      <g transform="translate(86, 0)">
        <rect width="84" height="28" rx="14" class="pill-bg"/>
        <text x="42" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Next.js</text>
      </g>
      <!-- TypeScript -->
      <g transform="translate(178, 0)">
        <rect width="102" height="28" rx="14" class="pill-bg" stroke="rgba(34,211,238,0.4)"/>
        <text x="51" y="18" class="font-sans text-accent-cyan" font-size="12" font-weight="600" text-anchor="middle">TypeScript</text>
      </g>
      <!-- Node.js -->
      <g transform="translate(288, 0)">
        <rect width="82" height="28" rx="14" class="pill-bg"/>
        <text x="41" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Node.js</text>
      </g>
      <!-- Tailwind -->
      <g transform="translate(378, 0)">
        <rect width="88" height="28" rx="14" class="pill-bg"/>
        <text x="44" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Tailwind</text>
      </g>
      <!-- GraphQL -->
      <g transform="translate(474, 0)">
        <rect width="90" height="28" rx="14" class="pill-bg"/>
        <text x="45" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">GraphQL</text>
      </g>
    </g>

    <!-- Pills Grid - Row 2 -->
    <g transform="translate(0, 64)">
      <!-- Python -->
      <g transform="translate(0, 0)">
        <rect width="80" height="28" rx="14" class="pill-bg"/>
        <text x="40" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Python</text>
      </g>
      <!-- Rust -->
      <g transform="translate(88, 0)">
        <rect width="68" height="28" rx="14" class="pill-bg" stroke="rgba(168,85,247,0.4)"/>
        <text x="34" y="18" class="font-sans text-accent-purple" font-size="12" font-weight="600" text-anchor="middle">Rust</text>
      </g>
      <!-- Postgres -->
      <g transform="translate(164, 0)">
        <rect width="90" height="28" rx="14" class="pill-bg"/>
        <text x="45" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Postgres</text>
      </g>
      <!-- Docker -->
      <g transform="translate(262, 0)">
        <rect width="80" height="28" rx="14" class="pill-bg"/>
        <text x="40" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Docker</text>
      </g>
      <!-- AWS -->
      <g transform="translate(350, 0)">
        <rect width="64" height="28" rx="14" class="pill-bg"/>
        <text x="32" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">AWS</text>
      </g>
      <!-- WebGL -->
      <g transform="translate(422, 0)">
        <rect width="76" height="28" rx="14" class="pill-bg"/>
        <text x="38" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">WebGL</text>
      </g>
      <!-- Figma -->
      <g transform="translate(506, 0)">
        <rect width="72" height="28" rx="14" class="pill-bg"/>
        <text x="36" y="18" class="font-sans text-primary" font-size="12" font-weight="500" text-anchor="middle">Figma</text>
      </g>
    </g>
  </g>

  <!-- Divider Line -->
  <line x1="512" y1="465" x2="1110" y2="465" stroke="rgba(255,255,255,0.08)" stroke-width="1" />

  <!-- FOOTER SOCIALS SECTION -->
  <g transform="translate(512, 490)">
    <!-- GitHub Button / Card -->
    <g transform="translate(0, 0)" filter="url(#glow-cyan)">
      <rect width="130" height="42" rx="10" class="glass-card"/>
      <!-- GitHub Icon -->
      <path d="M22 13.25C22 8.69 18.31 5 13.75 5C9.19 5 5.5 8.69 5.5 13.25C5.5 16.9 7.87 19.99 11.16 21.09C11.57 21.16 11.72 20.91 11.72 20.69C11.72 20.49 11.71 19.83 11.71 19.01C9.42 19.51 8.93 18.01 8.93 18.01C8.55 17.06 8.01 16.8 8.01 16.8C7.26 16.29 8.07 16.3 8.07 16.3C8.9 16.36 9.34 17.15 9.34 17.15C10.08 18.42 11.28 18.05 11.75 17.84C11.83 17.3 12.04 16.93 12.28 16.72C10.45 16.51 8.53 15.81 8.53 12.66C8.53 11.76 8.85 11.03 9.38 10.45C9.3 10.24 9.02 9.4 9.46 8.27C9.46 8.27 10.15 8.05 11.72 9.11C12.38 8.93 13.08 8.84 13.78 8.84C14.48 8.84 15.18 8.93 15.84 9.11C17.41 8.05 18.09 8.27 18.09 8.27C18.54 9.4 18.26 10.24 18.17 10.45C18.7 11.03 19.02 11.76 19.02 12.66C19.02 15.82 17.09 16.51 15.25 16.71C15.55 16.97 15.82 17.49 15.82 18.3C15.82 19.46 15.81 20.39 15.81 20.69C15.81 20.92 15.96 21.17 16.38 21.09C19.67 19.98 22 16.89 22 13.25Z" fill="#f8fafc"/>
      <text x="42" y="26" class="font-sans text-primary" font-size="13" font-weight="600">GitHub</text>
    </g>

    <!-- LinkedIn Button / Card -->
    <g transform="translate(145, 0)">
      <rect width="130" height="42" rx="10" class="glass-card"/>
      <!-- LinkedIn Icon -->
      <path d="M19 3A2 2 0 0 1 21 5V19A2 2 0 0 1 19 21H5A2 2 0 0 1 3 19V5A2 2 0 0 1 5 3H19M18.5 18.5V13.2C18.5 10.92 17.28 9.87 15.66 9.87C14.35 9.87 13.76 10.59 13.43 11.1V10.05H11V18.5H13.43V13.57C13.43 12.27 14.18 11.89 14.83 11.89C15.5 11.89 16.07 12.4 16.07 13.57V18.5H18.5M6.88 8.56C7.66 8.56 8.3 7.92 8.3 7.14C8.3 6.36 7.66 5.72 6.88 5.72C6.1 5.72 5.46 6.36 5.46 7.14C5.46 7.92 6.1 8.56 6.88 8.56M8.1 18.5V10.05H5.66V18.5H8.1Z" fill="#22d3ee"/>
      <text x="42" y="26" class="font-sans text-primary" font-size="13" font-weight="600">LinkedIn</text>
    </g>

    <!-- Twitter / X Button -->
    <g transform="translate(290, 0)">
      <rect width="130" height="42" rx="10" class="glass-card"/>
      <!-- X Icon -->
      <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z" fill="#f8fafc"/>
      <text x="42" y="26" class="font-sans text-primary" font-size="13" font-weight="600">Twitter / X</text>
    </g>

    <!-- Email Contact Button -->
    <g transform="translate(435, 0)" filter="url(#glow-purple)">
      <rect width="150" height="42" rx="10" fill="url(#grad-accent-dark)"/>
      <!-- Email Icon -->
      <path d="M20 4H4C2.9 4 2.01 4.9 2.01 6L2 18C2 19.1 2.9 20 4 20H20C21.1 20 22 19.1 22 18V6C22 4.9 21.1 4 20 4ZM20 8L12 13L4 8V6L12 11L20 6V8Z" fill="#ffffff"/>
      <text x="42" y="26" class="font-sans" fill="#ffffff" font-size="13" font-weight="700">Get In Touch</text>
    </g>
  </g>
</svg>
<!-- light.svg -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="100%" height="100%">
  <defs>
    <!-- Fonts -->
    <style>
      @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&amp;family=Inter:wght@400;500;600;700;800&amp;display=swap');
      
      .font-mono { font-family: 'JetBrains Mono', monospace; }
      .font-sans { font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
      
      /* Light Theme Specific Styles */
      .bg-main-light { fill: #ffffff; }
      .panel-bg-light { fill: #f8fafc; fill-opacity: 0.8; }
      .text-primary-light { fill: #0f172a; }
      .text-secondary-light { fill: #475569; }
      .text-muted-light { fill: #94a3b8; }
      .text-accent-blue { fill: #2563eb; }
      .text-accent-cyan { fill: #0891b2; }
      .border-glow-light { stroke: rgba(15, 23, 42, 0.08); }
      .glass-card-light { fill: #ffffff; fill-opacity: 0.9; stroke: rgba(15, 23, 42, 0.08); }
      .pill-bg-light { fill: #f1f5f9; fill-opacity: 0.9; stroke: rgba(15, 23, 42, 0.06); }
      
      /* Animations */
      @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-8px); }
      }
      @keyframes pulse-slow {
        0%, 100% { opacity: 0.3; }
        50% { opacity: 0.6; }
      }
      .floating { animation: float 6s ease-in-out infinite; }
      .pulsing { animation: pulse-slow 4s ease-in-out infinite; }
    </style>

    <!-- Soft Light Shadows -->
    <filter id="shadow-card-light" x="-10%" y="-10%" width="120%" height="120%">
      <feDropShadow dx="0" dy="10" stdDeviation="14" flood-color="#0f172a" flood-opacity="0.06"/>
    </filter>
    
    <filter id="glow-blue-light" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="8" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <!-- Light Gradients -->
    <linearGradient id="grad-accent-light" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2563EB" />
      <stop offset="50%" stop-color="#06B6D4" />
      <stop offset="100%" stop-color="#10B981" />
    </linearGradient>

    <linearGradient id="grad-border-light" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2563EB" stop-opacity="0.5">
        <animate attributeName="stop-color" values="#2563EB;#06B6D4;#10B981;#2563EB" dur="10s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" stop-color="#06B6D4" stop-opacity="0.2">
        <animate attributeName="stop-color" values="#06B6D4;#10B981;#2563EB;#06B6D4" dur="10s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#10B981" stop-opacity="0.5">
        <animate attributeName="stop-color" values="#10B981;#2563EB;#06B6D4;#10B981" dur="10s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <radialGradient id="blob-blue-light" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#3b82f6" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="blob-cyan-light" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#06b6d4" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    </radialGradient>

    <!-- Scanline Pattern for Light Mode -->
    <pattern id="scanlines-light" width="100" height="4" patternUnits="userSpaceOnUse">
      <line x1="0" y1="0" x2="100" y2="0" stroke="#0f172a" stroke-opacity="0.04" stroke-width="1" />
    </pattern>

    <!-- Clipping Paths -->
    <clipPath id="left-panel-clip-light">
      <rect x="30" y="30" width="418" height="550" rx="16" />
    </clipPath>
    <clipPath id="right-panel-clip-light">
      <rect x="472" y="30" width="678" height="550" rx="16" />
    </clipPath>
    <clipPath id="ascii-clip-light">
      <rect x="50" y="90" width="378" height="460" />
    </clipPath>
  </defs>

  <!-- ================= BACKGROUND LAYER ================= -->
  <rect width="1180" height="610" rx="24" class="bg-main-light" />

  <!-- Animated Ambient Background Blobs -->
  <circle cx="150" cy="150" r="280" fill="url(#blob-blue-light)" class="pulsing">
    <animateTransform attributeName="transform" type="translate" values="0,0; 40,30; 0,0" dur="12s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1000" cy="450" r="320" fill="url(#blob-cyan-light)" class="pulsing">
    <animateTransform attributeName="transform" type="translate" values="0,0; -30,-40; 0,0" dur="15s" repeatCount="indefinite"/>
  </circle>

  <!-- Background Grid Lines -->
  <g stroke="#0f172a" stroke-opacity="0.03" stroke-width="1">
    <path d="M 0,61 L 1180,61 M 0,122 L 1180,122 M 0,183 L 1180,183 M 0,244 L 1180,244 M 0,305 L 1180,305 M 0,366 L 1180,366 M 0,427 L 1180,427 M 0,488 L 1180,488 M 0,549 L 1180,549" />
    <path d="M 118,0 L 118,610 M 236,0 L 236,610 M 354,0 L 354,610 M 472,0 L 472,610 M 590,0 L 590,610 M 708,0 L 708,610 M 826,0 L 826,610 M 944,0 L 944,610 M 1062,0 L 1062,610" />
  </g>

  <!-- Outer Border Shimmer -->
  <rect x="1" y="1" width="1178" height="608" rx="23" fill="none" stroke="url(#grad-border-light)" stroke-width="2" opacity="0.8" />

  <!-- ================= LEFT PANEL (LIGHT CYBER TERMINAL & ASCII) ================= -->
  <g filter="url(#shadow-card-light)">
    <rect x="30" y="30" width="418" height="550" rx="16" class="panel-bg-light" />
    <rect x="30" y="30" width="418" height="550" rx="16" fill="none" class="border-glow-light" />
  </g>

  <!-- Terminal Header -->
  <g clip-path="url(#left-panel-clip-light)">
    <rect x="30" y="30" width="418" height="40" fill="#e2e8f0" fill-opacity="0.7" />
    <line x1="30" y1="70" x2="448" y2="70" stroke="rgba(15,23,42,0.08)" stroke-width="1" />
    <!-- Window Controls -->
    <circle cx="52" cy="50" r="5" fill="#ef4444" opacity="0.8"/>
    <circle cx="68" cy="50" r="5" fill="#f59e0b" opacity="0.8"/>
    <circle cx="84" cy="50" r="5" fill="#10b981" opacity="0.8"/>
    <!-- Terminal Title -->
    <text x="239" y="54" class="font-mono text-secondary-light" font-size="11" text-anchor="middle" letter-spacing="1">profile_matrix.sh</text>
  </g>

  <!-- ASCII Art Portrait (Light Theme) -->
  <g clip-path="url(#ascii-clip-light)">
    <g class="floating">
      <rect x="60" y="100" width="358" height="430" fill="url(#grad-accent-light)" opacity="0.05" />
      
      <!-- ASCII Art Lines (Blue to Cyan Gradient) -->
      <g class="font-mono" font-size="10" font-weight="bold" fill="url(#grad-accent-light)" letter-spacing="1.2">
        <text x="55" y="120" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.2s" fill="freeze" />
          ████████████████████████████████████
        </text>
        <text x="55" y="133" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.3s" fill="freeze" />
          ██████████████▀▀▀▀▀▀▀███████████████
        </text>
        <text x="55" y="146" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.4s" fill="freeze" />
          ██████████▀              ▀██████████
        </text>
        <text x="55" y="159" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.5s" fill="freeze" />
          ████████▀    ▄▄▄    ▄▄▄    ▀████████
        </text>
        <text x="55" y="172" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.6s" fill="freeze" />
          ███████    █ prime █  █  dev  █    ███████
        </text>
        <text x="55" y="185" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.7s" fill="freeze" />
          ███████    ▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀    ███████
        </text>
        <text x="55" y="198" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.8s" fill="freeze" />
          ████████▄      ▄▄▄▄▄▄      ▄████████
        </text>
        <text x="55" y="211" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.9s" fill="freeze" />
          ██████████▄  ▀▀  ██  ▀▀  ▄██████████
        </text>
        <text x="55" y="224" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.0s" fill="freeze" />
          ████████████▄▄        ▄▄████████████
        </text>
        <text x="55" y="237" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.1s" fill="freeze" />
          ████████████████████████████████████
        </text>
        
        <!-- Code / System Readout -->
        <g font-size="9" fill="#475569" opacity="0.9">
          <text x="55" y="270" fill="#2563eb">> INITIALIZING CORE PROCESSES...</text>
          <text x="55" y="288">> LOADING SYSTEM ARCHITECTURE [OK]</text>
          <text x="55" y="306">> MOUNTING NEURAL PIPELINES [OK]</text>
          <text x="55" y="324">> STACK: TS, NEXT.JS, RUST, PY</text>
          <text x="55" y="342">> STATUS: READY TO BUILD</text>
        </g>

        <!-- Simulated JS Object -->
        <g font-size="8" fill="#64748b">
          <text x="55" y="375"><tspan fill="#2563eb">const</tspan> developer = {</text>
          <text x="70" y="390">name: <tspan fill="#059669">'Senior Architect'</tspan>,</text>
          <text x="70" y="405">mindset: <tspan fill="#059669">'Always Building'</tspan>,</text>
          <text x="70" y="420">coffeeToCode: <tspan fill="#d97706">Infinity</tspan></text>
          <text x="55" y="435">};</text>
        </g>
      </g>
    </g>

    <!-- Scanline Sweep Effect -->
    <rect x="30" y="70" width="418" height="510" fill="url(#scanlines-light)" pointer-events="none"/>
    <rect x="30" y="70" width="418" height="20" fill="url(#grad-accent-light)" opacity="0.08">
      <animate attributeName="y" values="70;560;70" dur="8s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- Terminal Footer -->
  <g clip-path="url(#left-panel-clip-light)">
    <rect x="30" y="540" width="418" height="40" fill="#e2e8f0" fill-opacity="0.9" />
    <line x1="30" y1="540" x2="448" y2="540" stroke="rgba(15,23,42,0.08)" stroke-width="1" />
    <text x="45" y="565" class="font-mono" font-size="11" fill="#059669">sys@kernel:~$</text>
    <text x="145" y="565" class="font-mono text-secondary-light" font-size="11">./run_profile --live</text>
    <rect x="285" y="553" width="7" height="14" fill="#2563eb">
      <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- ================= RIGHT PANEL (MAIN HERO CONTENT LIGHT) ================= -->
  <g filter="url(#shadow-card-light)">
    <rect x="472" y="30" width="678" height="550" rx="16" class="panel-bg-light" />
    <rect x="472" y="30" width="678" height="550" rx="16" fill="none" class="border-glow-light" />
  </g>

  <!-- Glass Refraction Light Sweep -->
  <path d="M 472 30 L 700 30 L 472 250 Z" fill="#ffffff" opacity="0.4" clip-path="url(#right-panel-clip-light)"/>

  <!-- HERO HEADER SECTION -->
  <g transform="translate(512, 75)">
    <!-- Greeting Badge -->
    <g>
      <rect x="0" y="0" width="96" height="26" rx="13" fill="#e2e8f0" fill-opacity="0.8" stroke="rgba(15,23,42,0.08)"/>
      <circle cx="12" cy="13" r="4" fill="#10b981">
        <animate attributeName="r" values="3;5;3" dur="2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.6;1;0.6" dur="2s" repeatCount="indefinite"/>
      </circle>
      <text x="24" y="17" class="font-mono text-primary-light" font-size="11" font-weight="500">Hi, there <tspan font-size="12">👋</tspan></text>
    </g>

    <!-- Main Name Title -->
    <text x="0" y="68" class="font-sans text-primary-light" font-size="44" font-weight="800" letter-spacing="-1">
      I'm <tspan fill="url(#grad-accent-light)">ALEX RIVERS</tspan>
    </text>

    <!-- Infinite Typing / Erasing Role Subtitle -->
    <g transform="translate(0, 102)">
      <text x="0" y="0" class="font-mono text-secondary-light" font-size="20" font-weight="500">
        <tspan fill="#2563eb">&gt;</tspan> 
        <tspan fill="#0f172a">
          <animate attributeName="textContent" 
                   values="Frontend Engineer; Full Stack Developer; Open Source Contributor; UI/UX Architect; AI Systems Engineer; Frontend Engineer" 
                   keyTimes="0; 0.2; 0.4; 0.6; 0.8; 1"
                   dur="12s" 
                   repeatCount="indefinite" />
        </tspan>
      </text>
      <!-- Blinking Typing Cursor -->
      <rect x="340" y="-16" width="10" height="22" fill="#2563eb">
        <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite"/>
      </rect>
    </g>
  </g>

  <!-- PROFILE INFO SECTION -->
  <g transform="translate(512, 225)">
    <!-- Location -->
    <g transform="translate(0, 0)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.4s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="0,15; 0,0" dur="0.5s" begin="0.4s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#e2e8f0"/>
      <path d="M12 6C9.2 6 7 8.2 7 11C7 14.8 12 19 12 19C12 19 17 14.8 17 11C17 8.2 14.8 6 12 6ZM12 12.5C11.2 12.5 10.5 11.8 10.5 11C10.5 10.2 11.2 9.5 12 9.5C12.8 9.5 13.5 10.2 13.5 11C13.5 11.8 12.8 12.5 12 12.5Z" fill="#2563eb"/>
      <text x="32" y="16" class="font-sans text-secondary-light" font-size="13"><tspan class="text-muted-light">Based in:</tspan> San Francisco, CA / Remote</text>
    </g>

    <!-- Focus -->
    <g transform="translate(280, 0)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.6s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="280,15; 280,0" dur="0.5s" begin="0.6s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#e2e8f0"/>
      <path d="M12 4V1 4ZM12 20V23 20ZM4 12H1 4ZM20 12H23 20ZM6.3 6.3L4.2 4.2 6.3 6.3ZM17.7 17.7L19.8 19.8 17.7 17.7ZM6.3 17.7L4.2 19.8 6.3 17.7ZM17.7 6.3L19.8 4.2 17.7 6.3Z" stroke="#0891b2" stroke-width="2" stroke-linecap="round"/>
      <text x="32" y="16" class="font-sans text-secondary-light" font-size="13"><tspan class="text-muted-light">Focus:</tspan> Design Systems &amp; WebGL</text>
    </g>

    <!-- Education -->
    <g transform="translate(0, 36)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="0.8s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="0,51; 0,36" dur="0.5s" begin="0.8s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#e2e8f0"/>
      <path d="M5 13.18V17.18L12 21L19 17.18V13.18L12 17L5 13.18ZM12 3L1 9L12 15L21 10.09V17H23V9L12 3Z" fill="#10b981"/>
      <text x="32" y="16" class="font-sans text-secondary-light" font-size="13"><tspan class="text-muted-light">Edu:</tspan> B.S. Computer Science, Stanford</text>
    </g>

    <!-- Portfolio -->
    <g transform="translate(280, 36)" opacity="0">
      <animate attributeName="opacity" to="1" dur="0.5s" begin="1.0s" fill="freeze" />
      <animateTransform attributeName="transform" type="translate" values="280,51; 280,36" dur="0.5s" begin="1.0s" fill="freeze" />
      <circle cx="12" cy="12" r="12" fill="#e2e8f0"/>
      <path d="M3.9 12C3.9 10.29 5.29 8.9 7 8.9H11V10.9H7C6.39 10.9 5.9 11.39 5.9 12C5.9 12.61 6.39 13.1 7 13.1H11V15.1H7C5.29 15.1 3.9 13.71 3.9 12ZM8 13H16V11H8V13ZM17 8.9H13V10.9H17C17.61 10.9 18.1 11.39 18.1 12C18.1 12.61 17.61 13.1 17 13.1H13V15.1H17C18.71 15.1 20.1 13.71 20.1 12C20.1 10.29 18.71 8.9 17 8.9Z" fill="#d97706"/>
      <text x="32" y="16" class="font-sans text-secondary-light" font-size="13"><tspan class="text-muted-light">Portfolio:</tspan> alexrivers.dev</text>
    </g>
  </g>

  <!-- Divider Line -->
  <line x1="512" y1="315" x2="1110" y2="315" stroke="rgba(15,23,42,0.08)" stroke-width="1" />

  <!-- SKILLS SECTION -->
  <g transform="translate(512, 335)">
    <text x="0" y="14" class="font-mono text-muted-light" font-size="11" font-weight="600" letter-spacing="1">TECHNICAL STACK &amp; CAPABILITIES</text>
    
    <!-- Pills Grid - Row 1 -->
    <g transform="translate(0, 28)">
      <g transform="translate(0, 0)">
        <rect width="78" height="28" rx="14" class="pill-bg-light"/>
        <text x="39" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">React</text>
      </g>
      <g transform="translate(86, 0)">
        <rect width="84" height="28" rx="14" class="pill-bg-light"/>
        <text x="42" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Next.js</text>
      </g>
      <g transform="translate(178, 0)">
        <rect width="102" height="28" rx="14" class="pill-bg-light" stroke="rgba(37,99,235,0.4)"/>
        <text x="51" y="18" class="font-sans text-accent-blue" font-size="12" font-weight="600" text-anchor="middle">TypeScript</text>
      </g>
      <g transform="translate(288, 0)">
        <rect width="82" height="28" rx="14" class="pill-bg-light"/>
        <text x="41" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Node.js</text>
      </g>
      <g transform="translate(378, 0)">
        <rect width="88" height="28" rx="14" class="pill-bg-light"/>
        <text x="44" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Tailwind</text>
      </g>
      <g transform="translate(474, 0)">
        <rect width="90" height="28" rx="14" class="pill-bg-light"/>
        <text x="45" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">GraphQL</text>
      </g>
    </g>

    <!-- Pills Grid - Row 2 -->
    <g transform="translate(0, 64)">
      <g transform="translate(0, 0)">
        <rect width="80" height="28" rx="14" class="pill-bg-light"/>
        <text x="40" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Python</text>
      </g>
      <g transform="translate(88, 0)">
        <rect width="68" height="28" rx="14" class="pill-bg-light" stroke="rgba(8,145,178,0.4)"/>
        <text x="34" y="18" class="font-sans text-accent-cyan" font-size="12" font-weight="600" text-anchor="middle">Rust</text>
      </g>
      <g transform="translate(164, 0)">
        <rect width="90" height="28" rx="14" class="pill-bg-light"/>
        <text x="45" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Postgres</text>
      </g>
      <g transform="translate(262, 0)">
        <rect width="80" height="28" rx="14" class="pill-bg-light"/>
        <text x="40" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Docker</text>
      </g>
      <g transform="translate(350, 0)">
        <rect width="64" height="28" rx="14" class="pill-bg-light"/>
        <text x="32" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">AWS</text>
      </g>
      <g transform="translate(422, 0)">
        <rect width="76" height="28" rx="14" class="pill-bg-light"/>
        <text x="38" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">WebGL</text>
      </g>
      <g transform="translate(506, 0)">
        <rect width="72" height="28" rx="14" class="pill-bg-light"/>
        <text x="36" y="18" class="font-sans text-primary-light" font-size="12" font-weight="500" text-anchor="middle">Figma</text>
      </g>
    </g>
  </g>

  <!-- Divider Line -->
  <line x1="512" y1="465" x2="1110" y2="465" stroke="rgba(15,23,42,0.08)" stroke-width="1" />

  <!-- FOOTER SOCIALS SECTION -->
  <g transform="translate(512, 490)">
    <!-- GitHub Button -->
    <g transform="translate(0, 0)">
      <rect width="130" height="42" rx="10" class="glass-card-light"/>
      <path d="M22 13.25C22 8.69 18.31 5 13.75 5C9.19 5 5.5 8.69 5.5 13.25C5.5 16.9 7.87 19.99 11.16 21.09C11.57 21.16 11.72 20.91 11.72 20.69C11.72 20.49 11.71 19.83 11.71 19.01C9.42 19.51 8.93 18.01 8.93 18.01C8.55 17.06 8.01 16.8 8.01 16.8C7.26 16.29 8.07 16.3 8.07 16.3C8.9 16.36 9.34 17.15 9.34 17.15C10.08 18.42 11.28 18.05 11.75 17.84C11.83 17.3 12.04 16.93 12.28 16.72C10.45 16.51 8.53 15.81 8.53 12.66C8.53 11.76 8.85 11.03 9.38 10.45C9.3 10.24 9.02 9.4 9.46 8.27C9.46 8.27 10.15 8.05 11.72 9.11C12.38 8.93 13.08 8.84 13.78 8.84C14.48 8.84 15.18 8.93 15.84 9.11C17.41 8.05 18.09 8.27 18.09 8.27C18.54 9.4 18.26 10.24 18.17 10.45C18.7 11.03 19.02 11.76 19.02 12.66C19.02 15.82 17.09 16.51 15.25 16.71C15.55 16.97 15.82 17.49 15.82 18.3C15.82 19.46 15.81 20.39 15.81 20.69C15.81 20.92 15.96 21.17 16.38 21.09C19.67 19.98 22 16.89 22 13.25Z" fill="#0f172a"/>
      <text x="42" y="26" class="font-sans text-primary-light" font-size="13" font-weight="600">GitHub</text>
    </g>

    <!-- LinkedIn Button -->
    <g transform="translate(145, 0)">
      <rect width="130" height="42" rx="10" class="glass-card-light"/>
      <path d="M19 3A2 2 0 0 1 21 5V19A2 2 0 0 1 19 21H5A2 2 0 0 1 3 19V5A2 2 0 0 1 5 3H19M18.5 18.5V13.2C18.5 10.92 17.28 9.87 15.66 9.87C14.35 9.87 13.76 10.59 13.43 11.1V10.05H11V18.5H13.43V13.57C13.43 12.27 14.18 11.89 14.83 11.89C15.5 11.89 16.07 12.4 16.07 13.57V18.5H18.5M6.88 8.56C7.66 8.56 8.3 7.92 8.3 7.14C8.3 6.36 7.66 5.72 6.88 5.72C6.1 5.72 5.46 6.36 5.46 7.14C5.46 7.92 6.1 8.56 6.88 8.56M8.1 18.5V10.05H5.66V18.5H8.1Z" fill="#2563eb"/>
      <text x="42" y="26" class="font-sans text-primary-light" font-size="13" font-weight="600">LinkedIn</text>
    </g>

    <!-- Twitter / X Button -->
    <g transform="translate(290, 0)">
      <rect width="130" height="42" rx="10" class="glass-card-light"/>
      <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z" fill="#0f172a"/>
      <text x="42" y="26" class="font-sans text-primary-light" font-size="13" font-weight="600">Twitter / X</text>
    </g>

    <!-- Email Contact Button -->
    <g transform="translate(435, 0)" filter="url(#glow-blue-light)">
      <rect width="150" height="42" rx="10" fill="url(#grad-accent-light)"/>
      <path d="M20 4H4C2.9 4 2.01 4.9 2.01 6L2 18C2 19.1 2.9 20 4 20H20C21.1 20 22 19.1 22 18V6C22 4.9 21.1 4 20 4ZM20 8L12 13L4 8V6L12 11L20 6V8Z" fill="#ffffff"/>
      <text x="42" y="26" class="font-sans" fill="#ffffff" font-size="13" font-weight="700">Get In Touch</text>
    </g>
  </g>
</svg>
