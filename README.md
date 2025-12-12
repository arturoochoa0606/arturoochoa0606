
<!-- 🎬 ANIMACIÓN COMPLETA SVG INCRUSTADA -->
<svg width="800" height="400" viewBox="0 0 800 400"
     xmlns="http://www.w3.org/2000/svg">

<defs>

  <!-- GLOW -->
  <filter id="glow">
    <feGaussianBlur stdDeviation="4" result="blur"/>
    <feMerge>
      <feMergeNode in="blur"/>
      <feMergeNode in="SourceGraphic"/>
    </feMerge>
  </filter>

  <!-- SCANLINES -->
  <pattern id="scan" width="4" height="4" patternUnits="userSpaceOnUse">
    <rect width="4" height="1" fill="rgba(255,255,255,0.06)"/>
  </pattern>

  <style>
    @keyframes fadeIn {
      0% {opacity:0; transform:translateY(40px) scale(.6);}
      60% {opacity:1;}
      100% {transform:translateY(0);}
    }

    @keyframes energyUp {
      0% {height:0; opacity:1;}
      100% {height:180px; opacity:0;}
    }

    @keyframes flash {
      0% {opacity:0;}
      20% {opacity:1;}
      100% {opacity:0;}
    }

    @keyframes suitOn {
      0% {opacity:0; transform:scale(.8);}
      100% {opacity:1; transform:scale(1);}
    }

    @keyframes helmetOn {
      0% {opacity:0; transform:translateY(-20px) scale(.6);}
      40% {opacity:1; transform:translateY(0) scale(1.05);}
      100% {transform:scale(1);}
    }

    @keyframes finalPose {
      0% {transform:scale(1);}
      50% {transform:scale(1.04);}
      100% {transform:scale(1);}
    }
  </style>

</defs>

<!-- FLOOR GLOW -->
<ellipse cx="400" cy="330" rx="240" ry="40" fill="#29f0ff33" filter="url(#glow)"/>

<!-- TRANSFORMACIÓN -->
<g transform="translate(350,60)" filter="url(#glow)">

  <!-- 1) CUERPO HOLOGRÁFICO -->
  <rect x="0" y="0" width="100" height="200"
        fill="#29f0ff44" stroke="#29f0ff88" stroke-width="2"
        style="animation:fadeIn 1.2s ease-out forwards;">
  </rect>

  <rect x="0" y="0" width="100" height="200"
        fill="url(#scan)" opacity="0.6"/>

  <!-- 2) ENERGÍA SUBE -->
  <rect x="0" y="200" width="100" height="100"
        fill="#29f0ff"
        style="animation:energyUp .6s linear forwards .8s;"/>

  <!-- 3) FLASH -->
  <rect x="-60" y="-40" width="220" height="300"
        fill="#ffffff99"
        style="animation:flash .25s ease-out 1.3s forwards; opacity:0;" />

  <!-- 4) ARMADURA -->
  <rect x="0" y="0" width="100" height="200"
        fill="#ff0055aa" stroke="#ff77c4" stroke-width="3"
        style="opacity:0; animation:suitOn .5s ease-out 1.4s forwards;">
  </rect>

  <!-- 5) CASCO -->
  <path d="M10 20 Q50 -20 90 20 L90 80 Q50 110 10 80 Z"
        fill="#000"
        stroke="#29f0ff"
        stroke-width="3"
        style="opacity:0; animation:helmetOn .6s ease-out 1.7s forwards;">
  </path>

  <!-- 6) POSE FINAL -->
  <rect x="0" y="0" width="100" height="200"
        fill="rgba(0,0,0,0)"
        style="animation:finalPose 1.2s ease-in-out 2.2s infinite;">
  </rect>

</g>

</svg>

---
