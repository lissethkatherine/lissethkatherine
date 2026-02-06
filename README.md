<div align="center">
  <svg width="600" height="200" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" style="stop-color:#ff006e;stop-opacity:1">
          <animate attributeName="stop-color" values="#ff006e;#8338ec;#3a86ff;#ff006e" dur="3s" repeatCount="indefinite"/>
        </stop>
        <stop offset="100%" style="stop-color:#3a86ff;stop-opacity:1">
          <animate attributeName="stop-color" values="#3a86ff;#ff006e;#8338ec;#3a86ff" dur="3s" repeatCount="indefinite"/>
        </stop>
      </linearGradient>
      <filter id="glow">
        <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
        <feMerge>
          <feMergeNode in="coloredBlur"/>
          <feMergeNode in="SourceGraphic"/>
        </feMerge>
      </filter>
    </defs>
    
    <rect width="600" height="200" fill="#1a1a2e" rx="15"/>
    
    <g transform="translate(80, 20)">
      <path d="M 45,65 C 45,50 35,40 25,40 C 15,40 10,45 10,55 C 10,45 5,40 -5,40 C -15,40 -20,50 -20,65 C -20,90 10,110 10,110 C 10,110 45,90 45,65 Z" 
            fill="url(#grad1)" filter="url(#glow)" transform="scale(1.5)">
        <animateTransform attributeName="transform" type="rotate" from="0 10 65" to="360 10 65" dur="6s" repeatCount="indefinite" additive="sum"/>
        <animateTransform attributeName="transform" type="scale" values="1.5;1.6;1.5" dur="2s" repeatCount="indefinite" additive="sum"/>
      </path>
    </g>
    
    <text x="220" y="110" font-family="'Segoe UI', Arial, sans-serif" font-size="55" font-weight="900" fill="url(#grad1)" filter="url(#glow)">
      TU NOMBRE
    </text>
    <text x="220" y="140" font-family="'Segoe UI', Arial, sans-serif" font-size="16" fill="#ffffff" opacity="0.7" letter-spacing="3">
      DEVELOPER
    </text>
  </svg>
</div>
