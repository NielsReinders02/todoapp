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

<!-- TODO: fill in once the Expo project exists -->

## Commands

<!-- TODO: fill in (start, android, lint, typecheck, test) -->

## Env

- Secrets in `.env` (gitignored). Mirror every key in `.env.example`, no values.
- `EXPO_PUBLIC_*` is bundled into the app and public. No secrets there.
