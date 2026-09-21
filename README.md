# Fôlego — Landing Page

Landing page do Fôlego, projeto de empreendedorismo do MBM12 (Insper).
Página única, sem build e sem dependências: todo o CSS e o JS estão dentro do `index.html`.

## Conteúdo

- `index.html` — a página inteira
- `.nojekyll` — desliga o processamento Jekyll do GitHub Pages (arquivo vazio, de propósito)

## Publicar no GitHub Pages

1. Crie um repositório **público** no GitHub.
2. Suba os arquivos desta pasta na raiz do repositório.
3. Settings → Pages → Build and deployment → Source: **Deploy from a branch**, branch `main`, pasta `/ (root)`.
4. Em 1 a 2 minutos a página fica no ar em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

### Pela linha de comando, se preferir

    git init
    git add .
    git commit -m "Landing page do Folego"
    git branch -M main
    git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPO.git
    git push -u origin main

## Domínio próprio

`github.io` não é domínio próprio. Para usar um `.com.br`:

1. Registre o domínio (no Brasil, registro.br).
2. **Primeiro** cadastre o domínio em Settings → Pages → Custom domain e salve.
   Fazer o inverso, mexer no DNS antes, abre brecha para sequestro de subdomínio.
3. No DNS, quatro registros `A` no apex `@`:
   185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
4. Um `CNAME` de `www` para `SEU-USUARIO.github.io` (sem o nome do repositório).
5. Propagação em até 24h. Quando liberar, marque **Enforce HTTPS**.

## Antes de publicar: o que ainda falta

- [ ] **Trocar o número do WhatsApp.** No `index.html`, procure por `const WHATSAPP` e
      substitua `5511999999999` pelo número real, no formato 55 + DDD + número.
      Sem isso o botão principal da página não funciona.
- [ ] **Conferir o e-mail do rodapé** (`contato@folego.com.br`). Só funciona se o domínio for seu.
- [ ] **Depoimentos.** A seção `<section class="vozes" ... hidden>` está pronta e oculta.
      Preencha os `<figure class="voz">` com depoimentos reais e tire o atributo `hidden`.
      Se preencher só um ou dois, os placeholders restantes somem sozinhos.
- [ ] **Contador de engajamento.** Em `<span class="contador" ... data-n="0" hidden>`,
      troque o `data-n` pelo número real de pessoas que pediram o teste e tire o `hidden`.

## Observações

- O repositório precisa ser público no plano gratuito do GitHub, ou seja,
  o código-fonte fica visível. O número de WhatsApp colocado aqui vira um dado público.
- Depoimentos com nome, empresa e cargo de pessoas reais numa página pública
  pedem autorização explícita de cada pessoa.
