#2 - Create Empire Builder project slide deck
What & Why
The user confirmed they want a slide deck about their existing Empire Builder strategy game. Create a concise project overview grounded in the actual game, not a speculative investor pitch.

Done looks like
A separate slides artifact opens and every slide renders with readable content.
Approximately 8 slides explain the concept, player journey, economy, construction, army, battles, progression and leaderboard, and implementation summary.
The deck uses the existing game’s dark medieval identity, exact theme colors, Cinzel headings, Inter body font, and existing relevant assets.
Distinguishes implemented behavior from intended ambition: XP is awarded but automatic leveling is not verified; battles loot resources, not proven territorial ownership. No invented traction or metrics.
Out of scope
Changing the game or backend, fixing existing bugs, adding gameplay, invented market claims.
Steps
Read the artifacts skill and relevant slide-authoring instructions available after migration.
Create the presentation using createArtifact({ artifactType: "slides", slug: "empire-builder-deck", previewPath: "/", title: "Empire Builder — Project Overview", description: "A project overview of the medieval empire-building strategy game and its core systems." }).
Inventory the migrated game’s theme, fonts, images, and UI. Reuse exact brand tokens and appropriate existing images; do not redesign the brand. Original theme uses Cinzel and Inter, primary HSL 43 74% 49%, background HSL 222 47% 6%.
Read game pages and storage logic to verify claims. Original sources: client/src/pages/{Landing,Empire,Barracks,Map,Leaderboard}.tsx, client/src/index.css, server/storage.ts, shared/schema.ts. Locate equivalent migrated paths.
Build approximately 8 slides: title and vision; collect/build/train/attack/reinvest loop; resources and population; grid-based construction and five building types; swordsmen/archers/cavalry; target selection and battle reports/loot; XP and leaderboard with honest current limitations; React/TypeScript/Express/PostgreSQL and authenticated saved empires. Keep copy concise and use clear diagrams without invented numbers.
Verify all slides and navigation, responsive presentation rendering, and screenshots via running workflows. Ensure the game is unaffected.
Call presentArtifact({ artifactId }) with the new stable artifact ID.
Call markTaskComplete({ task_ref: "", ... }) as the final callback in CodeExecution.
Relevant files
Migrated game frontend pages and theme, API storage and schema.
Original client/src/index.css, client/src/pages/Landing.tsx, server/storage.ts, shared/schema.ts.
Note to the code reviewer
Do NOT reject for missing workspace hooks when endpoints are not needed, subjective component reuse, or presentation-native navigation differing from the game. Do NOT flag unused scaffold files or root-level pnpm dev failing; verify via workflows. DO flag broken slides, brand colors/fonts/images not matching the game, invented capabilities or metrics, and regressions to the existing game.

The project has already been migrated to PNPM_WORKSPACE. Do not run the migration again.
