# FilmlaborOS — AI Business Operating System

> Ein komplettes AI-gesteuertes Business OS auf Basis von **Obsidian + Claude Code**.
> 95+ Skills, automatisierte Pipelines, und eine strukturierte Wissensbasis nach der Jake Van Clief Methodik.

---

## System-Architektur

```
FilmlaborOS/
 |
 |-- CLAUDE.md                  # Routing Table — das Gehirn des Systems
 |-- CONTEXT.md                 # Was dieses Vault ist
 |-- ENVIRONMENT.md             # Technische Umgebung (Python, Ports, Tools)
 |
 |-- context/                   # WISSEN (read-only Wahrheit)
 |   |-- business/              #   Firmendaten, API-Config, Strategien
 |   |   |-- telos/             #     Mission, Vision, Werte
 |   |   +-- onboarding/        #     Team-Onboarding Guides
 |   |-- learning/              #   Lernmaterial, Kurse, Transkripte
 |   +-- calls/                 #   Call Notes, Meeting Protokolle
 |
 |-- code/                      # SYSTEM (Skills + externe Tools)
 |   |-- skills/                #   95+ Business Skills (SKILL.md je Ordner)
 |   +-- external/              #   Referenz-Repos (playwright-cli, GSD, etc.)
 |
 |-- workspace/                 # AKTIVE ARBEIT (veraenderbar)
 |   |-- clients/               #   Ein Ordner pro Client
 |   |-- content/               #   LinkedIn Posts, Social Media
 |   |-- foundations/            #   Tagesplanung, Outreach
 |   |-- projects/              #   Laufende Projekte
 |   |-- research/              #   Marktanalysen, Deep Research
 |   +-- schule/                #   Schulmaterial (Biologie, Chemie)
 |
 |-- scripts/                   # CODE & AUTOMATIONEN
 |   |-- api/                   #   API Clients (LinkedIn, Airtable)
 |   |-- pipelines/             #   Lead Enrichment, Content, Outreach
 |   |-- projects/              #   Web-Apps (Next.js, Payload CMS)
 |   |-- reports/               #   Daily Digest, KPI, Analytics
 |   |-- servers/               #   Telegram Bot, Webhook Server
 |   |-- services/              #   Shannon (AI Pentester), Kondo
 |   |-- tools/                 #   Utility Scripts
 |   |-- video/                 #   Videocut, Remotion
 |   +-- tinder-auto/           #   Playwright Tinder Automation
 |
 |-- .claude/skills/            # PROJEKT-SPEZIFISCHE SKILLS (28 weitere)
 |-- _archive/                  # ARCHIV (abgeschlossene Projekte)
 |-- data/                      # Datenbanken
 |-- resources/                 # Toolkit, Stellenanzeigen
 +-- Templates/                 # Obsidian Templates
```

---

## Wie es funktioniert

```
                    +------------------+
                    |    CLAUDE.md     |
                    |  Routing Table   |
                    +--------+---------+
                             |
              "Was willst du tun?"
                             |
         +-------------------+-------------------+
         |                   |                   |
    +----v----+        +-----v-----+       +-----v-----+
    |  SALES  |        |  CONTENT  |       |   VIDEO   |
    +---------+        +-----------+       +-----------+
    | prospect |       | linkedin   |      | schnitt   |
    | outreach |       | pipeline   |      | videocut  |
    | angebot  |       | repurpose  |      | remotion  |
    | enrichment|      | strategy   |      | pitch     |
    +----+-----+       +-----+------+      +-----+-----+
         |                   |                    |
         v                   v                    v
    +---------+        +-----------+       +-----------+
    | scripts/|        | scripts/  |       | scripts/  |
    |pipelines|        | pipelines |       | video/    |
    +---------+        +-----------+       +-----------+
         |                   |                    |
         v                   v                    v
    +---------+        +-----------+       +-----------+
    |Airtable |        | LinkedIn  |       | ClickUp   |
    |  CRM    |        |  API      |       | Pipeline  |
    +---------+        +-----------+       +-----------+
```

---

## Die 3 Schichten

| Schicht | Ordner | Regel |
|---------|--------|-------|
| **Wissen** | `context/` | Read-only. Wahrheit. Nie aus Outputs lernen. |
| **System** | `code/skills/`, `scripts/` | Skills + Automationen. SKILL.md ist Anleitung. |
| **Arbeit** | `workspace/` | Aktive Dateien. Ein Ordner pro Client/Projekt. |

---

## Skill-System (169 Skills total)

### Wo liegen Skills?

| Ort | Anzahl | Beschreibung |
|-----|--------|-------------|
| `code/skills/` | 103 | Business Skills (Sales, Content, Video, Web, Strategie) |
| `.claude/skills/` (Projekt) | 28 | Projekt-spezifische Skills (SEO, Ads, Humanizer) |
| `~/.claude/skills/` (System) | 38 | System-Skills (Videocut, Design, Obsidian, Debugging) |

### Jeder Skill hat:

```
skill-name/
  SKILL.md          # Anleitung: Wann, Wie, Stages, Beispiele
  examples/          # Referenz-Outputs (optional)
  references/        # Externe Docs (optional)
  scripts/           # Automations-Code (optional)
```

### Top Skills nach Kategorie

| Kategorie | Skills |
|-----------|--------|
| **Sales** | prospect-orchestrator, lead-enrichment, cold-email, door-opener, angebot-pdf |
| **Content** | linkedin-post, content-pipeline, content-repurposer, content-strategy |
| **Video** | videocut, schnitt-pipeline, video-pitch, remotion-render |
| **Web/Design** | impeccable, taste-skill, soft-skill, developer-agent |
| **Research** | deep-search, industry-scout, market-intelligence |
| **Automation** | tinder-auto (Playwright), kondo (Webhooks), telegram-command-center |

---

## Automatisierungs-Pipelines

```
 LEAD ENRICHMENT                    CONTENT PIPELINE
 ===============                    ================

 Airtable CRM                      Content Strategie
      |                                  |
      v                                  v
 waterfall_enrich.py               content-pipeline Skill
      |                                  |
      +-- Firecrawl (Website)            +-- Research
      +-- Apify (LinkedIn)               +-- Draft
      +-- PhantomBuster                  +-- Review
      +-- Email Finder                   +-- Schedule
      |                                  |
      v                                  v
 Enriched Lead                     LinkedIn / Social
      |
      v
 sequence_engine.py
      |
      v
 Outreach (Email/LinkedIn)
```

---

## Jake Van Clief Methodik

Die Ordnerstruktur folgt den Prinzipien von Jake Van Clief:

1. **CONTEXT.md in jedem Hauptordner** — Lies sie bevor du arbeitest
2. **PROGRESS.md pro Client** — Session-Start: lesen. Session-Ende: updaten.
3. **Routing Table in CLAUDE.md** — Jede Aufgabe hat einen klaren Pfad
4. **Skills-First** — Skill existiert? Folge ihm. Nicht? Baue einen.
5. **USER/SYSTEM Trennung** — `context/`, `workspace/` = User. `code/`, `scripts/` = System.
6. **Scoring & Quality Gates** — Jeder Output wird bewertet bevor er rausgeht.

---

## Externe Integrationen

| Tool | Zweck | Verbindung |
|------|-------|-----------|
| **Airtable** | CRM, Lead Pipeline | API + MCP Server |
| **ClickUp** | Projekt-/Schnitt-Pipeline | API |
| **LinkedIn** | Outreach, Content, Sales Nav | API + Playwright |
| **Telegram** | Bot, Notifications, Commands | Bot API + MCP |
| **Playwright** | Web Scraping, Automation, Tinder | Browser Automation |
| **Firecrawl** | Website Scraping | MCP Server |
| **ElevenLabs** | KI-Telefonanlage, Voice | Agent API |
| **Remotion** | Video Rendering | Node.js |
| **Claude Code** | AI Kern des Systems | CLI + Skills |

---

## Quick Start

```bash
# 1. Obsidian Vault oeffnen
#    vault/ als Obsidian Vault oeffnen

# 2. System-Skills installieren
cp -r claude-skills/* ~/.claude/skills/

# 3. Environment einrichten
cp vault/BusinessOS\ Obsidian/env-example.txt vault/BusinessOS\ Obsidian/.env
# Eigene API Keys eintragen

# 4. CLAUDE.md lesen — dort steht alles
cat vault/BusinessOS\ Obsidian/CLAUDE.md
```

---

## Ordner-Konventionen

| Typ | Namensschema | Beispiel |
|-----|-------------|---------|
| Client-Dateien | `YYYY-MM-DD-client-topic.md` | `2026-04-01-promega-outreach.md` |
| Content | `platform-topic_draft.md` | `linkedin-ki-trends_draft.md` |
| Versionen | `_v1`, `_v2` | `angebot_v2.pdf` |
| Status | `_draft` / `_review` / `_final` | `post_review.md` |

---

## Design-System

- **Fonts:** Geist, Outfit, Instrument Sans, Fraunces (nie Inter/Roboto)
- **Farben:** Off-Black `#171717`, OKLCH Farbsystem
- **Schatten:** box-shadow statt border (Vercel-Style)
- **Spacing:** letter-spacing h1: `-0.04em`, h2: `-0.03em`
- **Animation:** `cubic-bezier(0.16, 1, 0.3, 1)`

---

*Built with Obsidian + Claude Code + 169 AI Skills*
