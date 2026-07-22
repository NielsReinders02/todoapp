# todoapp

Todo app. React Native + Expo. Android first, web and iOS later.
Learning and portfolio project — optimize for understanding, not speed.

## Rules

- Explain before implementing.
- One feature or screen per round. Small diffs.
- No new dependencies without asking.
- No clever code, no abstraction up front.
- Explain root cause before fixing a bug.
- Ask instead of assuming.
- Never commit or push unless asked.

## Conventions

- Code, comments, commits, PRs, conversation: English.
- User want's to improve his english capabilities - address weak language and give small improvements at beginning of sentences
- TypeScript `strict`. No `any` without a reason in a comment.
- Conventional Commits (`feat:`, `fix:`, `refactor:`, `test:`, `chore:`).
- One feature = one branch = one PR.
- Comments explain *why*, not *what*.

## Stack

| Concern | Choice |
| --- | --- |
| Framework | Expo + expo-router |
| Language | TypeScript |
| State | `useState` / Context (no Redux/Zustand yet) |
| Storage | AsyncStorage |
| Styling | `StyleSheet` (no NativeWind yet) |
| Tests | Jest + React Native Testing Library |

## Structure

- `src/app/` — screens. File-based routing (expo-router): each file is a route.
  - `_layout.tsx` — root layout, wraps every screen (`<Stack>`).
  - `index.tsx` — the `/` route (home).
- `assets/images/` — app icon, splash, Android adaptive icon, web favicon.
  Referenced from `app.json`; not imported in code.
- `app.json` — app identity: name, icon, Android package, plugins, EAS project id.
- `eas.json` — cloud build profiles (`development`, `preview`, `production`).
- `tsconfig.json` — `strict` on; `@/*` maps to `src/*`.

Path alias: import with `@/...` (e.g. `@/components/todo-item`), not relative `../..`.

## Commands

| Command | Does |
| --- | --- |
| `npx expo start` | Start Metro dev server; open the app via the dev build. |
| `npx expo start --web` | Run in the browser (fast, no device needed). |
| `npm run android` | Start with the Android target selected. |
| `npm run lint` | Run Expo's ESLint. |
| `npx tsc --noEmit` | Type-check without emitting files. |
| `npx expo install <pkg>` | Add a dependency at the SDK-correct version. |
| `eas build --profile development --platform android` | Rebuild the dev client (needed only when native code changes). |

No `test` script yet — added when Jest is set up.

## Env

- Secrets in `.env` (gitignored). Mirror every key in `.env.example`, no values.
- `EXPO_PUBLIC_*` is bundled into the app and public. No secrets there.
