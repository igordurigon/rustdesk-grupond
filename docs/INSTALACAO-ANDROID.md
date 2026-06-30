# Instalação no Android — Admin GrupoND

Guia de instalação do **Admin GrupoND** (acesso remoto) em celulares/tablets Android.
Esta é a versão **controladora**: serve para o time de TI **conectar e controlar** as
máquinas a partir do celular. Já vem apontada para o servidor `rustdesk.grupond.tv.br`.

- **Requisitos:** Android 5.1 (ou superior) e processador **arm64** (qualquer aparelho dos últimos ~8 anos).
- **App:** aparece como **Admin GrupoND** com o logo do Grupo ND.

---

## Parte 1 — Obter o APK (feito pela TI, uma vez)

O APK é gerado pelo GitHub Actions do projeto `rustdesk-grupond`.

1. Acesse o repositório no GitHub → aba **Actions**.
2. Na barra lateral, clique no workflow **"Build GrupoND Android Versions"**.
3. Abra a execução (run) mais recente que esteja **verde** (✔).
4. Role até o final, seção **Artifacts**, e baixe **`Admin_GrupoND_android_arm64-v8a`**.
   - O download vem como um **arquivo .zip**.
5. **Extraia o .zip** — dentro dele está o arquivo **`Admin_GrupoND_arm64-v8a.apk`**.

> ⚠️ É o `.apk` (de dentro do zip) que se instala — **não** o `.zip`.

> 💡 **Dica de distribuição:** os artefatos do GitHub **expiram** (≈90 dias) e exigem login.
> Para distribuir com facilidade ao time, hospede o `.apk` num local interno
> (pasta de rede, portal interno, etc.) e compartilhe esse link/arquivo.

---

## Parte 2 — Instalar no celular

### 2.1 — Transferir o APK para o aparelho
Envie o `Admin_GrupoND_arm64-v8a.apk` para o celular por qualquer meio:
cabo USB, Google Drive, e-mail, WhatsApp, pasta de rede, etc.

### 2.2 — Abrir o APK
No celular, abra o **Arquivos** (ou Downloads) e **toque no `.apk`**.

### 2.3 — Permitir instalação de fontes desconhecidas
Na primeira vez, o Android pede permissão para o app pelo qual você abriu o APK
(ex.: Arquivos, Chrome):
- Toque em **Configurações** quando aparecer o aviso, **OU**
- Vá em **Configurações → Apps → Acesso especial → Instalar apps desconhecidos**
  → escolha o app (ex.: **Arquivos**/**Chrome**) → ative **"Permitir desta fonte"**.
- Volte e toque no `.apk` novamente.

### 2.4 — Passar pelo Play Protect ⚠️ (passo que mais confunde)
Por ser um app **fora da Play Store**, o **Google Play Protect** mostra um aviso
de "app não reconhecido / pode ser nocivo". **Isso é esperado e não é problema do app.**

**Opção A (normal):**
1. No aviso do Play Protect, toque em **"Mais detalhes"** (More details).
2. Toque em **"Instalar mesmo assim"** (Install anyway).

> O botão "Instalar mesmo assim" geralmente só aparece **depois** de tocar em
> "Mais detalhes". Muita gente toca em "OK" e desiste sem ver a opção.

**Opção B (se a Opção A não oferecer "Instalar mesmo assim"):**
1. Abra a **Play Store**.
2. Toque na **foto do perfil** (canto superior direito).
3. **Play Protect** → ícone de **engrenagem** (Configurações).
4. **Desligue** "Verificar apps com o Play Protect".
5. Instale o `.apk`.
6. (Opcional) Religue o Play Protect depois de instalar.

### 2.5 — Concluir
Toque em **Instalar** e aguarde. O app **Admin GrupoND** aparecerá na lista de apps
com o logo do Grupo ND.

---

## Parte 3 — Usar (conectar numa máquina)

1. Abra o **Admin GrupoND**.
2. O app já está configurado para o servidor `rustdesk.grupond.tv.br` (a aba de rede
   fica oculta de propósito — não precisa configurar nada).
3. Digite o **ID** da máquina que quer acessar e toque em **Conectar**.
4. Informe a **senha** da máquina quando solicitado.

> Como esta é a versão **controladora (Admin)**, ela serve para **acessar** outras
> máquinas. Não é necessário conceder permissões de captura de tela no celular.

---

## Solução de problemas

| Sintoma | Causa provável | Solução |
|---|---|---|
| "Problema ao analisar o pacote" | Tentou instalar o **.zip**, download incompleto, ou aparelho 32-bit | Extraia e instale o **.apk**; rebaixe; confirme que o aparelho é arm64 |
| **Bloqueado pelo Play Protect** | App fora da Play Store (normal) | Parte 2.4 — "Mais detalhes" → "Instalar mesmo assim", ou desligar o Play Protect |
| "App não instalado" | Versão anterior com assinatura diferente já instalada | Desinstale a versão antiga do app e instale de novo |
| Não conecta na máquina | Máquina destino offline ou ID errado | Confirme que a máquina está ligada/online e o ID está correto |

---

*App interno do Grupo ND, baseado no RustDesk. Distribuição fora da Play Store —
o aviso do Play Protect na instalação é normal.*
