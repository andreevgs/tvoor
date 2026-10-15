# TVOOR

TVOOR is a client-side web application for practicing foreign languages through writing essays. Instead of passive vocabulary drills, the app focuses on active text composition, sentence-level grammar feedback, and tracking writing accuracy over time.

## Capabilities

### Writing and Text Analysis
The editor allows composing texts in the target language with real-time length tracking against minimum volume requirements. For learners who need inspiration, a built-in prompt generator provides essay topics. Writers can explicitly flag whether an external translator was used, keeping progress statistics transparent.

Essays are evaluated sentence by sentence. The review workflow identifies specific sentences containing errors, displays corrected versions with explanations, and assigns an overall grammar score on a 10-point scale. All past submissions remain accessible in an archive with their full sentence breakdowns.

> ⚠️ **How AI Evaluation Works**
>
>TVOOR intentionally does not feature direct API integrations with neural network providers. Instead of automated backend calls requiring paid API keys, the application uses a structured step-by-step prompt dialog: the user copies preformatted review prompts into any web interface (such as Google Gemini, Qwen, or ChatGPT) and pastes the response back into the app.
>
> This architectural choice is the key reason TVOOR is completely free, private, and open-source. It eliminates the need for paid developer accounts, subscriptions, or token budgets, while ensuring user writings are never routed through intermediary servers.

### Progress and Scoring
Progress is measured on a 0 to 100 mastery scale. The scoring model evaluates three factors: the proportion of clean sentences without grammatical mistakes, writing independence from external translation tools, and average grammar quality scores. The progress dashboard displays these metrics alongside historical trend charts and actionable recommendations for areas that need improvement.

### Personal Vocabulary
Words and phrases encountered during writing or text review can be saved into an integrated dictionary. Each record stores the word, its translation, surrounding context, and language pair. The dictionary supports instant search and filtering by language pair.

### Data Storage and Localization
All application data – essays, evaluation history, and dictionary entries – lives strictly inside the browser via IndexedDB. There is no external account or database dependency. Users can export their entire workspace into a `.tvoor` file for backup or cross-device transfer, and restore previous backups at any time.

The application includes light and dark display modes and is fully localized into English, Russian, Belarusian, Polish, German, Spanish, Lithuanian, and Turkish.

## Development

### Prerequisites
Node.js 18 or newer is required.

### Local Setup
Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The application will be accessible at `http://localhost:3000/tvoor/`.

### Production Build
To create a production build:

```bash
npm run build
```

The compiled static assets are generated in the `dist` directory.
