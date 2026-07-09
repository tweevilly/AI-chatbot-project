# Intro to Artificial Intelligence 
**WESTERN GOVENORS UNIVERSITY**
C951 |Task1 | Virtual Career Advisor Chatbot

## About
A rule-based chatbot built with [AIML](https://en.wikipedia.org/wiki/AIML) on the [Pandorabots](https://www.pandorabots.com/) platform. 
Maki acts as a virtual career advisor for computer science students, helping them explore computing careers that match their interests through a guided, decision-tree conversation.
Maki is a conversational AI chatbot developed as part of an Artificial Intelligence and Machine Learning (AIML) coursework project.

## Objective ##
  Implement fundamental AIML concepts in a real-world application
  Build a functional conversational AI system
  Demonstrate Natural Language Processing techniques
  Design structured dialogue handling
  Explore intelligent response generation

## Key Features  ##
  Natural language input processing
  Intent recognition
  Automated response generation
  Rule-based / ML-based logic (update based on your implementation)
  Interactive conversational interface
  
## Overview
The scenario: a university's computer science program has grown too large for career advisors to meet individually with every student. Maki simulates a short advising session — greeting the student, identifying their area of interest, and recommending a matching career path with salary expectations, education requirements, and concrete next steps — without requiring a human advisor to be present.

## Conversation flow
1. **Greeting** — any input triggers a welcome message introducing Maki as a virtual career advisor and asks the student to confirm they'd like to begin (`YES`).
2. **Interest selection** — the student picks one of five areas, either by number or by keyword (e.g. `1` or `building software`).
3. **Career recommendation** — Maki suggests a matching career and offers to go deeper (`MORE`) or return to the menu (`OTHER`).
4. **Details** — `MORE` returns a job description, typical degree requirement, and entry-level salary.
5. **Next steps** — `NEXT` returns actionable preparation advice (portfolio building, relevant skills, certifications).
6. **Closure** — `SATISFIED`, `NO`, or `BYE` ends the session with a closing message; `OTHER` loops back to the interest menu.

## Careers Maki recommends
| Interest              | Career                  |
|------------------------|--------------------------|
| Building software       | Software Developer       |
| Working with data       | Data Analyst             |
| Securing systems        | CyberSecurity Analyst    |
| Managing networks       | Systems Administrator    |
| Designing websites      | Web Developer             |

## Repository contents
| File | Description |
|---|---|
| `pandorabot_code.txt` | AIML source for the chatbot — categories for greeting, the five career paths, and session closure. |

## Running it yourself
Pandorabots' free tier doesn't expose a public URL for every bot, so to try Maki you'll need to deploy it under your own account:

1. Create an account at [pandorabots.com](https://www.pandorabots.com/).
2. From the dashboard, create a new bot and upload `pandorabot_code.txt` as its AIML source.
3. Open the bot's test console and try the flow above — start with any greeting, then `YES` to reach the main menu.

## Design notes
AIML's `<pattern>` tags map student input to responses, `<topic>` tags keep the conversation scoped to the selected career (so `MORE` after picking Data Analyst only returns Data Analyst details), and `<srai>` tags let inputs like number keys or free-text phrases (`BUILDING *`) redirect to the same response, avoiding duplicated categories.

The main tradeoff of this approach is that AIML is pattern-matching, not true language understanding — the bot needs close-to-exact keywords (`more`, `next`, `yes`) and won't reliably parse full sentences or paraphrased input. It's well suited to a structured, decision-tree-style advising session, but doesn't generalize beyond the paths it was explicitly programmed for.


