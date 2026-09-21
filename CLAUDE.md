# CLAUDE.md — Perfil GitHub (repositório especial `<usuario>/<usuario>`)

## Objetivo do projeto
Construir o README.md do repositório especial do GitHub (mesmo nome do usuário),
que é exibido automaticamente na página de perfil. Público-alvo: recrutadores e
devs da área de desenvolvimento **mobile**. Tom: **profissional e sério** — sem
emoji em excesso, sem visual de "tutorial básico", sem gambiarra estática.

Regra de ouro: nada de HTML estático simples e parado. O perfil deve usar
automações reais (GitHub Actions) que se atualizam sozinhas, não apenas imagens
fixas coladas no README.

## Identidade visual (consistente com o banner já feito para o LinkedIn)
- Paleta de azul: `#1862BA` (azul céu vivo), `#072254` (azul marinho profundo),
  `#0D0D10` (preto), `#F7F9FC` (branco quase puro).
- Mesmo espírito do banner do LinkedIn: fundo escuro/azul, tipografia bold
  condensada para destaques, badges/tags no estilo "+ TAG" quando fizer sentido.

## Assets disponíveis
Pasta local com as imagens já existe no projeto (`assets/` ou equivalente):
- `assets/banner.png` — banner já usado no LinkedIn, pode ser reaproveitado
  como imagem de topo do README se fizer sentido visualmente.
- `assets/foto-perfil.png` — foto pessoal. **Provavelmente não será usada**
  neste README (o avatar do GitHub já cobre esse papel); só usar se a
  composição do hero pedir uma imagem da pessoa além do banner.

## Redes sociais / contato (usar no rodapé, com ícones via shields.io)
- LinkedIn: https://www.linkedin.com/in/kaio-silva-6459372b8/
- TikTok: https://www.tiktok.com/@kaiosilva1411

## Estrutura do README.md (ordem)
1. **Hero/topo**: nome centralizado (com `<p align="center">`) + efeito de
   digitação animado (`readme-typing-svg`) alternando frases como abaixo.
   Usar o banner (`assets/banner.png`) aqui só se a composição pedir; a foto
   pessoal não entra nesta seção (ver "Assets disponíveis"):
   - "Mobile Developer em formação"
   - "React Native & TypeScript"
   - "Sempre aprendendo, sempre construindo"
2. **Badges de tecnologia** (shields.io + Simple Icons), nesta ordem de
   prioridade: React Native, TypeScript, Expo, JavaScript, React, Node.js,
   Git/GitHub, SQLite, HTML5, CSS3.
3. **Sobre** — 2 a 3 linhas, reaproveitando o tom já usado no "Sobre" do
   LinkedIn: migração de carreira, Ensino Médio Integrado ao Técnico em
   Desenvolvimento de Sistemas, foco em mobile, aprendizado na prática.
4. **Estatísticas do GitHub** — `github-readme-stats` (stats card) +
   `github-readme-streak-stats` (streak) lado a lado.
5. **Atividade automatizada** — dashboard gerado via GitHub Action
   `lowlighter/metrics` (linguagens mais usadas, atividade recente).
6. **Rodapé** — ícones (via shields.io) linkando para LinkedIn e TikTok
   (ver seção "Redes sociais / contato" abaixo), alinhados ao centro,
   sem texto solto ao lado — só os ícones clicáveis.

## Tecnologias/ferramentas a usar
- **GitHub Actions + `lowlighter/metrics`** — dashboard automático que se
  regenera a cada execução agendada (não é imagem estática).
- **`github-readme-stats`** — cards de estatísticas via URL de imagem.
- **`github-readme-streak-stats`** — sequência de contribuições.
- **`readme-typing-svg`** — animação de digitação no topo.
- **Shields.io** — badges de tecnologia e status.
- **Simple Icons / Devicon** — ícones oficiais das tecnologias nos badges.
- **`platane/snk`** (opcional, se quiser um toque extra) — Action que gera
  uma animação de "snake" comendo o gráfico de contribuições.

## Regras técnicas
- O README.md fica na raiz do repositório especial `<usuario>/<usuario>`.
- Usar Markdown + tags HTML que o GitHub renderiza (`<p align="center">`,
  `<img>`, `<details>`, `<table>`) — o GitHub **não executa CSS externo nem
  JavaScript** no README, então toda "animação" vem de imagens SVG/GIF já
  geradas por serviços externos ou por GitHub Actions, nunca de script.
- Qualquer imagem estática (foto, banner) deve ter alt text descritivo.
- Priorizar automação (Actions) sobre imagem fixa sempre que a tecnologia
  acima oferecer as duas opções.
- Manter consistência de paleta e tom com o perfil do LinkedIn já criado.

## Fora de escopo
- **Sem seção de projetos/repositórios** — isso já aparece separadamente nos
  repositórios fixados ("pinned") do GitHub; este README é só o perfil.
- Sem "Snake" ou animações decorativas se elas comprometerem o tom sério
  (usar com moderação, no máximo uma).
- Sem seção de hobbies/curiosidades pessoais — o foco é 100% profissional.
- Sem badges de contagem de visitas ("profile views") — não agrega
  credibilidade para recrutador.