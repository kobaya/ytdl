# ytdl

Aplicativo para baixar o **áudio** de vídeos, faixas e playlists do YouTube e do
YouTube Music. Cole o link e o arquivo é salvo no seu computador.

Este repositório serve apenas para **distribuir os arquivos prontos**. 

## Baixar

| Sistema | Arquivo | Tamanho |
| --- | --- | --- |
| **Windows** (10/11, 64 bits) | [ytdl-0.1.1-windows-amd64.zip](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-windows-amd64.zip) | 130 MB |
| Windows ARM (Snapdragon) | [ytdl-0.1.1-windows-arm64.zip](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-windows-arm64.zip) | 92 MB |
| **macOS** (chip Apple) | [ytdl-0.1.1-darwin-arm64.tar.gz](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-darwin-arm64.tar.gz) | 58 MB |
| macOS (Intel) | [ytdl-0.1.1-darwin-amd64.tar.gz](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-darwin-amd64.tar.gz) | 68 MB |
| **Linux** | [ytdl-0.1.1-linux-amd64.tar.gz](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-linux-amd64.tar.gz) | 137 MB |
| Linux ARM (Raspberry Pi) | [ytdl-0.1.1-linux-arm64.tar.gz](https://github.com/kobaya/ytdl/releases/download/v0.1.1/ytdl-0.1.1-linux-arm64.tar.gz) | 123 MB |

Se estiver em dúvida, quase todo PC com Windows é o **amd64** (mesmo que o
processador seja AMD ou Intel).

## Como usar

1. Baixe o arquivo do seu sistema e descompacte em qualquer pasta.
2. Execute o programa:
   - Windows: `ytdl.exe`
   - macOS e Linux: `./ytdl`
3. A página abre sozinha no navegador. Cole o link e clique em **Baixar**.

Mantenha a janela do programa aberta durante o download. Para encerrar, feche a
janela.

Os áudios ficam na pasta `data/downloads`, criada ao lado do programa.

## Formatos

O formato é escolhido na própria tela: MP3, M4A, OPUS, FLAC, WAV, ou o áudio
original sem conversão. A capa e os metadados (título, artista) são embutidos
automaticamente.

## Perguntas frequentes

**Preciso instalar alguma coisa?**
Não. O programa já vem com tudo que precisa, e foi feito em Go justamente para
não exigir runtime instalado.

**Por que o arquivo é grande?**
A maior parte é o `ffmpeg`, que faz a conversão de áudio. Ele vai junto para
você não precisar instalar nada.

**Na primeira execução ele baixou algo. O que foi?**
O `yt-dlp`, o componente que conversa com o YouTube. Ele é baixado e mantido
atualizado automaticamente, porque o YouTube muda com frequência e essa parte
precisa acompanhar. Precisa de internet na primeira vez.

**Alguns vídeos falham com erro de verificação.**
Se aparecer "Sign in to confirm you're not a bot", escolha o navegador onde você
já está logado no YouTube, na opção de cookies do aplicativo. Os cookies ficam
apenas na sua máquina.

**Nada foi enviado para fora do meu computador?**
Não. Todo o trabalho acontece na sua máquina. O único acesso externo é o
download do `yt-dlp` e o próprio vídeo que você pediu.

**Não abre no macOS.**
Se aparecer aviso de desenvolvedor não identificado, clique com o botão direito
no programa e escolha **Abrir**. Em Linux, se necessário: `chmod +x ytdl`.

## Verificação de integridade

Cada pacote tem o tamanho listado acima. Se o download vier corrompido, o
descompactador vai acusar — baixe novamente.

## Componentes de terceiros

O aplicativo distribui e utiliza componentes de terceiros, que mantêm suas
próprias licenças:

- **[FFmpeg](https://ffmpeg.org/)** — compilado com a opção `--enable-gpl`,
  portanto sob **GPL v3**. Os binários são executados como programas separados,
  acompanhados deste aplicativo. O código-fonte correspondente está disponível
  em [github.com/yt-dlp/FFmpeg-Builds](https://github.com/yt-dlp/FFmpeg-Builds)
  (Linux e Windows) e em [ffmpeg.martin-riedl.de](https://ffmpeg.martin-riedl.de/)
  (macOS).
- **[yt-dlp](https://github.com/yt-dlp/yt-dlp)** — domínio público (Unlicense).
  Baixado no primeiro uso.

As marcas YouTube e YouTube Music pertencem ao Google. Este aplicativo não tem
vínculo com o Google e destina-se a uso pessoal; respeite os termos de serviço e
os direitos autorais do conteúdo que você baixar.
