# Como instalar o Admin GrupoND no Android

Aplicativo de acesso remoto do Grupo ND. **Você recebeu o instalador pelo WhatsApp** —
siga os passos abaixo. O app aparece como **Admin GrupoND** e já vem pronto para uso
(não precisa configurar servidor nem digitar endereço).

> **Requisitos:** Android 5.1 ou superior.

---

## Passo 1 — Baixar o instalador
Você vai receber pelo WhatsApp **um link** ou **um arquivo**:
- **Se for um link** (Google Drive, etc.): toque no link → **Baixar**. Vai para a pasta *Downloads*.
- **Se for um arquivo `.zip`**: toque nele → **Extrair**. Dentro há o arquivo que termina em `.apk` — é esse que será instalado.

## Passo 2 — Abrir o instalador
Abra o app **Arquivos** (ou **Downloads**), encontre o **Admin_GrupoND...apk** e **toque nele**.

## Passo 3 — Permitir a instalação
Na primeira vez o Android pede permissão. Quando aparecer o aviso:
1. Toque em **Configurações** (no próprio aviso).
2. Ative **"Permitir desta fonte"**.
3. Volte e toque no `.apk` de novo.

## Passo 4 — Liberar no Play Protect ⚠️ (atenção!)
Como o app não vem da Play Store, o **Google Play Protect** avisa que o app "não foi
reconhecido". **Isso é normal e seguro** — é um app interno do Grupo ND. Para continuar:
1. Toque em **"Mais detalhes"**.
2. Toque em **"Instalar mesmo assim"**.

> ⚠️ O botão **"Instalar mesmo assim"** só aparece **depois** de tocar em **"Mais detalhes"**.
> Se tocar em "OK", o app **não** instala — procure sempre por "Mais detalhes".

## Passo 5 — Concluir
Toque em **Instalar** e aguarde. O **Admin GrupoND** aparece na lista de apps com o logo do Grupo ND.

---

## Como usar — conectar numa máquina
1. Abra o **Admin GrupoND**.
2. Digite o **ID** da máquina que quer acessar e toque em **Conectar**.
3. Digite a **senha** da máquina quando solicitado.

> O app já está configurado para o servidor do Grupo ND — não precisa mexer em rede.

---

## Se algo der errado

| O que aconteceu | O que fazer |
|---|---|
| Não acho "Instalar mesmo assim" | Toque primeiro em **"Mais detalhes"** no aviso do Play Protect |
| "Problema ao analisar o pacote" | Arquivo incompleto ou você abriu o `.zip` — baixe de novo e instale o `.apk` |
| "Aplicativo não instalado" | Existe versão antiga instalada — desinstale e tente de novo |
| Não conecta na máquina | Confirme que a máquina está ligada/online e o ID está correto |

---

## 🔧 Nota para a TI (quem envia)
O WhatsApp normalmente **bloqueia o envio de arquivos `.apk`**. Envie de uma destas formas:
1. **Link (recomendado):** suba o `.apk` no Google Drive/pasta interna e mande o **link** — mais simples para o usuário.
2. **Zip:** compacte o `.apk` em `.zip` e envie o zip (o usuário extrai).

O APK é gerado no GitHub Actions (workflow **"Build GrupoND Android Versions"** → **Artifacts** →
`Admin_GrupoND_android_arm64-v8a`). ⚠️ Os artefatos do GitHub **expiram em ~90 dias** — para
distribuição contínua, hospede o `.apk` num local interno fixo.

---

*App interno do Grupo ND, baseado no RustDesk. Distribuição fora da Play Store —
o aviso do Play Protect na instalação é normal.*
