---
title: "IDE 단축키"
excerpt: "생산성 향상을 위한 IDE 단축키"

categories: 
  - IT
tag:
  - Shortcut
  - IDE
  - IntellJ IDEA
  - VS Code
  - Eclipse
  - Vim
last-modified-at: 2020-01-27T22:12:00
---

## VS Code

Binding | Action
--- | ---
Ctrl+Shift+K | Delete Line
Alt+↑/↓ | Move line up/down`
Alt+←/→ | Go back/forward
Ctrl+` | Show/Hide Terminal
Ctrl + F4 | Close Editor
Ctrl + w | Close Window

> <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf>

## IntelliJ IDEA

Action | Binding
--- | ---
Organize import | Ctrl + Alt + O
Smart Code Completion | Ctrl + Shift + Space
Search Everywhere | Double Shift
Show Intention Actions and quick-fixes | Alt + Enter
Recent files popup | Ctrl + E
Rename | Shift + F6
Toggle Maximizing editor | Ctrl + Shift + F12
Move line up/down | Shift + Alt + ↑/↓  
Settings | Ctrl + Alt + S
Reformat Code | Ctrl + Alt + L
Create Test | Ctrl + Shift + T
Go to Implementation | Ctrl + Alt + B
Go to Declaration | Ctrl + B
Next Highlited Error | F2
Previous Highlited Error | Shift + F2
Override Methods | Ctrl + O
Quick Javadoc | Ctrl + Q
Generate... | Alt + Insert

> <https://resources.jetbrains.com/storage/products/intellij-idea/docs/IntelliJIDEA_ReferenceCard.pdf>

> <https://www.jetbrains.com/help/idea/mastering-keyboard-shortcuts.html>

## Android Studio

Binding | Action
--- | ---
Ctrl + Y | Delete Line
Ctrl + F9 | Make Project
Shift + F10 | Run
Ctrl + F2 | Stop

> <https://developer.android.com/studio/intro/keyboard-shortcuts>

## Vim

Action | Bindng
--- | ---
현재 커서에서 줄 끝까지 삭제 | d$ 또는 D
현재 커서에서 줄 끝까지 삭제하고 insert mode | c$ 또는 C

![](/assets/images/vim_shortcut.jpg)

![](/assets/images/vim_move_shortcut.jpg)

> 출처 : https://itisfun.tistory.com/281

### .ideavimrc

```
# 시스템 클립보드 연동
set clipboard+=unnamed

# 사용자 정의 단축키
nnoremap <leader>rr :action Run<cr>
```
* cmd 
  * n+nore+map
  * n : normal mode
  * nore : non-recursive
  * map
* attr
  * \<leader\> : \ (back slash)
  * \<space\> : Space
  * \<C-A\> : Ctrl + a
  * \<tab> : Tab
* lhs (left hand side)
  * :action
* rhs
  * command 
  * \<cr\> : Carriage Return

### ESC 키매핑 바꾸기

VIM 을 사용하면 ESC 키를 겁나게 누르게 되어 있다.  그런데 지리적으로 키보드 좌측상단에 있다보니 왼쪽 약지 손가락을 쭉펴서 찾아가야 한다. 처음 VI 가 태어날 당시에는 키보드에서 ESC 키의 위치가 현재와 달리 지금의 Tab 키 자리 였다고 한다.

![ADM-3A terminal](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/KB_Terminal_ADM3A.svg/1200px-KB_Terminal_ADM3A.svg.png)

검색해보면 여러가지 방법이 나오긴 하는데...  
일단은 jj 를 써보기로 한다.

```
:imap jj <ESC>
:imap kk <ESC>
```
### VS Code

settings.json

```json
    "vim.insertModeKeyBindings": [
      {
        "before": ["j", "j"],
        "after": ["<Esc>"]
      }
    ]
```

### .vrapperrc

파일 : %UESRPROFILE%/.vrapperrc

```
imap jj <ESC>
imap kk <ESC>
```

참고 : [Document - Configuration](http://vrapper.sourceforge.net/documentation/?topic=configuration)
