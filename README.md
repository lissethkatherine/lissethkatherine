<p align="center">
  <svg width="600" height="200" viewBox="0 0 600 200" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
        <feGaussianBlur stdDeviation="3" result="blur" />
        <feComposite in="SourceGraphic" in2="blur" operator="over" />
      </filter>
      
      <linearGradient id="grad" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" style="stop-color:#8A2BE2;stop-opacity:1" />
        <stop offset="50%" style="stop-color:#FF1493;stop-opacity:1" />
        <stop offset="100%" style="stop-color:#00BFFF;stop-opacity:1" />
      </linearGradient>
    </defs>

    <rect x="50" y="40" width="500" height="120" rx="20" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.2)" stroke-width="1" />

    <g transform="translate(150, 100)">
      <g>
        <path d="M0 30 L-30 0 A20 20 0 0 1 0 -20 A20 20 0 0 1 30 0 Z" fill="url(#grad)" filter="url(#glow)">
          <animateTransform 
            attributeName="transform" 
            type="scale" 
            values="1,1; 0,1; 1,1; 0,1; 1,1" 
            dur="3s" 
            repeatCount="indefinite" />
        </path>
      </g>
    </g>

    <text x="230" y="115" font-family="Arial, sans-serif" font-weight="bold" font-size="45" fill="white" style="text-shadow: 0 0 10px #FF1493;">
      TU_NOMBRE
      <animate attributeName="opacity" values="0.8;1;0.8" dur="2s" repeatCount="indefinite" />
    </text>
  </svg>
</p>
