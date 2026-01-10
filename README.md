# LimitMiddleClickPaste

Prevent middle click pasting either always or just when a text area is not focused.

Available natively in [Equicord](https://github.com/Equicord/Equicord), a Vencord fork, or as a userplugin (you're here!) in [Vencord](https://github.com/Vendicated/Vencord/).

## Features
1. Scope
    - Prevent middle click from pasting always.
    - Prevent middle click from pasting if an input is not focused.
2. Threshold
    - Custom duration after a middle click occurs in which pasting is blocked.
    - Due to the nature of how paste events are handeled in javascript, there is no way to differentiate between a middle click paste or an alternate paste method, such as `ctrl+v`. As such, when a middle click is detected, ALL pasting is locked for the duration of this threshold. Lower thresholds will unlock pasting quicker, but run the risk of unlocking pasting before the middle click paste event has fired on slower systems. The default value is `100` milliseconds, and I personally use `50` milliseconds. Experiment to find the smallest value that works reliably on your system.
