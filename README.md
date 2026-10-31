# Legend of Mana (PSX) — Tradução PT-BR

Tradução para português do Brasil do Legend of Mana de PlayStation (versão americana).

**[⬇ Baixar a versão mais recente](https://github.com/alexcominoti/LoM/releases/latest)**

## O que está traduzido (v1.0.0)

- Tradução completa de todos os diálogos, enciclopédias e menus.
- Imagens traduzidas: títulos dos eventos, telas de fim de evento, telas de título, nomes de armas e menus,
  efeitos de batalha.
- Ainda em inglês: os nomes dos lugares e dias da semana nos mapas. Entram numa próxima versão.

## O que você precisa

A imagem **original americana** do jogo, em um único arquivo `.bin`:

| | |
|---|---|
| Arquivo | `Legend of Mana (USA).bin` |
| Tamanho | 677.406.576 bytes |
| CRC32 | `5028946F` |

Um `.iso` de 2048 bytes por setor ou um `.bin` já modificado não servem.

## Como aplicar

### Arrastar e soltar (Windows)

1. Baixe o `.zip` da [release](https://github.com/alexcominoti/LoM/releases/latest) e extraia a pasta inteira.
2. Arraste o `.bin` original em cima de `aplicar_patch.bat`.
3. Quando aparecer "Pronto!", a pasta vai ter `Legend of Mana (PT-BR).bin` e `Legend of Mana (PT-BR).cue`.
4. Abra o `.cue` no emulador (DuckStation, ePSXe, Mednafen/Beetle PSX...). O `.bin` original não é alterado.

### Linha de comando / outros sistemas

```
xdelta3 -d -s "Legend of Mana (USA).bin" "Legend of Mana PT-BR v1.0.0.xdelta" "Legend of Mana (PT-BR).bin"
```

Depois crie `Legend of Mana (PT-BR).cue` com:

```
FILE "Legend of Mana (PT-BR).bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
```

Também dá para usar o [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher) ou o [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/).

### Como conferir

O `.bin` traduzido da v1.0.0 tem **671.938.176 bytes** e CRC32 **`8FA68B0B`**. Ele é menor que o original
porque a ferramenta de inserção remonta o CD de forma mais compacta. Se o xdelta acusar erro de checksum, a
imagem de origem não é a original americana.

### Atualizando de uma versão anterior

Aplique sempre o patch sobre o `.bin` **original americano**, nunca sobre um já traduzido. Os saves do cartão de
memória continuam valendo.

## Créditos

- **Tradução PT-BR:** sm0ke
- **Ferramentas de extração/inserção (PSX-LoM-Tools):** BahaBulle
- **Apoio:** Green Goblin (tradução espanhola)

Novidades da tradução: https://legendofmanaproject.blogspot.com/

## Aviso

Projeto de fã, gratuito e sem fins lucrativos, sem ligação com a Square Enix. Legend of Mana é propriedade da
Square Enix. Este repositório contém apenas o patch de tradução: não contém o jogo nem a imagem do CD, e o patch
não funciona sem a sua própria cópia original. Não distribua a imagem do jogo, nem a original nem a traduzida.

O `xdelta3.exe` incluído no pacote é o xdelta 3.0.6, de Joshua MacDonald, sob a licença GPL
([código-fonte](https://github.com/jmacd/xdelta)).
