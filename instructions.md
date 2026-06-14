# Clever Cubes: Online Puzzle Games Platform (Deliverable Specification and Verification Guide)

## 1. Project Overview

### 1.1 The project
Clever Cubes is an online platform offering free, interactive puzzle games. We require a responsive, full-stack Minimum Viable Product (MVP) featuring three core puzzles: Sudoku, Word Search, and a Sliding Tile puzzle. It must handle dynamic puzzle generation, user authentication, and secure score tracking, loading in under two seconds on all devices. 

### 1.2 The deliverable
The package contains eight specific files inside one zipped folder: front and backend source code, database schema, admin and deployment guides, API documentation, a QA report, and UI assets.

### 1.3 What good looks like
A successful delivery means seamless mobile gameplay with zero horizontal scrolling. Users can instantly generate a puzzle, securely save their score, and view leaderboards. The client’s team can deploy the platform smoothly using only your provided Markdown guide.

### 1.4 Business context
This MVP proves user retention through fast, frictionless gameplay. Bug-free puzzle logic, a native mobile feel, and secure data handling are mandatory. 

### 1.5 Why the scope is shaped this way
This is a custom build, not a template. We require separated frontend/backend architectures, strictly validated custom game logic, and complete handover documentation so the client owns the deployment.

### 1.6 What this job is not
This is not a native iOS/Android app, a 3D game, or an ongoing maintenance contract. It is a one-time fixed-scope MVP build.

### 1.7 Brand note
Clever Cubes is a modern, minimalist puzzle brand. The UI should reflect focus and mental sharpness.

---

## 2. Deliverables at a Glance

### 2.1 The eight files

| # | Deliverable | Format | Exact file name |
|---|---|---|---|
| 1 | Frontend source archive | ZIP | `CleverCubes_Frontend_v1.zip` |
| 2 | Backend source archive | ZIP | `CleverCubes_Backend_v1.zip` |
| 3 | Database schema | PDF | `CleverCubes_DatabaseSchema_v1.pdf` |
| 4 | Admin documentation | PDF | `CleverCubes_AdminGuide_v1.pdf` |
| 5 | Deployment guide | Markdown | `CleverCubes_DeploymentGuide_v1.md` |
| 6 | API documentation | JSON | `CleverCubes_APIDocs_v1.json` |
| 7 | QA and test report | PDF | `CleverCubes_TestReport_v1.pdf` |
| 8 | UI assets archive | ZIP | `CleverCubes_UIAssets_v1.zip` |

### 2.2 How to check the delivery
Ensure exactly eight files exist with the names above. Verify code zips lack compiled `/node_modules`. Run the deployment guide locally, test the API via Postman, and verify cross-device playability per the QA report.

---

## 3. Brand and Look

### 3.1 Brand palette
| Use | Color Name | Hex |
|---|---|---|
| Primary Brand & Headers | Logic Blue | `#2B547E` |
| Accents & Active States | Sharp Mint | `#42B883` |
| Typography & Borders | Slate Dark | `#2C3E50` |
| Backgrounds & Play Areas | Focus White | `#F8F9FA` |

### 3.2 Type & Logo
Use a legible sans-serif web font with tabular (monospaced) numbers for puzzle grids. The logo is a simple "Clever Cubes" text in bold Logic Blue.

### 3.3 UI basics
* **Mobile-First:** Grids scale to viewport width. No horizontal scrolling.
* **Touch Targets:** Interactive cells must be at least 44x44 pixels.
* **Clear States:** Highlight selected puzzle cells cleanly.

---

## 4. The Product and the Logic

### 4.1 The puzzles
| ID | Puzzle Type | Requirements |
|---|---|---|
| P01 | Sudoku | 9x9 grid. Easy/Med/Hard. Exactly one unique solution per board. |
| P02 | Word Search | Dynamic generation from db themes. Horizontal, vertical, diagonal words. |
| P03 | Sliding Tile | 4x4 or 3x3. Must mathematically guarantee solvability (inversions check). |

### 4.2 The five beats (views)
1.  **Homepage:** Categories, challenges, and registration CTA.
2.  **Auth:** Sign up, log in, password reset.
3.  **Game Interface:** Grid, timer, and controls (Pause/Restart).
4.  **Completion:** Score, time, and leaderboard pop-up.
5.  **Dashboard:** User history and best times.

### 4.3 Core mechanics
* **Timer:** Counts up, pauses accurately, stops on win-state.
* **Validation:** Grids only accept valid inputs (e.g., 1-9 for Sudoku).
* **Security:** Backend validates completion times to prevent impossible scores.

---

## 5. Deliverable Specifications

### 5.1 & 5.2 Source Archives (Front & Back)
* **Frontend (`.zip`):** React/Vue + Tailwind/CSS. Responsive grids. No `/node_modules` or `.env` secrets.
* **Backend (`.zip`):** Node/Python REST API. Bcrypt auth, JWT sessions. No `/node_modules` or `.env` secrets.

### 5.3 Database schema (PDF)
Includes an Entity Relationship Diagram (ERD) and a Data Dictionary detailing tables, types, and constraints.

### 5.4 Admin documentation (PDF)
Instructions and screenshots on how to manage users, ban accounts, and update Word Search lists.

### 5.5 Deployment guide (MD)
Step-by-step terminal commands to install dependencies, run migrations, and launch on a standard service (AWS/Vercel).

### 5.6 API documentation (JSON)
A Postman Collection detailing all endpoints, request bodies, and responses.

### 5.7 QA and test report (PDF)
Checklist proving Sudoku generation works, sliding puzzles are solvable, and cross-browser/mobile tests passed.

### 5.8 UI assets archive (ZIP)
Raw icons, fonts, or logos used.

---

## 6. Code Quality Checks
1.  **Valid Generation:** Sudoku always has one solution; Sliding tiles are always solvable.
2.  **Responsive:** Fits 320px mobile screens without side-scrolling.
3.  **Secure:** SQLi/XSS prevention and server-side score validation (no 0-second wins).
4.  **Clean Code:** Semantic HTML, zero fatal browser console errors, and instant puzzle generation.

---

## 7. Security and Responsiveness
* **Data:** Passwords hashed via bcrypt/Argon2. Sensitive fields stripped from API responses.
* **Mobile:** Prevent double-tap zoom via standard viewport meta tags.
* **Network:** Mandate HTTPS for production.

---

## 8. File Names

### 8.1 The pattern
`CleverCubes_[Deliverable]_v[N].[ext]`. No spaces, no extra tags. 

### 8.2 The exact names
1. `CleverCubes_Frontend_v1.zip`
2. `CleverCubes_Backend_v1.zip`
3. `CleverCubes_DatabaseSchema_v1.pdf`
4. `CleverCubes_AdminGuide_v1.pdf`
5. `CleverCubes_DeploymentGuide_v1.md`
6. `CleverCubes_APIDocs_v1.json`
7. `CleverCubes_TestReport_v1.pdf`
8. `CleverCubes_UIAssets_v1.zip`

### 8.3 New versions
If revising, bump the version on *all* files to `_v2` and resend the complete set.

---

## 9. Folder Layout
Place all eight files in a folder named exactly `CleverCubes_Delivery`. Zip this folder for handoff.

---

## 10. Not Part of This Job
* Live server hosting/domains.
* Native mobile app files (`.ipa`/`.apk`).
* Payment gateways.
* Puzzles beyond the core three.

---

## 11. Acceptance Criteria

### 11.1 What must be true to accept
1. Folder named `CleverCubes_Delivery` containing exactly 8 correctly named files.
2. Apps launch successfully using the deployment guide.
3. All puzzles play, validate correctly, and scale to mobile viewports.
4. User auth and leaderboard score saving function securely.
5. All provided documentation (API, Schema, QA) matches the code accurately.

### 11.2 Final check
Run the startup commands locally. Play one of each game on a mobile view, verify scores save to the database, and check the browser console for errors. Ensure file names match perfectly.

---

## 12. Suggested Workflow
1.  **Schema & Docs:** Map database and API; get sign-off.
2.  **Logic:** Build and isolate puzzle generation algorithms (Sudoku solvers, parity checks).
3.  **Backend:** Build API, Auth, and score validation.
4.  **Frontend:** Connect UI, timers, and grids.
5.  **Package:** Test, write guides, format folder, and deliver.
