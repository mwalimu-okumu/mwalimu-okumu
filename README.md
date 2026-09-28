
<!DOCTYPE html>
<html lang="sw">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mwalimu Okumu | Hadithi za Kiswahili</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #faf7f1;
      color: #30251d;
    }
    header {
      background: #49311f;
      color: white;
      padding: 22px 16px;
      text-align: center;
    }
    header h1 { margin: 0 0 8px; }
    nav {
      background: #6b4930;
      padding: 12px;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 10px;
      text-decoration: none;
    }
    main {
      max-width: 850px;
      margin: auto;
      padding: 20px;
    }
    .hero {
      background: #eadbc6;
      padding: 25px;
      border-radius: 14px;
      margin-bottom: 25px;
    }
    .hero h2 { margin-top: 0; }
    input {
      width: 100%;
      padding: 13px;
      border: 1px solid #c8b8a5;
      border-radius: 8px;
      font-size: 16px;
      margin: 10px 0 20px;
    }
    .story {
      background: white;
      padding: 18px;
      border-radius: 12px;
      margin-bottom: 15px;
      border: 1px solid #e6ded4;
    }
    .story h3 { margin-top: 0; }
    .story button {
      background: #49311f;
      color: white;
      border: 0;
      padding: 10px 15px;
      border-radius: 6px;
      cursor: pointer;
    }
    .content {
      display: none;
      line-height: 1.8;
      white-space: pre-line;
      margin-top: 15px;
    }
    footer {
      text-align: center;
      padding: 25px;
      background: #49311f;
      color: white;
    }
  </style>
</head>
<body>

<header>
  <h1>MWALIMU OKUMU</h1>
  <p>Hadithi zinazogusa maisha.</p>
</header>

<nav>
  <a href="#mwanzo">Mwanzo</a>
  <a href="#hadithi">Hadithi</a>
  <a href="#kuhusu">Kuhusu</a>
</nav>

<main>
  <section class="hero" id="mwanzo">
    <h2>Karibu katika ulimwengu wa hadithi</h2>
    <p>
      Soma hadithi za Kiswahili kuhusu mapenzi,
      maisha, familia, elimu na siri mbalimbali.
    </p>
  </section>

  <section id="hadithi">
    <h2>Maktaba ya Hadithi</h2>
    <p>Chagua hadithi unayotaka kusoma.</p>

    <input id="search"
      type="search"
      placeholder="Tafuta hadithi..."
      oninput="tafutaHadithi()">

    <article class="story">
      <h3>1. Safari ya Maisha</h3>
      <p><b>Aina:</b> Maisha</p>
      <p>
        Kila safari huanza kwa hatua moja.
        Hii ni hadithi kuhusu kijana mwenye ndoto.
      </p>
      <button onclick="soma(this)">Soma hadithi</button>
      <div class="content">
        Lameck alikuwa kijana mwenye ndoto kubwa.
        Kila siku aliamka mapema na kujiandaa
        kwa safari yake ya kutafuta elimu.

        Ingawa maisha hayakuwa rahisi,
        aliamini kuwa bidii na subira
        vingemsaidia kufikia malengo yake.

        Siku moja alipokea habari iliyobadilisha
        maisha yake kabisa.

        Hadithi hii itaendelea...
      </div>
    </article>

    <article class="story">
      <h3>2. Siri ya Barua</h3>
      <p><b>Aina:</b> Siri</p>
      <p>
        Barua ya zamani ilifichua ukweli
        ambao familia ilikuwa imeuficha.
      </p>
      <button onclick="soma(this)">Soma hadithi</button>
      <div class="content">
        Amina alipokuwa akisafisha nyumba ya
        bibi yake, alipata bahasha ya zamani.

        Ndani yake kulikuwa na barua yenye jina
        lake na tarehe ya miaka mingi iliyopita.

        Alipoanza kuisoma, aligundua kuwa
        kulikuwa na siri kubwa kuhusu familia yao.

        Je, angeweza kugundua ukweli wote?
      </div>
    </article>

    <article class="story">
      <h3>3. Upendo wa Kweli</h3>
      <p><b>Aina:</b> Mapenzi</p>
      <p>
        Hadithi ya watu wawili waliokutana
        wakati ambao hawakutarajia.
      </p>
      <button onclick="soma(this)">Soma hadithi</button>
      <div class="content">
        Neema na Daniel walikutana chuoni
        siku moja ya mvua.

        Mazungumzo yao mafupi yakawa mwanzo
        wa urafiki ambao ulijaa furaha,
        changamoto na maamuzi magumu.

        Lakini je, upendo wao ungeweza
        kushinda vikwazo vilivyowakabili?
      </div>
    </article>
  </section>

  <section id="kuhusu">
    <h2>Kuhusu Mwalimu Okumu</h2>
    <p>
      Mwalimu Okumu ni jukwaa la hadithi
      za Kiswahili linalolenga kuendeleza
      usomaji, ubunifu na vipaji vya uandishi.
    </p>
  </section>
</main>

<footer>
  <p>© 2026 Mwalimu Okumu</p>
  <p>Andika. Simulia. Gusa mioyo.</p>
</footer>

<script>
  function soma(button) {
    const content = button.nextElementSibling;
    const opened = content.style.display === "block";
    content.style.display = opened ? "none" : "block";
    button.textContent = opened ? "Soma hadithi" : "Funga hadithi";
  }

  function tafutaHadithi() {
    const query = document.getElementById("search")
      .value.toLowerCase();

    document.querySelectorAll(".story").forEach(story => {
      story.style.display =
        story.innerText.toLowerCase().includes(query)
          ? "block" : "none";
    });
  }
</script>

</body>
</html>
