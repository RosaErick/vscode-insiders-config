# vscode-insiders-config

Minhas configs do **VS Code Insiders** (Linux).

## Instalar

```bash
git clone https://github.com/RosaErick/vscode-insiders-config
cd vscode-insiders-config

# extensões
xargs -L1 code-insiders --install-extension < extensions.txt

# settings
cp settings.json ~/.config/"Code - Insiders"/User/
```

No VS Code estável, troque `code-insiders` por `code` e o destino por
`~/.config/Code/User/`. Outros sistemas:

| OS      | destino                                            |
|---------|----------------------------------------------------|
| macOS   | `~/Library/Application Support/Code - Insiders/User/` |
| Windows | `%APPDATA%\Code - Insiders\User\`                  |

## Atualizar

```bash
cp ~/.config/"Code - Insiders"/User/settings.json .
code-insiders --list-extensions > extensions.txt
git commit -am "update config"
```
