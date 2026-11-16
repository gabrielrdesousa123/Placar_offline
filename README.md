# 🎯 Placar Bocha Offline — SCBP

**Placar digital completo para partidas de Bocha Paralímpica (Boccia), 100% offline.**

Uma réplica fiel do placar ao vivo do [SCBP](https://scboccia.com) (Sistema de Campeonatos de Bocha Paralímpica), funcionando em um único arquivo HTML sem necessidade de servidor, internet ou instalação. Ideal para árbitros, organizadores de competições e treinadores que precisam registrar partidas em qualquer lugar.

---

## 🌐 Idiomas / Languages / Idiomas

- 🇧🇷 **Português (BR)** — [README.md](README.md) ← você está aqui
- 🇺🇸 **English** — [README.en.md](README.en.md)
- 🇪🇸 **Español** — [README.es.md](README.es.md)

O próprio placar possui um **seletor de idioma** no topo (PT | EN | ES).

---

## ✨ Funcionalidades

### ⚽ Durante a partida
- **Placar gigante** vermelho × azul, igual ao SCBP oficial
- **Timer individual por atleta** com play/pause (tempo conta separado para cada lado)
- **Parciais (Ends)**: P1, P2, P3, P4 + Tiebreak (TB1, TB2) com placar separado
- **Bolas por end** com contadores clicáveis (+/−)
- **Violações completas** baseadas no Artigo 16 das Regras World Boccia 2025-2028:
  - Retração (Art. 16.5)
  - Bola de Penalidade (Art. 16.6)
  - Retração + Penalidade (Art. 16.7)
  - Penalidade + Amarelo (Art. 16.8)
  - Cartão Amarelo (Art. 16.9)
  - Cartão Vermelho (Art. 16.11)
  - Forfeit (Art. 16.12)
- **Contador de bolas de penalidade (1P)** com chip amarelo
- **Tiebreak automático** quando há empate ao fim do último end
- **Persistência automática** em `localStorage` — feche o navegador e continue de onde parou

### 📺 Telão / Scoreboard
- Botão **"Telão"** no menu abre uma nova aba com layout de TV para exibição em quadra
- Atualização automática a cada 2 segundos (lê o `localStorage`)
- Ideal para TVs, projetores ou tablets na lateral da quadra

### 📄 Súmula oficial
- Modal com súmula **idêntica** ao modelo World Boccia / ANDE usado no SCBP
- Tabela de parciais com tempos de cada atleta
- Violações agrupadas (com contador "N × 1 Bola de Penalização")
- Box do vencedor com borda destacada
- **Botão "Imprimir / Salvar PDF"** — usa a impressão nativa do navegador, funciona offline

### 🏅 Classes oficiais suportadas
| Classe | Modalidade | Ends | Bolas/atleta | Tempo/parcial |
|--------|------------|------|--------------|----------------|
| BC1 | Individual | 4 | 6 | 4:30 min |
| BC2 | Individual | 4 | 6 | 3:30 min |
| BC3 | Individual (c/ RO) | 4 | 6 | 6 min |
| BC4 | Individual | 4 | 6 | 3:30 min |
| Pares BC3 | Dupla | 4 | 3 | 7 min |
| Pares BC4 | Dupla | 4 | 3 | 4 min |
| Equipe | Trio (BC1+BC2) | 6 | 2 | 5 min |
| ⚙️ Custom | Personalizado | 1-10 | 1-6 | 60-900s |

### 💻 Desktop
- Aplicativo para computador (Windows, Mac, Linux)
- Modo tela cheia (F11) disponível no menu

---

## 🚀 Como usar

### Opção 1 — Download direto (recomendado)
1. Baixe o arquivo [`index.html`](./index.html) deste repositório
2. Abra com duplo clique em qualquer navegador moderno (Chrome, Edge, Firefox, Safari)
3. Pronto! Não precisa de instalação, servidor ou internet

### Opção 2 — Clonar o repositório
```bash
git clone https://github.com/gabrielrdesousa123/Placar_offline.git
cd Placar_offline
# Abra o index.html no navegador
```

### Opção 3 — Usar como PWA
No Chrome/Edge, clique no ícone "Instalar" na barra de endereços para ter o placar como aplicativo no desktop ou celular.

---

## 🎮 Passo a passo rápido

1. **Selecione a classe** (BC1, BC2, BC3, BC4, Pares, Equipe ou Custom)
2. **Preencha nomes** (opcional — se deixar vazio, assume "VERMELHO" e "AZUL")
3. **Adicione clubes/equipes** (opcional)
4. Clique em **▶ INICIAR PARTIDA**
5. Use os botões ▶ ao lado de cada timer para controlar o tempo de cada atleta
6. Clique nos números do placar para adicionar pontos (+1)
7. Use os botões **−** e **+** para controlar as bolas lançadas
8. Clique em **⚠️ Adicionar Violação** para registrar infrações
9. Clique em **PRÓXIMO END ▶** para avançar
10. Ao final, clique em **☰ Menu → Ver Súmula → Imprimir / Salvar PDF**

---

## 💾 Armazenamento

- Todos os dados ficam salvos no `localStorage` do navegador
- Ao reabrir a página, a partida continua de onde parou
- Para começar um jogo novo: **☰ Menu → Zerar Jogo Completo**

---

## 📂 Estrutura do projeto

```
Placar_offline/
├── index.html        ← Placar completo (HTML + CSS + JS em um só arquivo)
├── README.md         ← Este arquivo (Português)
├── README.en.md      ← README em Inglês
├── README.es.md      ← README em Espanhol
└── LICENSE           ← Licença MIT
```

**Zero dependências externas.** Tudo está embutido no `index.html` (~55 KB).

---

## 🧠 Regras implementadas

Este placar segue as **Regras Oficiais da World Boccia (BISFed) 2025-2028**, em especial:

- **Art. 10.16** — Critérios de desempate (Tiebreak)
- **Art. 16** — Violações e penalidades (16.5 a 16.12)
- **Seção 2.1.5.1** — Placar de W.O. (6-0 ou maior diferença)

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Abra uma issue ou pull request.

---

## 📜 Licença

[MIT License](LICENSE) — livre para uso pessoal, comercial e modificações.

---

## 🔗 Links

- **SCBP (sistema online):** [scboccia.com](https://scboccia.com)
- **World Boccia:** [worldboccia.com](https://worldboccia.com)
- **Autor:** Gabriel R. de Sousa

---

## ❓ Perguntas frequentes

**Funciona sem internet?**
Sim, 100%. É um arquivo HTML autocontido.

**Os dados são enviados para algum servidor?**
Não. Tudo fica no seu navegador (localStorage). Nenhum dado sai do dispositivo.

**Posso usar em competições oficiais?**
Sim. O layout e as regras são idênticos aos usados no SCBP, sistema adotado pela ANDE e por diversas competições brasileiras de Bocha Paralímpica.

**Onde fica a súmula?**
No menu ☰ lateral, opção "Ver Súmula". Você pode imprimir ou salvar como PDF.

**Como abrir o telão?**
No menu ☰ lateral, opção "Telão / Scoreboard". Uma nova aba abre com o placar ampliado, ideal para TVs na quadra.