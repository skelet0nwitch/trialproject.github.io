
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Collapse — The Science of Becoming Real</title>
    <meta name="description"
        content="Where neuroplasticity meets quantum physics. A rigorous, mentored editorial on the mechanics of manifestation.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=Space+Grotesk:wght@300;400;500;600&family=Bodoni+Moda:ital,opsz,wght@0,6..96,400;0,6..96,700;1,6..96,400;1,6..96,700&display=swap"
        rel="stylesheet">
    <style>
        /* ── TOKENS ───────────────────────────────────────────── */
        :root {
            --ice: #C8E0D5;
            --ice-deep: #7BAAA0;
            --sage: #4A6858;
            --forest: #1A2820;
            --midnight: #0B0F0D;
            --lav: #B8AECA;
            --lav-pale: #DDD8E8;
            --parch: #E6DDC8;
            --terra: #C47060;
            --bg: #0B110F;
            --bg2: #131A17;
            --bg3: #1C2620;
            --txt: #E2EDE8;
            --txt-dim: #7A9A90;
            --f-syne: 'Syne', sans-serif;
            --f-space: 'Space Grotesk', sans-serif;
            --f-bod: 'Bodoni Moda', serif;
        }

        *,
        *::before,
        *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0
        }

        html {
            scroll-behavior: smooth
        }

        body {
            background: var(--bg);
            color: var(--txt);
            font-family: var(--f-space);
            font-weight: 300;
            overflow-x: hidden;
            line-height: 1.65
        }

        ::selection {
            background: var(--sage);
            color: var(--ice)
        }

        ::-webkit-scrollbar {
            width: 3px
        }

        ::-webkit-scrollbar-thumb {
            background: var(--ice-deep)
        }

        /* ── NOISE TEXTURE ───────────────────────────────────── */
        body::before {
            content: '';
            position: fixed;
            inset: 0;
            z-index: 0;
            pointer-events: none;
            opacity: .045;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
            mix-blend-mode: overlay;
        }

        /* ── HERO ─────────────────────────────────────────────── */
        .hero {
            min-height: 100svh;
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: auto auto;
            position: relative;
            overflow: hidden;
            padding: 60px 60px 80px;
            gap: 0;
            align-items: end;
        }

        .hero-bg {
            position: absolute;
            inset: 0;
            z-index: 0;
            background:
                radial-gradient(ellipse 60% 55% at 80% 30%, rgba(72, 140, 120, .18), transparent),
                radial-gradient(ellipse 50% 60% at 10% 80%, rgba(184, 174, 202, .10), transparent),
                var(--bg);
        }

        .hero-img {
            position: absolute;
            top: 0;
            right: 0;
            width: 52%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
            clip-path: polygon(8% 0, 100% 0, 100% 100%, 0% 100%);
        }

        .hero-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            filter: grayscale(.4) brightness(.55) contrast(1.2);
            mix-blend-mode: luminosity;
        }

        /* CSS art fallback for hero — animated quantum field */
        .hero-canvas {
            position: absolute;
            top: 0;
            right: 0;
            width: 52%;
            height: 100%;
            z-index: 1;
            clip-path: polygon(8% 0, 100% 0, 100% 100%, 0% 100%);
            overflow: hidden;
            background: var(--forest);
        }

        .hero-canvas::after {
            content: '';
            position: absolute;
            inset: 0;
            background:
                radial-gradient(circle 2px at 20% 30%, var(--ice), .5px, transparent 2px),
                radial-gradient(circle 1px at 70% 15%, var(--lav), .5px, transparent 1px),
                radial-gradient(circle 1.5px at 55% 60%, var(--ice-deep), .5px, transparent 2px),
                radial-gradient(circle 1px at 30% 75%, var(--lav), .5px, transparent 1px),
                radial-gradient(circle 2px at 85% 80%, var(--ice), .5px, transparent 2px),
                radial-gradient(ellipse 80% 80% at 50% 50%, rgba(72, 140, 120, .04), transparent);
        }

        .particles-svg {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%;
        }

        .hero-nav {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            z-index: 10;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 28px 60px;
        }

        .nav-logo {
            font-family: var(--f-syne);
            font-size: .75rem;
            font-weight: 800;
            letter-spacing: .35em;
            text-transform: uppercase;
            color: var(--ice-deep)
        }

        .nav-issue {
            font-size: .65rem;
            letter-spacing: .25em;
            text-transform: uppercase;
            color: var(--txt-dim)
        }

        .hero-left {
            grid-column: 1;
            grid-row: 1/3;
            z-index: 5;
            padding-top: 80px;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding-bottom: 0
        }

        .hero-right {
            grid-column: 2;
            grid-row: 2;
            z-index: 5;
            display: flex;
            align-items: flex-end;
            justify-content: flex-end;
            padding-bottom: 0
        }

        .hero-label {
            font-family: var(--f-space);
            font-size: .68rem;
            font-weight: 500;
            letter-spacing: .45em;
            text-transform: uppercase;
            color: var(--ice);
            margin-bottom: 24px;
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .hero-label::before {
            content: '';
            width: 32px;
            height: 1px;
            background: var(--ice-deep)
        }

        .hero-title {
            font-family: var(--f-syne);
            font-size: clamp(5rem, 11vw, 9.5rem);
            font-weight: 800;
            line-height: .88;
            letter-spacing: -.04em;
            text-transform: uppercase;
            color: var(--txt);
        }

        .hero-title .outline {
            -webkit-text-stroke: 1px var(--ice-deep);
            color: transparent
        }

        .hero-title .ice-word {
            color: var(--ice)
        }

        .hero-sub {
            margin-top: 36px;
            max-width: 420px;
            font-family: var(--f-bod);
            font-size: 1.15rem;
            font-style: italic;
            color: var(--txt-dim);
            line-height: 1.7;
        }

        .hero-sidebar {
            font-family: var(--f-space);
            font-size: .7rem;
            letter-spacing: .18em;
            text-transform: uppercase;
            color: var(--txt-dim);
            writing-mode: vertical-rl;
            text-orientation: mixed;
            transform: rotate(180deg);
        }

        /* ── MARQUEE ──────────────────────────────────────────── */
        .marquee-wrap {
            width: 100%;
            overflow: hidden;
            background: var(--ice);
            padding: 18px 0;
            position: relative;
            z-index: 5;
        }

        .marquee-inner {
            display: flex;
            gap: 60px;
            width: max-content;
            animation: marquee 28s linear infinite;
        }

        .marquee-inner span {
            font-family: var(--f-syne);
            font-weight: 800;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: .15em;
            color: var(--forest);
            white-space: nowrap;
        }

        .marquee-inner .sep {
            color: var(--sage)
        }

        @keyframes marquee {
            0% {
                transform: translateX(0)
            }

            100% {
                transform: translateX(-50%)
            }
        }

        /* ── SECTIONS ─────────────────────────────────────────── */
        .s {
            padding: 100px 60px;
            position: relative;
            z-index: 2
        }

        .grid-12 {
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 24px;
            max-width: 1400px;
            margin: 0 auto
        }

        /* ── INTRO ────────────────────────────────────────────── */
        .intro-text {
            grid-column: 1/8
        }

        .intro-aside {
            grid-column: 9/13;
            display: flex;
            flex-direction: column;
            justify-content: flex-end
        }

        .big-pull {
            font-family: var(--f-syne);
            font-size: clamp(2.5rem, 4vw, 3.8rem);
            font-weight: 700;
            line-height: 1.05;
            color: var(--txt);
            letter-spacing: -.02em;
        }

        .big-pull em {
            font-family: var(--f-bod);
            font-style: italic;
            color: var(--ice);
            font-size: 1.15em
        }

        .prose {
            font-size: 1.05rem;
            color: var(--txt-dim);
            line-height: 1.85;
            max-width: 580px
        }

        .prose p+p {
            margin-top: 18px
        }

        .prose strong {
            color: var(--txt);
            font-weight: 500
        }

        .prose em {
            color: var(--ice-deep);
            font-style: italic
        }

        .aside-stat {
            border-top: 1px solid rgba(200, 224, 213, .15);
            padding-top: 24px;
            margin-top: 32px;
        }

        .aside-num {
            font-family: var(--f-syne);
            font-size: 5rem;
            font-weight: 800;
            color: transparent;
            -webkit-text-stroke: 1px var(--ice-deep);
            line-height: 1;
        }

        .aside-label {
            font-size: .7rem;
            letter-spacing: .3em;
            text-transform: uppercase;
            color: var(--txt-dim);
            margin-top: 8px
        }

        /* ── CHAPTER HEADER ───────────────────────────────────── */
        .ch {
            display: flex;
            align-items: baseline;
            gap: 20px;
            margin-bottom: 56px
        }

        .ch-num {
            font-family: var(--f-syne);
            font-size: clamp(5rem, 8vw, 7rem);
            font-weight: 800;
            color: var(--bg3);
            line-height: 1;
            -webkit-text-stroke: 1px var(--lav);
            flex-shrink: 0
        }

        .ch-block {
            border-bottom: 1px solid rgba(255, 255, 255, .08);
            padding-bottom: 18px;
            flex: 1
        }

        .ch-eye {
            font-size: .65rem;
            letter-spacing: .4em;
            text-transform: uppercase;
            color: var(--terra);
            margin-bottom: 6px
        }

        .ch-title {
            font-family: var(--f-syne);
            font-size: clamp(1.6rem, 3vw, 2.4rem);
            font-weight: 700;
            color: var(--txt);
            line-height: 1.1
        }

        .ch-title em {
            font-family: var(--f-bod);
            font-style: italic;
            color: var(--ice)
        }

        /* ── CALLOUT BOX ──────────────────────────────────────── */
        .callout {
            padding: 40px;
            border-radius: 2px;
            background: linear-gradient(135deg, rgba(74, 104, 88, .18), rgba(184, 174, 202, .08));
            border: 1px solid rgba(200, 224, 213, .12);
            margin: 28px 0;
        }

        .callout-eye {
            font-size: .6rem;
            letter-spacing: .4em;
            text-transform: uppercase;
            color: var(--lav);
            margin-bottom: 14px
        }

        .callout p {
            font-family: var(--f-bod);
            font-style: italic;
            font-size: 1.1rem;
            color: var(--txt);
            line-height: 1.7
        }

        .callout p strong {
            font-style: normal;
            color: var(--ice)
        }

        /* ── CSS ART PANELS ───────────────────────────────────── */
        .art-panel {
            position: relative;
            overflow: hidden;
            background: var(--bg2);
            border-radius: 2px;
        }

        .art-panel--wave {
            background: linear-gradient(160deg, #0B0F0D 60%, #1A2820);
            aspect-ratio: 4/3
        }

        .art-panel--net {
            background: #0B110F;
            aspect-ratio: 3/4
        }

        .wave-svg,
        .net-svg {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%
        }

        .art-cap {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 20px 24px;
            background: linear-gradient(to top, rgba(11, 15, 13, .9), transparent);
            font-size: .65rem;
            letter-spacing: .25em;
            text-transform: uppercase;
            color: var(--ice-deep);
        }

        /* ── WIDE VISUAL BLOCK ────────────────────────────────── */
        .wide-block {
            grid-column: 1/13;
            display: grid;
            grid-template-columns: 5fr 7fr;
            gap: 0;
            min-height: 540px;
            margin: 40px 0
        }

        .wide-block-text {
            background: var(--bg2);
            padding: 60px 50px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            border-right: 1px solid rgba(200, 224, 213, .08);
        }

        .wide-block-art {
            position: relative;
            overflow: hidden
        }

        .wide-block-art canvas,
        .wide-block-art .art-full {
            position: absolute;
            inset: 0;
            width: 100%;
            height: 100%;
        }

        .art-full {
            background: var(--forest);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* ── BARRIER CARDS ────────────────────────────────────── */
        .barriers {
            grid-column: 1/13;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2px;
            margin: 60px 0
        }

        .barrier-card {
            padding: 48px 44px;
            background: var(--bg2);
            border-left: 3px solid transparent;
            transition: border-color .35s, background .35s;
            cursor: default;
        }

        .barrier-card:hover {
            border-left-color: var(--terra);
            background: var(--bg3)
        }

        .barrier-tag {
            display: inline-block;
            padding: 5px 14px;
            margin-bottom: 18px;
            background: rgba(196, 112, 96, .15);
            border: 1px solid rgba(196, 112, 96, .3);
            font-size: .62rem;
            letter-spacing: .3em;
            text-transform: uppercase;
            color: var(--terra);
            border-radius: 30px;
        }

        .barrier-card h3 {
            font-family: var(--f-syne);
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--txt);
            margin-bottom: 14px
        }

        .barrier-card p {
            font-size: .95rem;
            color: var(--txt-dim);
            line-height: 1.8
        }

        .barrier-card p strong {
            color: var(--txt)
        }

        /* ── HELPERS GRID ─────────────────────────────────────── */
        .helpers {
            grid-column: 1/13;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
            margin: 20px 0
        }

        .helper-card {
            padding: 36px 32px;
            background: var(--bg2);
            border-top: 2px solid var(--lav);
            transition: transform .4s;
        }

        .helper-card:hover {
            transform: translateY(-8px)
        }

        .helper-n {
            font-family: var(--f-syne);
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--ice), var(--lav));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1;
            margin-bottom: 16px;
        }

        .helper-card h3 {
            font-family: var(--f-syne);
            font-size: 1.05rem;
            font-weight: 700;
            margin-bottom: 12px;
            color: var(--txt)
        }

        .helper-card p {
            font-size: .88rem;
            color: var(--txt-dim);
            line-height: 1.75
        }

        .helper-card p strong {
            color: var(--ice-deep)
        }

        /* ── STATEMENT BAND ───────────────────────────────────── */
        .statement-band {
            padding: 110px 60px;
            background: var(--forest);
            clip-path: polygon(0 6%, 100% 0, 100% 94%, 0 100%);
            margin: 80px 0;
            text-align: center;
            position: relative;
            z-index: 2;
        }

        .st-label {
            font-size: .65rem;
            letter-spacing: .45em;
            text-transform: uppercase;
            color: var(--ice-deep);
            margin-bottom: 24px
        }

        .st-big {
            font-family: var(--f-syne);
            font-weight: 800;
            font-size: clamp(3rem, 6vw, 5.5rem);
            line-height: .88;
            text-transform: uppercase;
            letter-spacing: -.03em
        }

        .st-big .outline {
            -webkit-text-stroke: 1px rgba(200, 224, 213, .4);
            color: transparent
        }

        .st-big .fill {
            color: var(--ice)
        }

        .st-note {
            margin-top: 36px;
            font-family: var(--f-bod);
            font-style: italic;
            font-size: 1.2rem;
            color: var(--txt-dim);
            max-width: 620px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7
        }

        /* ── CLOSING ──────────────────────────────────────────── */
        .closing {
            grid-column: 3/11;
            text-align: center;
            padding: 60px 0
        }

        .closing h2 {
            font-family: var(--f-syne);
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 700;
            margin-bottom: 28px;
            line-height: 1.1
        }

        .closing h2 em {
            font-family: var(--f-bod);
            font-style: italic;
            color: var(--lav)
        }

        .closing p {
            font-size: 1.05rem;
            color: var(--txt-dim);
            line-height: 1.85;
            margin-bottom: 18px
        }

        .closing p strong {
            color: var(--txt)
        }

        /* ── FOOTER ───────────────────────────────────────────── */
        footer {
            padding: 70px 60px 50px;
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            border-top: 1px solid rgba(200, 224, 213, .1);
            position: relative;
            z-index: 2;
        }

        .f-logo {
            font-family: var(--f-syne);
            font-size: 5rem;
            font-weight: 800;
            color: transparent;
            -webkit-text-stroke: 1px var(--bg3);
            /* invisible — just the shape */
            background: linear-gradient(180deg, var(--ice-deep), var(--lav));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1;
        }

        .f-info {
            font-size: .7rem;
            letter-spacing: .2em;
            text-transform: uppercase;
            color: var(--txt-dim)
        }

        .f-info p+p {
            margin-top: 8px
        }

        /* ── REVEAL ───────────────────────────────────────────── */
        .r {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity .8s ease, transform .8s ease
        }

        .r.on {
            opacity: 1;
            transform: none
        }

        .r.d1 {
            transition-delay: .1s
        }

        .r.d2 {
            transition-delay: .2s
        }

        .r.d3 {
            transition-delay: .32s
        }

        /* ── RESPONSIVE ───────────────────────────────────────── */
        @media(max-width:900px) {
            .hero {
                grid-template-columns: 1fr;
                padding: 80px 24px 60px
            }

            .hero-img,
            .hero-canvas {
                display: none
            }

            .hero-right {
                display: none
            }

            .s {
                padding: 70px 24px
            }

            .grid-12 {
                grid-template-columns: 1fr
            }

            .intro-text,
            .intro-aside,
            .wide-block,
            .barriers,
            .helpers,
            .closing {
                grid-column: 1 !important
            }

            .wide-block {
                grid-template-columns: 1fr
            }

            .barriers {
                grid-template-columns: 1fr
            }

            .helpers {
                grid-template-columns: 1fr
            }

            .hero-nav {
                padding: 20px 24px
            }

            footer {
                flex-direction: column;
                gap: 28px;
                padding: 50px 24px 40px
            }
        }
    </style>
</head>

<body>

    <!-- HERO -->
    <nav class="hero-nav">
        <span class="nav-logo">Collapse</span>
        <span class="nav-issue">Vol. II — Quantum &amp; Neural</span>
    </nav>

    <header class="hero">
        <div class="hero-bg" aria-hidden="true"></div>

        <!-- CSS-art quantum field (no image needed) -->
        <div class="hero-canvas" aria-hidden="true">
            <svg class="particles-svg" viewBox="0 0 600 800" preserveAspectRatio="xMidYMid slice">
                <defs>
                    <radialGradient id="pg" cx="50%" cy="50%" r="50%">
                        <stop offset="0%" stop-color="#C8E0D5" stop-opacity=".9" />
                        <stop offset="100%" stop-color="#C8E0D5" stop-opacity="0" />
                    </radialGradient>
                    <filter id="glow">
                        <feGaussianBlur stdDeviation="3" result="b" />
                        <feMerge>
                            <feMergeNode in="b" />
                            <feMergeNode in="SourceGraphic" />
                        </feMerge>
                    </filter>
                </defs>
                <!-- Neural lines -->
                <g stroke="#4A6858" stroke-width=".6" fill="none" opacity=".5">
                    <path d="M80,200 Q200,180 300,260 Q400,340 520,300" />
                    <path d="M50,400 Q170,360 280,420 Q390,480 550,440" />
                    <path d="M120,600 Q240,550 340,610 Q440,670 560,630" />
                    <path d="M300,100 Q310,300 290,500 Q270,700 310,780" />
                    <path d="M160,50 Q240,200 220,380 Q200,560 250,700" />
                    <path d="M450,80 Q420,250 460,420 Q500,590 470,750" />
                </g>
                <!-- Nodes -->
                <g filter="url(#glow)">
                    <circle cx="300" cy="260" r="5" fill="#C8E0D5" opacity=".8">
                        <animate attributeName="opacity" values=".3;.9;.3" dur="4s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="520" cy="300" r="3.5" fill="#B8AECA" opacity=".7">
                        <animate attributeName="opacity" values=".5;1;.5" dur="3.2s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="280" cy="420" r="4" fill="#C8E0D5" opacity=".6">
                        <animate attributeName="opacity" values=".2;.8;.2" dur="5s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="550" cy="440" r="3" fill="#7BAAA0" opacity=".9">
                        <animate attributeName="opacity" values=".6;1;.6" dur="2.8s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="340" cy="610" r="4.5" fill="#B8AECA" opacity=".7">
                        <animate attributeName="opacity" values=".4;.9;.4" dur="3.7s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="250" cy="700" r="3" fill="#C8E0D5" opacity=".5">
                        <animate attributeName="opacity" values=".2;.7;.2" dur="4.5s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="220" cy="380" r="4" fill="#7BAAA0" opacity=".8">
                        <animate attributeName="opacity" values=".3;.9;.3" dur="3.9s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="460" cy="420" r="3.5" fill="#C8E0D5" opacity=".6">
                        <animate attributeName="opacity" values=".5;1;.5" dur="2.5s" repeatCount="indefinite" />
                    </circle>
                </g>
                <!-- Drifting particles -->
                <g fill="#C8E0D5" opacity=".4">
                    <circle cx="100" cy="150" r="1.5">
                        <animate attributeName="cy" values="150;130;150" dur="7s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="430" cy="200" r="1">
                        <animate attributeName="cy" values="200;180;200" dur="9s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="200" cy="500" r="1.5">
                        <animate attributeName="cy" values="500;475;500" dur="6s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="490" cy="560" r="1">
                        <animate attributeName="cy" values="560;540;560" dur="8s" repeatCount="indefinite" />
                    </circle>
                    <circle cx="370" cy="700" r="1.2">
                        <animate attributeName="cy" values="700;680;700" dur="10s" repeatCount="indefinite" />
                    </circle>
                </g>
                <!-- Quantum wave -->
                <path d="M0,400 Q75,370 150,400 Q225,430 300,400 Q375,370 450,400 Q525,430 600,400" stroke="#7BAAA0"
                    stroke-width="1.2" fill="none" opacity=".3" stroke-dasharray="6 4">
                    <animate attributeName="d" values="M0,400 Q75,370 150,400 Q225,430 300,400 Q375,370 450,400 Q525,430 600,400;
                  M0,400 Q75,430 150,400 Q225,370 300,400 Q375,430 450,400 Q525,370 600,400;
                  M0,400 Q75,370 150,400 Q225,430 300,400 Q375,370 450,400 Q525,430 600,400" dur="6s"
                        repeatCount="indefinite" />
                </path>
                <!-- Gradient overlay -->
                <rect width="600" height="800" fill="url(#pg)" opacity=".04" />
                <rect width="600" height="800" fill="#0B110F" opacity=".35" />
            </svg>
        </div>

        <div class="hero-left">
            <div class="hero-label">A rigorous editorial</div>
            <h1 class="hero-title">
                COL<span class="outline">LAPSE</span><br>
                <span class="ice-word">INTO</span><br>
                REAL
            </h1>
            <p class="hero-sub">The intersection of quantum physics and neuroplasticity — and why it is the most honest
                thing ever said about manifestation.</p>
        </div>
        <div class="hero-right">
            <div class="hero-sidebar">Neuroplasticity × Quantum Mechanics × Manifestation</div>
        </div>
    </header>

    <!-- MARQUEE -->
    <div class="marquee-wrap" aria-hidden="true">
        <div class="marquee-inner">
            <span>Observer Effect</span><span class="sep">✦</span>
            <span>Neural Rewiring</span><span class="sep">✦</span>
            <span>Wave Collapse</span><span class="sep">✦</span>
            <span>Quantum Field</span><span class="sep">✦</span>
            <span>Hebbian Learning</span><span class="sep">✦</span>
            <span>Synaptic Density</span><span class="sep">✦</span>
            <span>Coherence</span><span class="sep">✦</span>
            <span>Observer Effect</span><span class="sep">✦</span>
            <span>Neural Rewiring</span><span class="sep">✦</span>
            <span>Wave Collapse</span><span class="sep">✦</span>
            <span>Quantum Field</span><span class="sep">✦</span>
            <span>Hebbian Learning</span><span class="sep">✦</span>
            <span>Synaptic Density</span><span class="sep">✦</span>
            <span>Coherence</span><span class="sep">✦</span>
        </div>
    </div>

    <!-- INTRO -->
    <section class="s">
        <div class="grid-12">
            <div class="intro-text r">
                <p class="big-pull">The universe does not respond to wishes. It responds to <em>coherence.</em></p>
                <div class="prose" style="margin-top:36px">
                    <p>Here is the honest version of manifestation: it is not mystical. It is the convergence of two of
                        the most rigorously tested fields in modern science — <strong>Quantum Mechanics</strong> and
                        <strong>Neuroplasticity</strong> — operating simultaneously within you.</p>
                    <p>Quantum Physics describes the nature of reality before it is observed. Neuroplasticity describes
                        the architecture of the instrument doing the observing. When you understand both, manifestation
                        stops being a belief system and becomes an <strong>engineering discipline.</strong></p>
                    <p>This editorial walks you through the logic, the application, the barriers that silently sabotage
                        the process, and the precise conditions under which it becomes reliable.</p>
                </div>
            </div>
            <div class="intro-aside r d2">
                <div class="art-panel art-panel--wave" style="aspect-ratio:3/4">
                    <svg class="wave-svg" viewBox="0 0 400 530" preserveAspectRatio="xMidYMid slice">
                        <defs>
                            <linearGradient id="wg" x1="0" y1="0" x2="0" y2="1">
                                <stop offset="0%" stop-color="#C8E0D5" stop-opacity=".7" />
                                <stop offset="100%" stop-color="#B8AECA" stop-opacity=".2" />
                            </linearGradient>
                        </defs>
                        <g fill="none" stroke="url(#wg)" stroke-width="1">
                            <path d="M0,100 Q100,60 200,100 Q300,140 400,100">
                                <animate attributeName="d"
                                    values="M0,100 Q100,60 200,100 Q300,140 400,100;M0,100 Q100,140 200,100 Q300,60 400,100;M0,100 Q100,60 200,100 Q300,140 400,100"
                                    dur="5s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,150 Q100,110 200,150 Q300,190 400,150">
                                <animate attributeName="d"
                                    values="M0,150 Q100,110 200,150 Q300,190 400,150;M0,150 Q100,190 200,150 Q300,110 400,150;M0,150 Q100,110 200,150 Q300,190 400,150"
                                    dur="5.5s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,200 Q100,160 200,200 Q300,240 400,200">
                                <animate attributeName="d"
                                    values="M0,200 Q100,160 200,200 Q300,240 400,200;M0,200 Q100,240 200,200 Q300,160 400,200;M0,200 Q100,160 200,200 Q300,240 400,200"
                                    dur="6s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,250 Q100,210 200,250 Q300,290 400,250">
                                <animate attributeName="d"
                                    values="M0,250 Q100,210 200,250 Q300,290 400,250;M0,250 Q100,290 200,250 Q300,210 400,250;M0,250 Q100,210 200,250 Q300,290 400,250"
                                    dur="4.8s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,300 Q100,260 200,300 Q300,340 400,300">
                                <animate attributeName="d"
                                    values="M0,300 Q100,260 200,300 Q300,340 400,300;M0,300 Q100,340 200,300 Q300,260 400,300;M0,300 Q100,260 200,300 Q300,340 400,300"
                                    dur="5.2s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,350 Q100,310 200,350 Q300,390 400,350">
                                <animate attributeName="d"
                                    values="M0,350 Q100,310 200,350 Q300,390 400,350;M0,350 Q100,390 200,350 Q300,310 400,350;M0,350 Q100,310 200,350 Q300,390 400,350"
                                    dur="4.5s" repeatCount="indefinite" />
                            </path>
                            <path d="M0,400 Q100,360 200,400 Q300,440 400,400">
                                <animate attributeName="d"
                                    values="M0,400 Q100,360 200,400 Q300,440 400,400;M0,400 Q100,440 200,400 Q300,360 400,400;M0,400 Q100,360 200,400 Q300,440 400,400"
                                    dur="5.8s" repeatCount="indefinite" />
                            </path>
                        </g>
                        <!-- Collapsing particle -->
                        <circle r="8" fill="#C8E0D5" opacity=".0">
                            <animateMotion dur="8s" repeatCount="indefinite"
                                path="M200,80 Q240,150 200,250 Q160,350 200,430" />
                            <animate attributeName="opacity" values="0;.9;0" dur="8s" repeatCount="indefinite" />
                            <animate attributeName="r" values="8;4;8" dur="8s" repeatCount="indefinite" />
                        </circle>
                        <text x="20" y="510" font-family="'Space Grotesk'" font-size="9" fill="#7BAAA0"
                            letter-spacing="3" text-transform="uppercase">Fig 1.1 — Wave Collapse</text>
                    </svg>
                </div>
                <div class="aside-stat" style="margin-top:20px">
                    <div class="aside-num">11M</div>
                    <div class="aside-label">bits of sensory data per second — only 50 reach conscious awareness</div>
                </div>
            </div>
        </div>
    </section>

    <!-- CH 1: THE OVERLAP -->
    <section class="s" style="padding-top:40px">
        <div class="grid-12">
            <div style="grid-column:1/13" class="r">
                <div class="ch">
                    <div class="ch-num">I</div>
                    <div class="ch-block">
                        <div class="ch-eye">The Logic</div>
                        <h2 class="ch-title">The Quantum-Neural <em>Bridge</em></h2>
                    </div>
                </div>
            </div>

            <div class="wide-block">
                <div class="wide-block-text r">
                    <div class="prose" style="max-width:100%">
                        <p>Quantum mechanics established that at the subatomic level, particles exist in a state called
                            <strong>superposition</strong> — simultaneously in multiple states at once. They are waves
                            of probability, not fixed objects. This changes only when an observer interacts with the
                            system. The act of observation forces the wave to "collapse" into a single, definite state.
                            This is the <strong>Observer Effect</strong>.</p>
                        <p>Now pair that with what neuroplasticity tells us: <strong>focused, repeated attention
                                physically rewires the brain.</strong> New synaptic connections form. Old, unused ones
                            dissolve. Your brain is not fixed hardware — it is living architecture that reshapes itself
                            around whatever you consistently pay attention to.</p>
                        <p>The bridge: <em>You are both the quantum observer and the biological instrument at once.</em>
                            Your focused intention collapses probability fields toward a specific outcome, while your
                            neural architecture is simultaneously being rebuilt to perceive and act on those collapsed
                            states.</p>
                        <p>This is the logical engine of manifestation — not wishing, but <strong>sustained, coherent
                                observation that reshapes both the internal (neural) and the external (quantum
                                field).</strong></p>
                    </div>
                    <div class="callout" style="margin-top:28px">
                        <div class="callout-eye">The Core Mechanism</div>
                        <p>Quantum reality responds to the <strong>state of the observer</strong>, not to their desires.
                            Neuroplasticity ensures that the more you embody a state, the more deeply it is encoded as
                            your default. Manifestation is the art of becoming the observer <em>whose state matches the
                                reality they seek</em>, consistently enough for both fields to reorganize around it.</p>
                    </div>
                </div>
                <div class="wide-block-art r d2">
                    <!-- CSS Net Art -->
                    <svg viewBox="0 0 700 540" style="position:absolute;inset:0;width:100%;height:100%"
                        preserveAspectRatio="xMidYMid slice">
                        <rect width="700" height="540" fill="#0B110F" />
                        <!-- Grid lines -->
                        <g stroke="#1C2620" stroke-width="1" fill="none">
                            <line x1="0" y1="90" x2="700" y2="90" />
                            <line x1="0" y1="180" x2="700" y2="180" />
                            <line x1="0" y1="270" x2="700" y2="270" />
                            <line x1="0" y1="360" x2="700" y2="360" />
                            <line x1="0" y1="450" x2="700" y2="450" />
                            <line x1="100" y1="0" x2="100" y2="540" />
                            <line x1="200" y1="0" x2="200" y2="540" />
                            <line x1="300" y1="0" x2="300" y2="540" />
                            <line x1="400" y1="0" x2="400" y2="540" />
                            <line x1="500" y1="0" x2="500" y2="540" />
                            <line x1="600" y1="0" x2="600" y2="540" />
                        </g>
                        <!-- Probability cloud -->
                        <ellipse cx="350" cy="270" rx="220" ry="180" fill="none" stroke="#4A6858" stroke-width="1"
                            opacity=".4" stroke-dasharray="8 5">
                            <animate attributeName="rx" values="220;200;220" dur="6s" repeatCount="indefinite" />
                            <animate attributeName="ry" values="180;200;180" dur="6s" repeatCount="indefinite" />
                        </ellipse>
                        <ellipse cx="350" cy="270" rx="140" ry="110" fill="rgba(74,104,88,.06)" stroke="#7BAAA0"
                            stroke-width=".8" opacity=".5" />
                        <ellipse cx="350" cy="270" rx="60" ry="50" fill="rgba(200,224,213,.04)" stroke="#C8E0D5"
                            stroke-width=".8" opacity=".6" />
                        <!-- Collapse lines -->
                        <g stroke="#B8AECA" stroke-width=".8" opacity=".3">
                            <line x1="100" y1="100" x2="350" y2="270">
                                <animate attributeName="opacity" values=".3;.7;.3" dur="4s" repeatCount="indefinite" />
                            </line>
                            <line x1="600" y1="80" x2="350" y2="270">
                                <animate attributeName="opacity" values=".2;.6;.2" dur="5s" repeatCount="indefinite" />
                            </line>
                            <line x1="150" y1="440" x2="350" y2="270">
                                <animate attributeName="opacity" values=".4;.8;.4" dur="3.5s"
                                    repeatCount="indefinite" />
                            </line>
                            <line x1="580" y1="460" x2="350" y2="270">
                                <animate attributeName="opacity" values=".3;.7;.3" dur="4.5s"
                                    repeatCount="indefinite" />
                            </line>
                        </g>
                        <!-- Center particle collapse -->
                        <circle cx="350" cy="270" r="12" fill="#C8E0D5" opacity=".9">
                            <animate attributeName="r" values="12;6;12" dur="4s" repeatCount="indefinite" />
                            <animate attributeName="opacity" values=".9;1;.9" dur="4s" repeatCount="indefinite" />
                        </circle>
                        <text x="26" y="524" font-family="'Space Grotesk'" font-size="9" fill="#4A6858"
                            letter-spacing="3">Fig 1.2 — Probability Field Collapsing to Observation Point</text>
                    </svg>
                </div>
            </div>
        </div>
    </section>

    <!-- CH 2: HOW TO APPLY -->
    <section class="s">
        <div class="grid-12">
            <div style="grid-column:1/13" class="r">
                <div class="ch">
                    <div class="ch-num">II</div>
                    <div class="ch-block">
                        <div class="ch-eye">The Practice</div>
                        <h2 class="ch-title">How to Apply It — <em>Five Precise Conditions</em></h2>
                    </div>
                </div>
            </div>
            <div class="helpers">
                <div class="helper-card r">
                    <div class="helper-n">01</div>
                    <h3>State Before Action</h3>
                    <p>Do not try to <em>earn</em> the feeling of your desired reality. Embody it first. Quantum
                        observation is a function of current state, not future reward. Neuroplasticity follows: the
                        brain encodes the state you <strong>spend the most time inhabiting</strong>, not the one you
                        reach for. Practice this daily, even 10 minutes of genuinely inhabiting the felt sense of your
                        goal.</p>
                </div>
                <div class="helper-card r d1">
                    <div class="helper-n">02</div>
                    <h3>Specificity Over Volume</h3>
                    <p>A vague, daily affirmation builds a vague, diffuse neural pathway. <strong>Precision is the
                            sharpening agent.</strong> Research on mental rehearsal (Pascual-Leone, 1995) shows vivid,
                        specific visualization activates the same motor cortex as physical action. The quantum field
                        responds to specific frequency — a clear, defined internal state. Define the exact outcome.
                        Rehearse the detail.</p>
                </div>
                <div class="helper-card r d2">
                    <div class="helper-n">03</div>
                    <h3>Emotion as Biochemistry</h3>
                    <p>Dopamine is not a reward signal — it is a <strong>learning consolidation signal.</strong>
                        Elevated emotional states during visualization release dopamine and norepinephrine, which flag
                        the neural circuit as "critical — encode deeply." This is why dry affirmations fail. The feeling
                        is not optional. It is the biochemical mechanism that makes the new pathway permanent.</p>
                </div>
                <div class="helper-card r">
                    <div class="helper-n">04</div>
                    <h3>Repetition Without Lapsing</h3>
                    <p>Neural pathways are formed by consistent firing and weakened by neglect. Quantum coherence — the
                        sustained alignment of your internal frequency — requires the same. <strong>One week of vivid
                            visualization followed by three days of doubt does not equal six days of work.</strong> It
                        resets progress. Consistency is the compound interest of this process.</p>
                </div>
                <div class="helper-card r d1">
                    <div class="helper-n">05</div>
                    <h3>Identity-Level Integration</h3>
                    <p>The brain does not sustain behaviors that conflict with its self-model. If you visualize success
                        but your core identity is "someone who struggles," the limbic system will quietly sabotage
                        aligned action. True integration requires updating the <strong>identity narrative</strong>, not
                        just the goal. Begin describing yourself in the present tense as the version who already lives
                        it.</p>
                </div>
                <div class="helper-card r d2">
                    <div class="helper-n">06</div>
                    <h3>Act from the New State</h3>
                    <p>The quantum-neural process culminates in action — but the quality of action changes. Once neural
                        pathways are genuinely rewired around the desired state, <strong>the actions required to reach
                            the goal stop feeling like discipline and start feeling inevitable.</strong> If action still
                        feels like force, the internal architecture is not there yet. Keep building it.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- STATEMENT BAND -->
    <div class="statement-band r">
        <div class="st-label">The Core Truth</div>
        <p class="st-big">
            <span class="outline">YOU ARE NOT</span><br>
            <span class="fill">ATTRACTING</span><br>
            <span class="outline">YOUR REALITY</span><br>
            <span class="fill">YOU ARE BECOMING</span><br>
            <span class="outline">COHERENT WITH IT</span>
        </p>
        <p class="st-note">The quantum field does not parse language or intent. It responds to the electromagnetic
            coherence of the observer's internal state — which is precisely what neuroplasticity shapes when practiced
            correctly.</p>
    </div>

    <!-- CH 3: BARRIERS -->
    <section class="s">
        <div class="grid-12">
            <div style="grid-column:1/13" class="r">
                <div class="ch">
                    <div class="ch-num">III</div>
                    <div class="ch-block">
                        <div class="ch-eye">The Saboteurs</div>
                        <h2 class="ch-title">Barriers to <em>Delete</em> — The Mechanisms of Self-Interference</h2>
                    </div>
                </div>
            </div>

            <div class="barriers">
                <div class="barrier-card r">
                    <span class="barrier-tag">Neural Barrier</span>
                    <h3>The Dominant Default</h3>
                    <p>Your most-used neural pathways are your fastest. If the dominant circuit is "I am not enough /
                        this won't work," that pathway fires faster and louder than any new, thin affirmation pathway.
                        The barrier is not the new thought — it is the <strong>physical infrastructure of the old
                            one.</strong> You cannot delete it by ignoring it. You counter it by consistent, emotionally
                        charged repetition of the alternative until the new path achieves dominance. Expect resistance
                        for weeks, not hours.</p>
                </div>
                <div class="barrier-card r d1">
                    <span class="barrier-tag">Quantum Barrier</span>
                    <h3>State Incoherence</h3>
                    <p>The quantum observer effect is about the state of the observer, not their intention. If you
                        visualize abundance for 10 minutes but spend 14 hours in low-frequency states (anxiety,
                        resentment, scarcity), the dominant state is the low one. The brain-field coherence is broken.
                        <strong>Your 10-minute ritual cannot override your 14-hour default.</strong> The solution is not
                        more visualization; it is elevating your operating baseline throughout the day.</p>
                </div>
                <div class="barrier-card r">
                    <span class="barrier-tag">Biochemical Barrier</span>
                    <h3>Cortisol Dominance</h3>
                    <p>Chronic stress floods the system with cortisol. Cortisol is neuroplasticity's enemy — it
                        physically shrinks the prefrontal cortex (the seat of deliberate thought and future planning)
                        and enlarges the amygdala (threat response). Under cortisol dominance, <strong>you are literally
                            incapable of the sustained, forward-oriented focus that manifestation requires.</strong>
                        This is not a willpower failure. It is biology. Address stress as a foundational prerequisite —
                        not as a sidebar.</p>
                </div>
                <div class="barrier-card r d1">
                    <span class="barrier-tag">Identity Barrier</span>
                    <h3>The Self-Model Conflict</h3>
                    <p>Your brain maintains a model of who you are and acts as its enforcer. When actions or states
                        arise that contradict the self-model, the limbic system generates discomfort — guilt, fear,
                        impostor syndrome — to push behavior back into the familiar. This is not weakness; it is the
                        immune system of the self-concept. You do not break it by force. You <strong>renegotiate it
                            gradually</strong>, by accumulating experiences that validate the new identity until the old
                        model updates.</p>
                </div>
                <div class="barrier-card r">
                    <span class="barrier-tag">Attention Barrier</span>
                    <h3>The Divided Mind</h3>
                    <p>The Reticular Activating System — the brain's filtering mechanism — is programmed by the objects
                        of sustained attention. A fragmented, low-attention practice (a minute of affirmations while
                        checking your phone) does not convince the RAS to reprioritize. <strong>The depth of attention
                            determines the depth of programming.</strong> Single-pointed focus — even briefly — is more
                        effective than distracted hours. Quality of attention is the variable most underestimated in
                        this process.</p>
                </div>
                <div class="barrier-card r d1">
                    <span class="barrier-tag">Timing Barrier</span>
                    <h3>Expecting Instant Collapse</h3>
                    <p>Quantum probability collapse into material reality operates on a timeline shaped by the density
                        of existing conditions — your habits, relationships, beliefs, and physical circumstances all
                        have inertia. Neural rewiring takes weeks to months of daily practice before behavioral change
                        becomes automatic. <strong>Many people quit inside the gap.</strong> The universe is not slow;
                        the infrastructure being built is simply significant. The gap between internal coherence and
                        external evidence is where most either deepen or abandon the process.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CH 4: WHAT HELPS -->
    <section class="s" style="padding-top:40px">
        <div class="grid-12">
            <div style="grid-column:1/13" class="r">
                <div class="ch">
                    <div class="ch-num">IV</div>
                    <div class="ch-block">
                        <div class="ch-eye">The Accelerants</div>
                        <h2 class="ch-title">What Perfects the Process — <em>Conditions That Compound</em></h2>
                    </div>
                </div>
            </div>

            <div style="grid-column:1/7" class="prose r">
                <p><strong>Sleep.</strong> During deep sleep, the brain undergoes memory consolidation — it takes the
                    day's neural firing patterns and reinforces their synaptic connections. High-quality sleep after
                    visualization dramatically accelerates neural pathway formation. It is not rest; it is
                    <em>production time for the brain's construction crew.</em></p>
                <p><strong>Meditation.</strong> Regular meditation measurably increases cortical thickness, strengthens
                    prefrontal control over the amygdala, and reduces baseline cortisol — directly addressing the three
                    most common barriers. It also trains single-pointed attention, the precise skill required for
                    effective quantum observation. Think of it as calibrating the instrument before use.</p>
                <p><strong>Cold exposure.</strong> Brief cold exposure (cold showers, immersion) triggers a
                    norepinephrine release of 200–300%. Norepinephrine sharpens focus, elevates mood, and alongside
                    dopamine, is one of the two key neurochemicals that lock in new neural pathways. What feels like
                    discomfort is, biochemically, a precision enhancement of your neuroplastic capacity.</p>
            </div>
            <div style="grid-column:7/13" class="prose r d2">
                <p><strong>Movement.</strong> Aerobic exercise increases BDNF (Brain-Derived Neurotrophic Factor) — a
                    molecule neuroscientists call "Miracle-Gro for the brain." BDNF promotes the growth of new neurons
                    and the strengthening of synaptic connections. A walk before or after your visualization practice is
                    not supplementary. It is <em>neural fertilizer.</em></p>
                <p><strong>Gratitude as state management.</strong> Gratitude is not spiritual bypassing. Active
                    gratitude practice shifts prefrontal dominance from right-hemisphere (threat and avoidance) to
                    left-hemisphere (approach and opportunity). It measurably elevates baseline dopamine and serotonin.
                    Done daily, it reconstructs your operating emotional state, which is the quantum observer frequency
                    the field reads.</p>
                <p><strong>Journaling as identity negotiation.</strong> Writing in the present tense about who you are
                    becoming engages the Default Mode Network — the brain's narrative self-model. Consistent journaling
                    from the perspective of the desired identity is one of the most underrated tools for updating the
                    self-concept that otherwise acts as the immune system blocking change.</p>
                <div class="callout" style="margin-top:28px">
                    <div class="callout-eye">The Mentor's Final Word</div>
                    <p>You are not trying to convince the universe of anything. You are trying to <strong>become the
                            version of yourself whose coherent internal state the universe cannot help but
                            reflect.</strong> That version is built in the brain, lived in the body, and sustained
                        across time. Everything else follows.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CLOSING -->
    <section class="s">
        <div class="grid-12">
            <div class="closing r">
                <h2>Manifestation is not performance.<br>It is <em>precision engineering</em> of the self.</h2>
                <p>The quantum field is not listening to what you say. It is reading what you <strong>are</strong> — the
                    electromagnetic signature of your dominant neural state, your operating emotional frequency, your
                    moment-to-moment internal architecture.</p>
                <p>Neuroplasticity gives you the tools to rebuild that architecture deliberately. Quantum mechanics
                    gives you the framework to understand why that rebuilt architecture changes what you encounter in
                    reality. Together, they describe a process that is demanding, unglamorous, and — when done correctly
                    — <strong>uncommonly effective.</strong></p>
            </div>
        </div>
    </section>

    <footer>
        <div>
            <div class="f-logo">COLLAPSE</div>
            <div class="f-info" style="margin-top:16px">
                <p>Vol. II — Quantum &amp; Neural Architecture</p>
                <p>Collapse Into Real, 2026 Editorial</p>
            </div>
        </div>
        <div style="text-align:right">
            <div class="f-info">
                <p>Fonts: Syne · Space Grotesk · Bodoni Moda</p>
                <p>Palette: Forest · Ice · Lavender · Terra</p>
            </div>
        </div>
    </footer>

    <script>
        const rs = document.querySelectorAll('.r');
        const obs = new IntersectionObserver(es => {
            es.forEach(e => { if (e.isIntersecting) { e.target.classList.add('on'); obs.unobserve(e.target) } });
        }, { threshold: .1, rootMargin: '0px 0px -50px 0px' });
        rs.forEach(el => obs.observe(el));
    </script>
</body>

</html>
