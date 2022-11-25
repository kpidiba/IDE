# CONFIGURATION

It is about modification of the idea which improve productivity or make it more comfortable

1. **FIRA CODE**

Fira Code is a free monospaced font containing ligatures for common programming multi-character combinations. This is just a font rendering feature: underlying code remains ASCII-compatible. This helps to read and understand code faster. For some frequent sequences like `..` or `//`, ligatures allow us to correct spacing.

- Go to Fira code github page and click on **how to Install**

- follow the instructions and install the fonts

- follow the instructions and add it to vs code
2. **settings.json**

Go to the **command palette**(Ctrl + Shift +p) and type settings.json choose **open user settings.json**, go to the command palette and type settings.json choose open user settings.

-  **"editor.renderWhitespace": "trailing",** : know the number of space or tabulation,

- **"editor.suggest.insertMode": "replace",** :replace the old suggestion with a new one and not add it before

- **"editor.acceptSuggestionOnCommitCharacter": false,** : do not take the first suggestion directly.

- **"files.autoSave": "afterDelay",** :autosave after time

- **"workbench.tree.indent": 15,** : explorer ident

- **"git.enableSmartCommit": true,** : easy commit

- **"editor.lineHeight": 26,** : the height between the lines

- **"gitlens.hovers.currentLine.over": "line",** : informations about a line
3. **keybindings.json**

Define keyboard shortcuts,Go to the **command palette**(Ctrl + Shift +p) and type   **open keyboard shortcut (JSON)**

- **Expand Selection**
  
  ```json
  {
          "key": "ctrl+e",
          "command": "editor.action.smartSelect.expand",
          "when": "editorTextFocus"
  }
  ```

- **Create New File**
  
  ```json
  {
      "key": "ctrl+n",
      "command": "explorer.newFile"
  }
  ```

- **Document Format**
  
  ```json
  {
      "key": "ctrl+alt+l",
      "command": "editor.action.formatDocument"
  }
  ```

- **Default Formatter**
  
  ```json
   "[javascript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
  ```

- **CONFIG FOR TODO TREE EXTENSION**
  
  ```json
  "todo-tree.highlights.defaultHighlight": {
      "icon": "alert",
      "type": "text-and-comment",
      "foreground": "black",
      "background": "white",
      "opacity": 50,
      "iconColour": "blue",
      "gutterIcon": true,
  },
  "todo-tree.highlights.customHighlight": {
      "TODO": {
          "icon": "check",
          "foreground": "black",
          "background": "white",
          "iconColour": "white",
      },
      "NOTE": {
          "icon": "note",
          "foreground": "white",
          "background": "gray",
          "iconColour": "gray",
      },
      "COMMENT": {
          "icon": "note",
          "foreground": "white",
          "background": "gray",
          "iconColour": "gray",
      },
      "FIXME": {
          "foreground": "black",
          "background": "yellow",
          "iconColour": "yellow",
      },
      "BUG": {
          "foreground": "black",
          "background": "red",
          "iconColour": "red",
      },
      "[ ]": {
          "icon": "check",
          "foreground": "black",
          "background": "white",
          "iconColour": "yellow",
      },
      "[x]": {
          "icon": "check",
          "foreground": "white",
          "background": "green",
          "iconColour": "green",
      }
  },
  "todo-tree.general.tags": [
      "BUG",
      "HACK",
      "FIXME",
      "TODO",
      "NOTE",
      "COMMENT",
      "[ ]",
      "[x]"
  ],
  "todo-tree.regex.regex": "(//|#|<!--|;|/\\*|^|^\\s*(-|\\d+.))\\s*($TAGS).*(\\n\\s*//\\s{2,}.*)*",
  ```
4. 
