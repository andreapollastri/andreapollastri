<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>GitHub profile cover — Andrea Pollastri</title>
    <meta name="description" content="Banner-style cover for GitHub profile, matching web.ap.it">
    <style>
        @font-face {
            font-family: 'JetBrains Mono';
            src: url('/fonts/jetbrains-mono.woff2') format('woff2');
            font-weight: 300 700;
            font-style: normal;
            font-display: swap;
        }

        :root {
            --green: #4ce66e;
            --hero-bg: #0a0a0a;
            --hero-text: #d4d4d4;
            --hero-soft: #777;
            --hero-faint: #3a3a3a;
        }

        *,
        *::before,
        *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            font-size: 16px;
        }

        body {
            font-family: 'JetBrains Mono', 'SF Mono', Consolas, monospace;
            background: #111;
            color: var(--hero-text);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            -webkit-font-smoothing: antialiased;
        }

        /* GitHub banner: 1200×400 is a common screenshot target */
        .cover {
            width: 100%;
            max-width: 1200px;
            aspect-ratio: 3 / 1;
            min-height: 280px;
            background: var(--hero-bg);
            color: var(--hero-text);
            position: relative;
            overflow: hidden;
            border: 1px solid var(--hero-faint);
            border-radius: 4px;
            box-shadow:
                0 0 0 1px rgba(76, 230, 110, 0.06),
                0 24px 48px rgba(0, 0, 0, 0.45);
        }

        .cover-accent {
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 3px;
            background: linear-gradient(180deg, var(--green) 0%, rgba(76, 230, 110, 0.15) 55%, transparent 100%);
            opacity: 0.65;
            z-index: 2;
            pointer-events: none;
        }

        .cover::after {
            content: '';
            position: absolute;
            inset: 0;
            pointer-events: none;
            background: repeating-linear-gradient(0deg,
                    transparent, transparent 2px,
                    rgba(0, 0, 0, 0.04) 2px, rgba(0, 0, 0, 0.04) 4px);
        }

        .cover::before {
            content: '$ gh profile --user andreapollastri';
            position: absolute;
            right: 1.5rem;
            top: 1.25rem;
            font-size: 0.65rem;
            opacity: 0.14;
            color: var(--green);
            letter-spacing: 0.04em;
            z-index: 2;
        }

        .hero-bg {
            position: absolute;
            right: -1vw;
            bottom: -8%;
            font-size: clamp(10rem, 28vw, 18rem);
            font-weight: 700;
            line-height: 0.8;
            letter-spacing: -0.06em;
            opacity: 0.04;
            pointer-events: none;
            user-select: none;
            color: var(--hero-text);
            white-space: pre;
            z-index: 0;
        }

        .inner {
            position: relative;
            z-index: 1;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: clamp(1.25rem, 4vw, 2.5rem) clamp(1.5rem, 5vw, 3rem);
        }

        .tag {
            font-size: 0.65rem;
            color: var(--green);
            letter-spacing: 0.12em;
            text-transform: uppercase;
            margin-bottom: 0.85rem;
            display: flex;
            align-items: center;
            gap: 0.65rem;
        }

        .tag::before {
            content: '';
            width: 0.85rem;
            height: 1px;
            background: var(--green);
        }

        .name {
            font-size: clamp(1.75rem, 4.2vw, 2.75rem);
            font-weight: 700;
            line-height: 1.05;
            letter-spacing: -0.04em;
            margin-bottom: 0.35rem;
        }

        .sub {
            font-size: clamp(0.75rem, 1.35vw, 0.9rem);
            font-weight: 300;
            opacity: 0.42;
            margin-bottom: 1rem;
        }

        .line {
            font-size: clamp(0.72rem, 1.2vw, 0.88rem);
            font-weight: 300;
            line-height: 1.65;
            opacity: 0.72;
            max-width: 52ch;
        }

        .line strong {
            font-weight: 500;
            color: var(--hero-text);
            opacity: 0.95;
        }

        .line .g {
            color: var(--green);
            font-weight: 400;
        }

        .chips {
            display: flex;
            flex-wrap: wrap;
            gap: 0.45rem;
            margin-top: 1.15rem;
        }

        .chips span {
            font-size: 0.6rem;
            color: var(--hero-soft);
            padding: 0.25rem 0.5rem;
            border: 1px solid var(--hero-faint);
            border-radius: 2px;
            opacity: 0.85;
        }

        .chips span:hover {
            color: var(--green);
            border-color: rgba(76, 230, 110, 0.45);
        }

        .foot {
            position: absolute;
            bottom: 1rem;
            left: clamp(1.5rem, 5vw, 3rem);
            right: clamp(1.5rem, 5vw, 3rem);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.55rem;
            color: var(--hero-soft);
            z-index: 2;
        }

        .foot a {
            color: var(--hero-soft);
            text-decoration: none;
        }

        .foot a:hover {
            color: var(--green);
        }

        .foot-links {
            display: flex;
            gap: 0.85rem;
        }

        @media (max-width: 700px) {
            .cover::before {
                display: none;
            }

            .foot {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.35rem;
            }
        }
    </style>
</head>

<body>

    <article class="cover" aria-label="GitHub profile cover">
        <span class="cover-accent" aria-hidden="true"></span>
        <span class="hero-bg" aria-hidden="true">AP</span>
        <div class="inner">
            <p class="tag">Software developer · Milan · since 2005</p>
            <h1 class="name">Andrea Pollastri</h1>
            <p class="sub">Laravel · Filament · open source · security-minded</p>
            <p class="line">
                I build scalable web apps and ship <strong>Cipi</strong> for painless Laravel deployments.
                <span class="g">~/</span> also: music, live sound, wine &amp; cheese when the compiler is quiet.
            </p>
            <div class="chips" aria-hidden="true">
                <span>PHP</span>
                <span>Laravel</span>
                <span>Filament</span>
                <span>Open source</span>
                <span>DevOps</span>
            </div>
        </div>
        <footer class="foot">
            <span>web.ap.it</span>
            <div class="foot-links">
                <a href="https://github.com/andreapollastri">GitHub</a>
                <a href="https://www.linkedin.com/in/andrea-pollastri">LinkedIn</a>
                <a href="https://web.ap.it">web.ap.it</a>
            </div>
        </footer>
    </article>

</body>

</html>
