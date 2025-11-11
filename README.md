# Remove "Exit Fullscreen" popup in Chromium-based browsers

A simple [Windhawk](https://windhawk.net) mod to remove the annoying “TO EXIT FULLSCREEN PRESS ESC/F11” popup in Chromium-based browsers.

![Chrome](screenshots/chrome.png)
![OperaGX](screenshots/operagx.png)

## Browsers

Here's a list of the browsers I tested.

Supported:
- Google Chrome
- Microsoft Edge
- Opera/OperaGX
- Brave
- Maxthon
- Naver Whale
- Aloha
- Comet

Unsupported (not working):
- Vivaldi
- Yandex


The mod might work with other browsers. If you want to test it, you can add the executable name in the mod includes:

`// @include         chrome.exe`

## ⚠ Important

Based on testing, the mod works as intended. However, it **may also hide other windows** that share similar properties with the popup.

### Explanation
Apparently the popup window has this properites:
- `className` = `"Chrome_WidgetWin_1"`
- `GWL_STYLE` with flags: `WS_POPUP`  (value is: `0x86000000`)
- `GWL_EXSTYLE` with flags: `WS_EX_TOOLWINDOW`, `WS_EX_NOACTIVATE`, `WS_EX_TOPMOST`, `WS_EX_TRANSPARENT`  (value is: `0x80000a8`)
  
It is quite unlikely but if another window has the same properties, it will be hidden as well


