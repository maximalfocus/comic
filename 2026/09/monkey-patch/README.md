# 猴子补丁 / Monkey Patch

**Shared thread:** a monkey patch replaces something every part of a program shares, so everyone
reading it sees the fake; whoever applies it must remove it after the test (`unittest.mock.patch`
in a `with` block does this automatically).

## How the two versions differ

| | en: Monkey Patch | zh: 猴子补丁 |
|---|---|---|
| The monkey | a stick-figure monkey | 孙悟空 (golden fillet, staff, 筋斗云) |
| The patch | a fake midnight clock face | a "定" talisman: 贴符 = patch, 揭符 = unpatch |
| The shared thing | the town clock tower | the office punch clock |
| The turn | the town wonders why it is midnight | 天黑了还是九点, nobody can clock out |
| The lesson | "Patch it, test it, peel it off." | "定！" / "解！", 解铃还须系铃人 |

Kept identical because culture-neutral: the technical claim, the four-beat structure, the orange
accent on the patch.

## Published

- en: Substack, web only, no email, 2026-09-12 — https://maximalfocus.substack.com/p/monkey-patch
