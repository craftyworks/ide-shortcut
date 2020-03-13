# 🐵 IDE 단축키

생산성 향상을 위한 IDE 단축키

* Visual Studio Code
* IntelliJ IDEA
* Android Studio
* Vim

## Visual Studio Code

Action | Binding
--- | ---
Delete Line | Ctrl + Shift + K | 
Move line up/down | Alt + ↑/↓ | 
Go back/forward | Alt + ←/→ | 
Show/Hide Terminal | Ctrl + ` | 
Close Editor | Ctrl + F4 | 
Close Window | Ctrl + w | 

> https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf

### VSCodeVim

settings.json

```json
    "vim.useSystemClipboard": true,
    "vim.insertModeKeyBindings": [
      {
          "before": ["j", "j"],
          "after": ["<Esc>"]
      },
      {
          "before": ["k", "k"],
          "after": ["<Esc>"]
      }
    ],
```
> https://github.com/VSCodeVim/Vim

## IntelliJ IDEA

Action | Binding
--- | ---
Show Intention Actions and quick-fixes | Alt + Enter
Smart Code Completion | Ctrl + Shift + Space
Rename | Shift + F6
Search Everywhere | Double Shift
Toggle Maximizing editor | Ctrl + Shift + F12
Recent files popup | Ctrl + E
Move line up/down | Shift + Alt + ↑/↓  
Reformat Code | Ctrl + Alt + L
Organize import | Ctrl + Alt + O
Settings | Ctrl + Alt + S
Go to Implementation | Ctrl + Alt + B
Go to Declaration | Ctrl + B
Next Highlited Error | F2
Previous Highlited Error | Shift + F2
Create Test | Ctrl + Shift + T
Override Methods | Ctrl + O
Generate... | Alt + Insert
Quick Javadoc | Ctrl + Q

> https://resources.jetbrains.com/storage/products/intellij-idea/docs/IntelliJIDEA_ReferenceCard.pdf

> https://www.jetbrains.com/help/idea/mastering-keyboard-shortcuts.html

### .ideavimrc

```
set clipboard+=unnamed

nnoremap <leader>rr :action Run<cr>
nnoremap <leader>ss :action Android.SyncProject<cr>

imap jj <ESC>
imap kk <ESC>

```
## Android Studio

Action | Binding | 
--- | ---
Delete Line | Ctrl + Y | 
Make Project | Ctrl + F9 | 
Run | Shift + F10 | 
Stop | Ctrl + F2 | 

> https://developer.android.com/studio/intro/keyboard-shortcuts

## Vim

Action | Bindng
--- | ---
현재 커서에서 줄 끝까지 삭제 | d$ 또는 D
현재 커서에서 줄 끝까지 삭제하고 insert mode | c$ 또는 C

![](/assets/images/vim_shortcut.jpg)

![](/assets/images/vim_move_shortcut.jpg)

> 출처 : https://itisfun.tistory.com/281

### ESC 키매핑 바꾸기

VIM 을 사용하면 ESC 키를 겁나게 누르게 되어 있다.  그런데 지리적으로 키보드 좌측상단에 있다보니 왼쪽 약지 손가락을 쭉펴서 찾아가야 한다. 처음 VI 가 태어날 당시에는 키보드에서 ESC 키의 위치가 현재와 달리 지금의 Tab 키 자리 였다고 한다.

![ADM-3A terminal](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/KB_Terminal_ADM3A.svg/1200px-KB_Terminal_ADM3A.svg.png)

검색해보면 여러가지 방법이 나오긴 하는데...  
일단은 jj 를 써보기로 한다.

```
:imap jj <ESC>
:imap kk <ESC>
```

### .vrapperrc

파일 : %UESRPROFILE%/.vrapperrc

```
imap jj <ESC>
imap kk <ESC>
```

참고 : [Document - Configuration](http://vrapper.sourceforge.net/documentation/?topic=configuration)
