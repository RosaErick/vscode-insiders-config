# vscode-insiders-config

Minhas configs do **VS Code Insiders** (Linux).

## Instalar

### Linux / macOS

```bash
git clone https://github.com/RosaErick/vscode-insiders-config
cd vscode-insiders-config

# extensões
xargs -L1 code-insiders --install-extension < extensions.txt

# settings
cp settings.json ~/.config/"Code - Insiders"/User/            # Linux
cp settings.json ~/Library/Application\ Support/"Code - Insiders"/User/   # macOS
```

### Windows (PowerShell)

```powershell
git clone https://github.com/RosaErick/vscode-insiders-config
cd vscode-insiders-config

# extensões
Get-Content extensions.txt | ForEach-Object { code-insiders --install-extension $_ }

# settings
Copy-Item settings.json "$env:APPDATA\Code - Insiders\User\"
```

Se o `code-insiders` não for reconhecido, marque *Add to PATH* no instalador
ou rode a partir de `%LOCALAPPDATA%\Programs\Microsoft VS Code Insiders\bin\`.

No VS Code estável, troque `code-insiders` por `code` e tire o ` - Insiders`
do caminho de destino.

## Atualizar

```bash
cp ~/.config/"Code - Insiders"/User/settings.json .
code-insiders --list-extensions > extensions.txt
git commit -am "update config"
```
