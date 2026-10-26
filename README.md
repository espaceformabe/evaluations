# Espace Forma — évaluations

App Next.js autonome pour les quiz informatiques et les évaluations de formation d’Espace Forma (EF) asbl.

## Lancer en local

```bash
pnpm install
pnpm dev
```

Ouvre [http://localhost:3002](http://localhost:3002).

## Envoi des PDF

Copiez `.env.example` vers `.env` et renseignez :

- `RESEND_API_KEY`
- `EVALUATIONS_FROM_EMAIL` (domaine vérifié chez Resend, pas une adresse Outlook)
- `EVALUATIONS_TO_EMAIL` (défaut : `ecdasbl@outlook.be`)

## Production

```bash
pnpm build
pnpm start
```

En production l’app est sur [https://evaluations.espaceforma.be](https://evaluations.espaceforma.be). Le site vitrine redirige `/quiz1a`, `/quiz1b`, `/quiz1c`, `/quiz2`, `/evaluation-ts` et `/evaluations` vers cette origine (`EVALUATIONS_ORIGIN`, défaut `https://evaluations.espaceforma.be`).

Pages :

- `/` — choix entre quizz informatiques et évaluation de formation
- `/quizz-informatiques` — quiz 1A, 1B, 1C et 2
- `/evaluation-de-formation` — évaluations de module
- `/quiz1a` → `/quiz-1a`
- `/quiz1b` → `/quiz-1b`
- `/quiz1c` → `/quiz-1c`
- `/quiz2` → `/quiz-2`
- `/evaluation-ts` → `/titres-services`
- `/evaluations` → `/`
