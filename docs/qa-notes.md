# QA Notes

Automated browser checks (Playwright + Chromium) run on the final build. Viewports tested: 360, 768, and 1280 px wide. Keyboard checks used Tab, Space, and Enter.

## Bonus feature test checks
| Feature | Type | Check | Result |
|---|---|---|---|
| F1 Assistant | layout | panel and reply visible | PASS |
| F1 Assistant | accessibility | intent selectable by keyboard (radio) | PASS |
| F1 Assistant | accessibility | chat is role=log with labelled panel | PASS |
| F1 Assistant | responsive | fits viewport at 360px | PASS |
| F1 Assistant | responsive | fits viewport at 768px | PASS |
| F2 Recommendation | layout | default card on Home | PASS |
| F2 Recommendation | layout | card changes with saved recipe | PASS |
| F2 Recommendation | accessibility | "Why this suggestion?" opens (details) | PASS |
| F2 Recommendation | accessibility | confidence shown as text label | PASS |
| F2 Recommendation | innovation | "Not helpful" hides card | PASS |
| F2 Recommendation | responsive | no sideways scroll at 360px | PASS |
| F2 Recommendation | responsive | no sideways scroll at 768px | PASS |
| F3 Progress | layout | 4 forecast cards in grid | PASS |
| F3 Progress | layout | milestone turns Done | PASS |
| F3 Progress | accessibility | overall bar has label + text status | PASS |
| F3 Progress | responsive | grid reflows at 360px | PASS |
| F3 Progress | responsive | grid reflows at 768px | PASS |
| F4 Vision | layout | overlay hidden before scan | PASS |
| F4 Vision | layout | boxes + tags visible after scan | PASS |
| F4 Vision | accessibility | button label + status text + image alt | PASS |
| F4 Vision | responsive | scan image fits at 360px | PASS |
| F5 Safety | layout | risk panel + step badges in recipe | PASS |
| F5 Safety | accessibility | badge uses icon + words (not color only) | PASS |
| F5 Safety | accessibility | callout is role=note with name | PASS |
| F5 Safety | responsive | no sideways scroll at 360px | PASS |
| F6 Models | layout | 3 cards side by side with 3 bars each | PASS |
| F6 Models | layout | choosing a model changes suggestion meter | PASS |
| F6 Models | accessibility | keyboard focus flips card + visible ring | PASS |
| F6 Models | responsive | cards stack on 360px | PASS |

## Fixes made during testing
- 9-link navigation caused sideways scrolling at 768 px. Fix: the nav now scrolls inside its own row.
- A home column was 7 px too wide at 360 px. Fix: added min-width and max-width limits.
- Model card Cost bar was clipped. Fix: taller cards.

## Still to do by the team
- Manual check in Firefox and Safari, and on a real phone.
- Screen-reader pass (NVDA or VoiceOver).
- Run the W3C validators and Lighthouse; record scores here.
