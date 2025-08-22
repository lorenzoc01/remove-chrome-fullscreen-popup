# Remove "Press Esc to Exit Fullscreen" popup – Chrome/Opera/OperaGX

A simple [Windhawk](https://windhawk.net) mod to remove the annoying “TO EXIT FULLSCREEN PRESS ESC/F11” popup in Chrome, Opera and OperaGX.

![Chrome](screenshots/chrome.png)
![OperaGX](screenshots/operagx.png)

## ⚠ Important

Based on testing, the mod works as intended. However, it **may also hide other windows** that share similar properties with the popup.

### Explanation
Apparently the popup window has this properites:
- hWndParent = nullptr
- lpWindowName = nullptr
- className = "Chrome_WidgetWin_1"
- windowHeight = 0

If any other window meets this criteria, it may be hidden as well.
