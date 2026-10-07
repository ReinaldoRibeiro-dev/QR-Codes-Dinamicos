# QR Dinâmico (GitHub Pages)

Site estático, sem servidor. Os QR codes apontam para `https://SEU-USUARIO.github.io/REPO/?c=ID`;
o destino de cada ID fica em `codes.json`. O painel `admin.html` edita esse arquivo pela API do GitHub.

## Como publicar
1. Crie um repositório no GitHub (público) e envie estes arquivos para a raiz.
2. Em **Settings → Pages**, escolha *Deploy from a branch*, branch `main`, pasta `/ (root)`.
3. Acesse `https://SEU-USUARIO.github.io/REPO/admin.html`.
4. Crie um token em **Settings → Developer settings → Personal access tokens → Fine-grained tokens**:
   acesso apenas a este repositório, permissão **Contents: Read and write**.
5. Cole o token no painel, clique em *Conectar* e crie seus QR codes.

## Observações
- Mudanças de destino levam de segundos a alguns minutos para valer (cache do GitHub Pages).
- O token fica só no navegador (localStorage). Use um token restrito a este repo e com validade curta.
- `codes.json` é público: não coloque URLs secretas.
- Não há contagem de escaneamentos. Para isso, use um backend próprio.
- Domínio próprio: configure em Settings → Pages e os QRs passam a usar o novo endereço automaticamente
  (reimprima se já tiver impressos com o endereço antigo).
