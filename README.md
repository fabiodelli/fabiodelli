## Fabio Delli

**AI Integration Specialist · Versilia**

Costruisco applicazioni web con l'AI integrata dove serve davvero: assistenti che
rispondono al posto del titolare, pipeline che generano contenuti, strumenti che tolgono
lavoro manuale ripetitivo. Lavoro da freelance, soprattutto con hotel e attività locali
in Toscana.

Il principio che mi porto dietro in ogni progetto: **il modello orchestra, il codice
calcola**. I fatti — quantità, prezzi, regole, disponibilità — arrivano da funzioni
deterministiche e da dati verificati, mai da una stima a testo libero del modello.

[fabiodelli.com](https://www.fabiodelli.com) · [LinkedIn](https://linkedin.com/in/fabio-delli)

---

### Progetti

**[softale](https://github.com/fabiodelli/softale)** — Piattaforma di audio storytelling
generato con AI. Prodotto mio, online su [softale.app](https://softale.app) con abbonamenti.
Una storia non è un MP3: è voce, musica e ambiente su tracce separate, ricomposte nel
browser da un motore audio scritto a mano su `HTMLAudioElement`, con crossfade e mixer
per l'ascoltatore. La pipeline di produzione mette in fila Claude per concept e testi,
un server TTS locale e Stable Audio, e assembla con ffmpeg riusando i sottofondi già
generati.
`Next.js 16 · TypeScript · Supabase · Stripe · Zustand · ffmpeg`

**[villa-levante-demo](https://github.com/fabiodelli/villa-levante-demo)** — Assistente AI
multilingua per l'hospitality: risponde agli ospiti 24/7 in italiano, inglese e tedesco e
spinge la prenotazione diretta. Il fallback tra provider è risolto con un probe prima di
aprire lo stream, perché un `try/catch` attorno a `streamText` non intercetta gli errori
del provider: emergono durante il consumo dello stream, non alla chiamata.
Demo navigabile: [villa-levante-demo.vercel.app](https://villa-levante-demo.vercel.app)
`Next.js · Vercel AI SDK · Claude Haiku con fallback GPT-4o-mini · Supabase`

**[project-spark](https://github.com/fabiodelli/project-spark)** — Sistema multi-agente per
l'analisi strategica di Magic: The Gathering. Sei agenti a dominio separato — regole,
grafo delle sinergie, costruzione mazzi, meta-game, simulazione Monte Carlo — sopra una
base di dati Oracle. Zero tolleranza per le allucinazioni sui fatti: testi delle carte e
legalità di formato si leggono e si verificano, non si generano. 125 test.
`Python · FastAPI · NetworkX · React`

**[radar](https://github.com/fabiodelli/radar)** — Gestionale di prospecting locale con un
passaggio umano al centro. La parte interessante non sono le funzionalità ma i due vincoli
che disegnano l'architettura: i termini delle API Google Places, che vietano di persistere
i contenuti, e il GDPR, che impone di tracciare la provenienza di ogni dato. Il database
conserva il `place_id` e ciò che produce l'operatore; il resto si riscarica live.
`Next.js 16 · React 19 · Supabase · Google Places e PageSpeed · Anthropic SDK`

**[faidate-planner](https://github.com/fabiodelli/faidate-planner)** — Descrivi un lavoro
fai-da-te e ottieni un piano a fasi con la lista materiali. Le quantità passano sempre da
`material_specs` a `calc_quantity`: consumi reali per metro quadro e aritmetica in
TypeScript, con la formula mostrata all'utente. Il modello decide cosa chiedere e come
strutturare il piano, non quanta vernice serve.
`Next.js · TypeScript · Claude API con tool use · PostgreSQL`

---

Per lavoro o collaborazioni: [fabiodelli.com](https://www.fabiodelli.com/contact)
