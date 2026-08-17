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

**[catalog-normalizer](https://github.com/fabiodelli/catalog-normalizer)** — Prende righe
prodotto scritte da esseri umani in fonti diverse e produce un catalogo strutturato, più un
registro di tutto ciò che ha rifiutato con il motivo. Le regole deterministiche risolvono
quanto possono; solo il residuo ambiguo passa a un modello, e ogni valore proposto ripassa
dalle stesse regole prima di entrare — un colore fuori tavolozza o un EAN con checksum
errato viene rifiutato chiunque lo abbia scritto. I numeri realmente ambigui (`1,234`)
vengono respinti invece che indovinati. Primo progetto in Rust, dichiarato come tale.
`Rust · 60 test offline · output strutturati e contabilizzazione dei token`

**[faidate-planner](https://github.com/fabiodelli/faidate-planner)** — Descrivi un lavoro
fai-da-te e ottieni un piano a fasi con la lista materiali. Le quantità passano sempre da
`material_specs` a `calc_quantity`: consumi reali per metro quadro e aritmetica in
TypeScript, con la formula mostrata all'utente. Il modello decide cosa chiedere e come
strutturare il piano, non quanta vernice serve.
`Next.js · TypeScript · Claude API con tool use · PostgreSQL`

---

### Lavoro di squadra

**[BoolBnB](https://github.com/fabiodelli/boolbnb)** — Piattaforma di annunci per affitti
brevi: ricerca per zona e servizi, messaggi dagli ospiti, sponsorizzazioni degli annunci e
statistiche di visualizzazione. Costruita in cinque persone durante il bootcamp nel 2023,
Vue 3 sul front e Laravel per area privata e API
([boolbnb-backend](https://github.com/fabiodelli/boolbnb-backend)).
Fork dei repository del team, originali di
[@luca-macedone](https://github.com/luca-macedone).

Il mio contributo, in 79 commit: lato Laravel la feature delle visualizzazioni
end-to-end — model, relazione con `Apartment`, policy, CRUD del controller,
autorizzazione sui metodi di lettura — e le statistiche della dashboard (visite totali,
appartamento più visto), con la rotta API poi consumata dal front. Lato Vue i metodi di
chiamata API nello state, la ricerca semplice e quella avanzata, le card dei risultati e
parte del layout.

---

Per lavoro o collaborazioni: [fabiodelli.com](https://www.fabiodelli.com/contact)
