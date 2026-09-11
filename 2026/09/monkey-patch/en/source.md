/comic 最终方案

(The converged /peerreview design, 2026-09-11, verbatim:)

- Title: Monkey Patch
- Language: English
- Accent: orange #FF6B35 on the test result labels and the clock patch, strongest in panel 3
- Roles: Developer (glasses); Monkey (monkey-ear headband, clip-on curly tail); Townsfolk (crowd)
- Caption: Patch a shared clock, and its readers see the fake time.

| Panel | Beat | Picture | Line |
|---|---|---|---|
| 1 | 起 Setup | Developer at a desk; laptop shows an orange FAIL label. Through one window, the analog town clock's hands show 9:00, with no digits on its face. | Developer: "This test only passes at midnight." |
| 2 | 承 Development | Same desk and window: the laptop shows an orange PASS label while the monkey covers the clock with an orange analog face whose hands point to midnight, with no digits. | Developer: "It passes!" |
| 3 | 转 Turn | A small black sun icon and corner label "9:05 AM" establish daytime. The orange analog patch, its hands still at midnight and no digits, dominates the frame; a crowd points up. | Townsfolk: "Why is it midnight?" |
| 4 | 合 Conclusion | The test is over. The monkey holds the removed patch; the uncovered analog clock's hands show 9:05, with no digits. The developer nods. | Monkey: "Patch it, test it, peel it off." |

The patch is literally a fake clock face laid over the real one, like replacing the `time.time`
attribute on the shared `time` module object: callers in that process that look up `time.time`
while the patch is active see the replacement. (A caller that previously saved its own reference
does not.) The crowd in panel 3 makes that shared-state effect visible without code, and panel 4
shows the original restored after the test, as `unittest.mock.patch` does when its `with` block
exits.
