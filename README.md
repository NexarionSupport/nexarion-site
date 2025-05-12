# Ricreazione corretta dello ZIP contenente index.html

html_content = """<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nexarion – Strategic Investment Advisory</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f7f7f7; color: #222; }
    header { background-color: #0c1a30; color: white; padding: 2rem; text-align: center; }
    section { padding: 2rem; max-width: 900px; margin: auto; }
    h2 { color: #0c1a30; }
    .value-box { background: white; padding: 1rem; margin: 1rem 0; border-left: 4px solid #0c1a30; }
    footer { background-color: #0c1a30; color: white; text-align: center; padding: 1rem; }
    .cta { background-color: #e0e0e0; padding: 2rem; text-align: center; }
    .cta a { background: #0c1a30; color: white; padding: 1rem 2rem; text-decoration: none; border-radius: 4px; }
  </style>
</head>
<body>
  <header>
    <h1>Nexarion</h1>
    <p>Strategic Investment Advisory</p>
  </header>

  <section>
    <h2>Chi siamo</h2>
    <p>Nexarion è una boutique indipendente di advisory strategico, nata per supportare fondi, aziende e investitori nell'accesso e sviluppo di operazioni in Italia. Offriamo supporto discreto, operativo e flessibile, focalizzato su PMI, startup, real estate e investimenti selezionati.</p>
  </section>

  <section>
    <h2>A chi ci rivolgiamo</h2>
    <ul>
      <li>Fondi o advisory internazionali senza struttura locale</li>
      <li>PMI estere con interesse per il mercato italiano</li>
      <li>Famiglie e privati con capitale da investire o acquistare in Italia</li>
      <li>Studi legali, commercialisti e advisor che desiderano integrare un supporto tecnico</li>
    </ul>
  </section>

  <section>
    <h2>I nostri servizi</h2>
    <div class="value-box">
      <h3>Initial</h3>
      <p>Analisi mirata di un'opportunità singola. Report sintetico e call di restituzione.</p>
    </div>
    <div class="value-box">
      <h3>Strategic</h3>
      <p>Due diligence operativa, validazione e affiancamento completo su operazioni selezionate.</p>
    </div>
    <div class="value-box">
      <h3>Custom</h3>
      <p>Soluzioni su misura per investitori e aziende con obiettivi articolati. Possibilità di success fee.</p>
    </div>
  </section>

  <section class="cta">
    <h2>Contattaci</h2>
    <p>Scrivici per valutare insieme possibili sinergie.</p>
    <a href="mailto:info@nexarion.com">info@nexarion.com</a>
  </section>

  <footer>
    <p>&copy; 2025 Nexarion. Tutti i diritti riservati.</p>
  </footer>
</body>
</html>
"""

# Percorso per l'HTML
html_path = "/mnt/data/index.html"

# Scrivi l'HTML su file
with open(html_path, "w") as f:
    f.write(html_content)

# Crea lo ZIP
zip_path = "/mnt/data/nexarion_site.zip"
with zipfile.ZipFile(zip_path, 'w') as zipf:
    zipf.write(html_path, arcname="index.html")

zip_path
