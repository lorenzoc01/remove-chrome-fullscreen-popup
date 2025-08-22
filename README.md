# Remove "Exit Fullscreen" popup in Chrome/Opera/OperaGX

A simple [Windhawk](https://windhawk.net) mod to remove the annoying “TO EXIT FULLSCREEN PRESS ESC/F11” popup in Chrome, Opera and OperaGX.

![Chrome](screenshots/chrome.png)
![OperaGX](screenshots/operagx.png)

## ⚠ Important

Based on testing, the mod works as intended. However, it **may also hide other windows** that share similar properties with the popup.

### Explanation
Apparently the popup window has this properites:
- `className` = `"Chrome_WidgetWin_1"`
- `GWL_STYLE` with flags: `WS_POPUP`  (value is: `0x86000000`)
- `GWL_EXSTYLE` with flags: `WS_EX_TOOLWINDOW`, `WS_EX_NOACTIVATE`, `WS_EX_TOPMOST`, `WS_EX_TRANSPARENT`  (value is: `0x80000a8`)
  
It is quite unlikely but if another window has the same properties, it will be hidden as well
