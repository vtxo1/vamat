
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Вадим — репетитор по математике</title>
<meta name="description" content="Школьная математика, высшая математика, подготовка к Digital SAT Math, ЕНТ и ЕГЭ. Онлайн-занятия с интерактивной доской и поддержкой в Telegram.">
<link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>∫</text></svg>">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=IBM+Plex+Mono:wght@400;500;600&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>

  /* ============ TOKENS ============ */
  :root{
    --paper: #F7F6F1;
    --paper-deep: #EFEEE6;
    --line: rgba(28,36,48,0.10);
    --line-strong: rgba(28,36,48,0.18);
    --ink: #1C2430;
    --ink-soft: #4A5361;
    --muted: #78808C;
    --pine: #2F6F5E;
    --pine-dark: #1F4E41;
    --pine-tint: #E4EEEA;
    --chalk: #E8B930;
    --chalk-dark: #B9860E;
    --card: #FFFFFF;
    --shadow: 0 1px 2px rgba(28,36,48,0.04), 0 8px 24px rgba(28,36,48,0.06);

    --font-display: 'Instrument Serif', Georgia, serif;
    --font-mono: 'IBM Plex Mono', ui-monospace, Menlo, monospace;
    --font-body: 'IBM Plex Sans', -apple-system, sans-serif;

    --maxw: 1120px;
  }

  *{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin:0;
    background: var(--paper);
    color: var(--ink);
    font-family: var(--font-body);
    font-size: 17px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }
  img,svg{ display:block; max-width:100%; }
  a{ color: inherit; }
  .wrap{ max-width: var(--maxw); margin: 0 auto; padding: 0 28px; }

  h1,h2,h3{ font-family: var(--font-display); font-weight:400; letter-spacing:-0.01em; margin:0; }
  .eyebrow{
    font-family: var(--font-mono);
    font-size: 13px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--pine-dark);
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{ content:""; width:22px; height:1px; background: var(--pine); display:inline-block; }

  .btn{
    font-family: var(--font-mono);
    font-size: 15px;
    font-weight: 500;
    border-radius: 999px;
    padding: 14px 28px;
    border: 1px solid transparent;
    cursor: pointer;
    display: inline-flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
    transition: transform .15s ease, box-shadow .15s ease, background .15s ease;
  }
  .btn:focus-visible{ outline: 2px solid var(--pine); outline-offset: 3px; }
  .btn-primary{ background: var(--ink); color: var(--paper); }
  .btn-primary:hover{ transform: translateY(-1px); box-shadow: var(--shadow); background: var(--pine-dark); }
  .btn-chalk{ background: var(--chalk); color: var(--ink); }
  .btn-chalk:hover{ transform: translateY(-1px); box-shadow: var(--shadow); background: var(--chalk-dark); }
  .btn-ghost{ background: transparent; border-color: var(--line-strong); color: var(--ink); }
  .btn-ghost:hover{ border-color: var(--ink); }

  /* graph-paper texture, used sparingly as the page's signature material */
  .grid-paper{
    background-image:
      linear-gradient(var(--line) 1px, transparent 1px),
      linear-gradient(90deg, var(--line) 1px, transparent 1px);
    background-size: 28px 28px;
  }

  section{ padding: 96px 0; }
  @media (max-width: 720px){ section{ padding: 64px 0; } }

  /* ============ HEADER ============ */
  header{
    position: sticky; top:0; z-index: 50;
    background: rgba(247,246,241,0.86);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }
  .nav{ display:flex; align-items:center; justify-content:space-between; padding: 18px 0; }
  .logo{ font-family: var(--font-mono); font-weight:600; font-size: 16px; display:flex; align-items:center; gap:8px; }
  .logo span.mark{ color: var(--pine); font-size:20px; }
  .nav .btn{ padding: 10px 20px; font-size: 14px; }

  /* ============ HERO ============ */
  .hero{
    padding-top: 72px;
    display:grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 56px;
    align-items:center;
  }
  @media (max-width: 900px){ .hero{ grid-template-columns: 1fr; padding-top: 40px; } }

  .hero h1{ font-size: clamp(2.3rem, 4.4vw, 3.4rem); line-height: 1.12; margin: 18px 0 22px; }
  .hero h1 em{ font-style: italic; color: var(--pine-dark); }
  .hero p.lede{ font-size: 19px; color: var(--ink-soft); max-width: 46ch; margin-bottom: 32px; }

  .bullets{ list-style:none; margin: 0 0 36px; padding:0; display:grid; gap:12px; }
  .bullets li{ display:flex; align-items:flex-start; gap:12px; font-size: 15.5px; }
  .bullets .ico{
    width: 26px; height:26px; flex:none; border-radius:7px;
    background: var(--pine-tint); color: var(--pine-dark);
    display:flex; align-items:center; justify-content:center;
    font-family: var(--font-mono); font-size:13px; font-weight:600;
  }
  .hero-ctas{ display:flex; align-items:center; gap:18px; flex-wrap:wrap; }
  .hero-ctas small{ font-family: var(--font-mono); color: var(--muted); font-size: 13px; }

  .hero-visual{
    position: relative;
    border-radius: 18px;
    border: 1px solid var(--line-strong);
    background: var(--card);
    padding: 20px;
    box-shadow: var(--shadow);
  }
  .hero-visual .grid-paper{ border-radius: 10px; padding: 18px; }
  .hero-visual figcaption{
    font-family: var(--font-mono); font-size:12.5px; color: var(--muted);
    margin-top:12px; display:flex; justify-content:space-between;
  }
  #curve{ stroke-dasharray: 900; stroke-dashoffset: 900; animation: draw 2.4s ease forwards .3s; }
  @keyframes draw{ to{ stroke-dashoffset: 0; } }
  @media (prefers-reduced-motion: reduce){ #curve{ animation: none; stroke-dashoffset:0; } }

  /* ============ METRICS ============ */
  .metrics-grid{
    display:grid; grid-template-columns: repeat(4,1fr); gap: 1px;
    background: var(--line); border: 1px solid var(--line); border-radius: 16px; overflow:hidden;
  }
  @media (max-width: 780px){ .metrics-grid{ grid-template-columns: repeat(2,1fr); } }
  .metric{ background: var(--card); padding: 32px 24px; text-align:center; }
  .metric .num{ font-family: var(--font-mono); font-weight:600; font-size: clamp(1.7rem,3vw,2.4rem); color: var(--pine-dark); }
  .metric .lab{ margin-top:6px; font-size: 14px; color: var(--muted); }

  .profi-row{
    margin-top: 28px; display:flex; align-items:center; gap:18px; flex-wrap:wrap;
    justify-content:center; text-align:center;
  }
  .profi-row .note{ font-size: 14px; color: var(--muted); max-width: 40ch; }

  /* ============ METHODOLOGY ============ */
  .method{ display:grid; grid-template-columns: 0.9fr 1.1fr; gap: 64px; align-items:start; }
  @media (max-width: 900px){ .method{ grid-template-columns: 1fr; gap:36px; } }
  .method h2{ font-size: clamp(1.8rem,3vw,2.4rem); margin: 14px 0 18px; }
  .method p{ color: var(--ink-soft); }
  .principles{ display:grid; gap: 22px; }
  .principle{ display:grid; grid-template-columns: 34px 1fr; gap:16px; }
  .principle .n{ font-family: var(--font-mono); color: var(--pine); font-weight:600; }
  .principle h3{ font-family: var(--font-body); font-weight:600; font-size:16px; margin-bottom:4px; }
  .principle p{ font-size:15px; margin:0; }

  .callout{
    margin-top: 26px; border-left: 3px solid var(--chalk); padding: 4px 0 4px 18px;
    font-size: 16px; color: var(--ink);
  }

  /* ============ CARDS ============ */
  .cards{ display:grid; grid-template-columns: repeat(3,1fr); gap: 24px; }
  @media (max-width: 900px){ .cards{ grid-template-columns: 1fr; } }
  .card{
    background: var(--card); border: 1px solid var(--line); border-radius: 16px;
    padding: 30px; display:flex; flex-direction:column; gap:14px;
    transition: transform .15s ease, box-shadow .15s ease;
  }
  .card:hover{ transform: translateY(-3px); box-shadow: var(--shadow); }
  .card .tag{ font-family: var(--font-mono); font-size:12px; color: var(--pine-dark); text-transform:uppercase; letter-spacing:.06em; }
  .card h3{ font-family: var(--font-display); font-size: 24px; font-weight:400; }
  .card p{ color: var(--ink-soft); font-size: 15px; margin:0; }
  .card .who{ margin-top:auto; padding-top:14px; border-top: 1px dashed var(--line-strong); font-size:13.5px; color: var(--muted); }

  /* ============ INFRASTRUCTURE ============ */
  .infra{ display:grid; grid-template-columns: repeat(3,1fr); gap: 28px; }
  @media (max-width: 900px){ .infra{ grid-template-columns: 1fr; } }
  .infra-item .ico{
    width:44px; height:44px; border-radius:12px; background: var(--pine-tint); color: var(--pine-dark);
    display:flex; align-items:center; justify-content:center; font-size:20px; margin-bottom:16px;
  }
  .infra-item h3{ font-family:var(--font-body); font-weight:600; font-size:17px; margin-bottom:8px; }
  .infra-item p{ color: var(--ink-soft); font-size:15px; margin:0; }

  /* ============ PROCESS ============ */
  .process-wrap{ border-radius: 20px; padding: 56px 40px; }
  @media (max-width:720px){ .process-wrap{ padding: 40px 20px; } }
  .steps{ display:grid; grid-template-columns: repeat(4,1fr); gap: 0; position:relative; }
  @media (max-width: 900px){ .steps{ grid-template-columns: 1fr; } }
  .step{ position:relative; padding: 0 20px; }
  .step:not(:first-child){ border-left: 1px dashed var(--line-strong); }
  @media (max-width: 900px){ .step{ border-left:none !important; padding: 24px 0; border-top: 1px dashed var(--line-strong); }
    .step:first-child{ border-top:none; padding-top:0; } }
  .step .idx{ font-family: var(--font-mono); font-size: 34px; color: var(--pine); font-weight:600; opacity:.5; }
  .step h3{ font-family: var(--font-body); font-weight:600; font-size:16.5px; margin: 8px 0 8px; }
  .step p{ font-size: 14.5px; color: var(--ink-soft); margin:0; }

  /* ============ FORM ============ */
  .cta-section{ background: var(--ink); color: var(--paper); border-radius: 22px; padding: 60px; }
  @media (max-width: 720px){ .cta-section{ padding: 34px 22px; border-radius:16px; } }
  .cta-grid{ display:grid; grid-template-columns: 0.9fr 1.1fr; gap: 48px; }
  @media (max-width: 900px){ .cta-grid{ grid-template-columns: 1fr; } }
  .cta-section h2{ color: var(--paper); font-size: clamp(1.8rem,3vw,2.3rem); margin-bottom:14px; }
  .cta-section p{ color: #C7CDD6; font-size:16px; }
  .cta-section .eyebrow{ color: var(--chalk); }
  .cta-section .eyebrow::before{ background: var(--chalk); }

  form{ display:grid; gap: 16px; }
  .field label{ display:block; font-family: var(--font-mono); font-size: 12.5px; color:#AEB6C2; margin-bottom:6px; letter-spacing:.03em; }
  .field input, .field select{
    width:100%; padding: 13px 14px; border-radius: 10px; border: 1px solid #3A4351;
    background: #232C39; color: var(--paper); font-family: var(--font-body); font-size:15px;
  }
  .field input:focus, .field select:focus{ outline: 2px solid var(--chalk); outline-offset:1px; }
  .row2{ display:grid; grid-template-columns: 1fr 1fr; gap:16px; }
  @media (max-width:560px){ .row2{ grid-template-columns:1fr; } }
  form .btn-chalk{ width:100%; justify-content:center; font-size:16px; padding:15px; margin-top:6px; }
  .trust{ font-size: 13px; color: #8E97A4; margin-top: 10px; }
  #formMsg{ font-size: 14px; margin-top: 10px; display:none; }
  #formMsg.ok{ display:block; color: var(--chalk); }

  footer{ padding: 40px 0 60px; text-align:center; color: var(--muted); font-size: 14px; }
  footer .fname{ font-family: var(--font-mono); color: var(--ink-soft); }

  .section-head{ max-width: 640px; margin-bottom: 44px; }
  .section-head h2{ font-size: clamp(1.8rem,3vw,2.5rem); margin: 14px 0 0; }

</style>
</head>
<body>

<header>
  <div class="wrap nav">
    <div class="logo"><span class="mark">∫</span> Вадим · Математика</div>
    <a href="#record" class="btn btn-primary">Записаться</a>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero wrap">
  <div>
    <div class="eyebrow">репетитор по математике · онлайн</div>
    <h1>Математика — это не про&nbsp;зубрёжку.<br>Это про&nbsp;<em>логику</em>.</h1>
    <p class="lede">Уже с первого занятия вы сможете самостоятельно решить то, что раньше казалось невыполнимым. Я не даю готовые шаблоны — я учу мыслить и задавать себе правильные вопросы.</p>

    <ul class="bullets">
      <li><span class="ico">Ш</span> Школьная математика — алгебра и геометрия, закрытие пробелов с любого уровня</li>
      <li><span class="ico">В</span> Высшая математика — пределы, производные, интегралы, линейная алгебра для студентов</li>
      <li><span class="ico">S</span> Digital SAT Math — системная подготовка по актуальному формату</li>
      <li><span class="ico">KZ</span> ЕНТ — разбор по спецификации, без лишней воды</li>
      <li><span class="ico">RU</span> ЕГЭ — база и профиль, от простого к сложному</li>
    </ul>

    <div class="hero-ctas">
      <a href="#record" class="btn btn-primary">Записаться на диагностику</a>
      <small>бесплатно · 30 минут · без обязательств</small>
    </div>
  </div>

  <figure class="hero-visual">
    <div class="grid-paper" style="aspect-ratio: 4/3.2;">
      <svg viewBox="0 0 320 240" width="100%" height="100%" aria-hidden="true">
        <path id="curve" d="M 12 210 C 70 210, 90 40, 140 40 C 190 40, 190 190, 240 190 C 270 190, 280 90, 308 60"
              fill="none" stroke="#2F6F5E" stroke-width="3" stroke-linecap="round"/>
        <circle cx="140" cy="40" r="4.5" fill="#E8B930"/>
        <circle cx="240" cy="190" r="4.5" fill="#E8B930"/>
      </svg>
    </div>
    <figcaption><span>f(x), разобрано по шагам</span><span>урок №1</span></figcaption>
  </figure>
</section>

<!-- ============ METRICS ============ -->
<section class="wrap">
  <div class="section-head" style="margin-bottom:32px;">
    <div class="eyebrow">в цифрах</div>
    <h2>Цифры, которым можно доверять</h2>
  </div>

  <div class="metrics-grid">
    <div class="metric"><div class="num" data-target="150" data-suffix="+">0</div><div class="lab">учеников подготовлено</div></div>
    <div class="metric"><div class="num" data-target="1200" data-suffix="+">0</div><div class="lab">часов проведённых занятий</div></div>
    <div class="metric"><div class="num" data-target="2.3" data-decimal="1" data-prefix="+">0</div><div class="lab">средний прирост балла ЕНТ / ЕГЭ</div></div>
    <div class="metric"><div class="num" data-target="98" data-suffix="%">0</div><div class="lab">учеников отмечают меньше страха перед предметом</div></div>
  </div>

  <div class="profi-row">
    <!-- Profi.ru widget start -->
    <div class="profi-widget" data-id="621b6c14ec25db4dc380e3d2900f689a" data-type="300x100">
        Powered by <a href="https://profi.kz/profile/TsvirenkoVV">Profi.ru</a>
    </div>
    <script src="https://profi.kz/jqs/widget/widget.js"></script>
    <!-- Profi.ru widget end -->
  </div>
</section>

<!-- ============ METHODOLOGY ============ -->
<section class="wrap">
  <div class="method">
    <div>
      <div class="eyebrow">методика</div>
      <h2>Почему это работает не так, как в школе</h2>
      <p>Большинство репетиторов решают за ученика примеры и просят повторить. Через неделю ученик снова не понимает, что делать, потому что запомнил не принцип, а картинку конкретной задачи.</p>
      <p>Я работаю иначе: на каждом занятии мы разбираем, как устроена математика внутри темы — откуда берётся формула и почему она работает именно так. Когда ученик понимает механизм, он перестаёт бояться незнакомых задач.</p>
      <div class="callout">Страх перед математикой почти никогда не связан с самим предметом — он связан с опытом «я не понимаю и стесняюсь спросить». Убрать этот опыт можно уже на первом уроке.</div>
    </div>

    <div class="principles">
      <div class="principle">
        <div class="n">01</div>
        <div><h3>Понимание раньше запоминания</h3><p>Сначала разбираем, откуда берётся формула, только потом — как её применять.</p></div>
      </div>
      <div class="principle">
        <div class="n">02</div>
        <div><h3>Вопрос важнее ответа</h3><p>Учу задавать себе вопросы «а почему так?», «а что если изменить условие?» — это и есть математическое мышление.</p></div>
      </div>
      <div class="principle">
        <div class="n">03</div>
        <div><h3>Уважение к темпу ученика</h3><p>Кто-то усваивает тему за 20 минут, кто-то — за три занятия. Оба варианта нормальны.</p></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ CARDS ============ -->
<section class="wrap">
  <div class="section-head">
    <div class="eyebrow">направления</div>
    <h2>Что мы будем разбирать</h2>
  </div>

  <div class="cards">
    <div class="card">
      <div class="tag">5–11 класс</div>
      <h3>Школьная программа</h3>
      <p>Закрываем пробелы там, где они реально образовались — иногда это тема из 6 класса, а не из текущей четверти. Работаем над тем, чтобы ученик уверенно выходил к доске и не боялся контрольных.</p>
      <div class="who">Для кого: нужно подтянуть оценки, разобраться «с нуля» или подготовиться к олимпиаде</div>
    </div>
    <div class="card">
      <div class="tag">SAT · ЕНТ · ЕГЭ</div>
      <h3>Подготовка к экзаменам</h3>
      <p>Готовимся системно, по актуальной спецификации конкретного экзамена. Разбираем типовые ловушки, тайм-менеджмент на экзамене и слабые места именно этого ученика по результатам диагностики.</p>
      <div class="who">Для кого: выпускники и абитуриенты с конкретным результатом к конкретной дате</div>
    </div>
    <div class="card">
      <div class="tag">1–2 курс</div>
      <h3>Высшая математика</h3>
      <p>Пределы, производные, интегралы, линейная алгебра — объясняю как логически связанную систему, а не набор формул из методички. Помогаю закрыть хвост или подготовиться к экзамену.</p>
      <div class="who">Для кого: студенты технических и экономических специальностей</div>
    </div>
  </div>
</section>

<!-- ============ INFRASTRUCTURE ============ -->
<section class="wrap">
  <div class="section-head">
    <div class="eyebrow">формат занятий</div>
    <h2>Ничего не отвлекает от математики</h2>
  </div>

  <div class="infra">
    <div class="infra-item">
      <div class="ico">⌗</div>
      <h3>Интерактивная доска</h3>
      <p>Пишем формулы, чертим графики и геометрические построения в реальном времени — как будто сидим рядом за одним столом.</p>
    </div>
    <div class="infra-item">
      <div class="ico">▤</div>
      <h3>Конспект после урока</h3>
      <p>Не нужно судорожно переписывать всё за 45 минут — после занятия вы получаете аккуратный конспект с решёнными примерами.</p>
    </div>
    <div class="infra-item">
      <div class="ico">✎</div>
      <h3>Telegram 24/7</h3>
      <p>Если задача не решается в 11 вечера накануне контрольной — можно написать и получить объяснение, не дожидаясь следующего занятия.</p>
    </div>
  </div>
</section>

<!-- ============ PROCESS ============ -->
<section class="wrap">
  <div class="process-wrap grid-paper" style="border:1px solid var(--line-strong); background-color: var(--paper-deep);">
    <div class="section-head" style="margin-bottom:36px;">
      <div class="eyebrow">как проходит работа</div>
      <h2>От первого сообщения до результата</h2>
    </div>
    <div class="steps">
      <div class="step">
        <div class="idx">01</div>
        <h3>Диагностика</h3>
        <p>Бесплатное занятие на 30 минут: смотрим уровень, выявляем реальные пробелы и обсуждаем цель.</p>
      </div>
      <div class="step">
        <div class="idx">02</div>
        <h3>Индивидуальная карта</h3>
        <p>Составляю план: какие темы разбираем в первую очередь, в каком порядке и с каким темпом.</p>
      </div>
      <div class="step">
        <div class="idx">03</div>
        <h3>Занятия</h3>
        <p>Регулярные онлайн-уроки по плану, с конспектами после каждого и поддержкой между занятиями.</p>
      </div>
      <div class="step">
        <div class="idx">04</div>
        <h3>Результат</h3>
        <p>Отслеживаем прогресс по пробникам и контрольным, корректируем план при необходимости.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ FORM ============ -->
<section class="wrap" id="record">
  <div class="cta-section">
    <div class="cta-grid">
      <div>
        <div class="eyebrow">начать</div>
        <h2>Начнём с бесплатной диагностики</h2>
        <p>30 минут, чтобы понять, с чем именно предстоит работать — без давления и без «продажи» курса.</p>
      </div>

      <form id="signupForm">
        <div class="field">
          <label for="f-name">Имя</label>
          <input id="f-name" name="name" type="text" required placeholder="Как к вам обращаться">
        </div>
        <div class="row2">
          <div class="field">
            <label for="f-contact">Telegram или телефон</label>
            <input id="f-contact" name="contact" type="text" required placeholder="@username или +7...">
          </div>
          <div class="field">
            <label for="f-grade">Класс / курс</label>
            <input id="f-grade" name="grade" type="text" placeholder="например, 9 класс">
          </div>
        </div>
        <div class="field">
          <label for="f-track">Направление</label>
          <select id="f-track" name="track">
            <option>Школьная программа</option>
            <option>Digital SAT Math</option>
            <option>ЕНТ</option>
            <option>ЕГЭ</option>
            <option>Высшая математика</option>
          </select>
        </div>
        <div class="field">
          <label for="f-time">Удобное время (необязательно)</label>
          <input id="f-time" name="time" type="text" placeholder="например, будни после 18:00">
        </div>
        <button type="submit" class="btn btn-chalk">Записаться на диагностику →</button>
        <div class="trust">Отвечаю на заявки в течение дня. Никакого спама — только подтверждение записи.</div>
        <div id="formMsg"></div>
      </form>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <span class="fname">Вадим</span> — репетитор по математике. Онлайн, для школьников и студентов.
  </div>
</footer>

<script>
  // ===== 1) Замените на свой юзернейм Telegram, чтобы заявки прилетали вам в чат =====
  const TELEGRAM_USERNAME = "@metronok"; // например "vadim_math"

  // ===== Счётчики: анимация чисел при появлении в зоне видимости =====
  const nums = document.querySelectorAll('.metric .num');
  const animateNum = (el) => {
    const target = parseFloat(el.dataset.target);
    const decimal = parseInt(el.dataset.decimal || "0", 10);
    const suffix = el.dataset.suffix || "";
    const prefix = el.dataset.prefix || "";
    const duration = 1200;
    const start = performance.now();
    const step = (now) => {
      const p = Math.min((now - start) / duration, 1);
      const eased = 1 - Math.pow(1 - p, 3);
      const val = target * eased;
      el.textContent = prefix + val.toFixed(decimal) + suffix;
      if (p < 1) requestAnimationFrame(step);
    };
    requestAnimationFrame(step);
  };
  const io = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        animateNum(entry.target);
        io.unobserve(entry.target);
      }
    });
  }, { threshold: 0.5 });
  nums.forEach(n => io.observe(n));

  // ===== Форма: собираем данные и открываем Telegram с готовым сообщением =====
  const form = document.getElementById('signupForm');
  const msg = document.getElementById('formMsg');
  form.addEventListener('submit', (e) => {
    e.preventDefault();
    const data = new FormData(form);
    const text =
`Заявка на диагностику:
Имя: ${data.get('name')}
Контакт: ${data.get('contact')}
Класс/курс: ${data.get('grade') || '—'}
Направление: ${data.get('track')}
Удобное время: ${data.get('time') || '—'}`;

    if (TELEGRAM_USERNAME && TELEGRAM_USERNAME !== "@metronok") {
      const url = `https://t.me/${TELEGRAM_USERNAME}?text=${encodeURIComponent(text)}`;
      window.open(url, '_blank');
      msg.textContent = "Открываю Telegram — останется нажать «Отправить».";
    } else {
      msg.textContent = "Заявка сформирована. Укажите свой Telegram-username в коде страницы (переменная TELEGRAM_USERNAME), чтобы заявки открывались в чате автоматически.";
    }
    msg.classList.add('ok');
    form.reset();
  });
</script>

</body>
</html>
