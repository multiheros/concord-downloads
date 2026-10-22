# Concord

Downloads oficiais do Concord para Windows. Este repositório distribui os instaladores; o código do aplicativo é mantido separadamente.

## Baixar

**[Baixar Concord para Windows (64 bits)](https://github.com/multiheros/concord-downloads/releases/latest/download/Concord-Setup.exe)**

[Ver versões e novidades](https://github.com/multiheros/concord-downloads/releases/latest) · [Checksum SHA-256](https://github.com/multiheros/concord-downloads/releases/latest/download/SHA256SUMS.txt)

## Instalar e usar

1. Feche o Concord caso ele esteja aberto.
2. Baixe e execute **Concord-Setup.exe**. Para receber as correções nativas, reinstale mesmo que já tenha a versão anterior.
3. Abra o app e entre com sua conta. Em uma sala de voz, escolha uma janela ou tela e confirme em **Compartilhar**.

Para jogos, selecione a janela do jogo e o perfil **Jogos — até 1440p, 60 fps**. Prefira executar o jogo em janela sem bordas.

## Requisitos e disponibilidade

- Windows de 64 bits. A captura nativa de janela requer Windows 10 1903 ou posterior e GPU NVIDIA com NVENC H.264 e driver compatível com API 12.1.
- O instalador inclui FFmpeg mínimo: não é necessário instalar FFmpeg ou pacote de codecs separadamente.
- O áudio do sistema ainda não está disponível no compartilhamento nativo.
- A captura alternativa de janela recorta a região do monitor e pode mostrar o que estiver cobrindo essa janela.

## Diagnósticos técnicos

O app envia automaticamente dados técnicos de funcionamento: falhas por etapa, FPS de captura/encode/recepção/exibição e métricas de conexão disponíveis. Uma fila limitada tenta reenviar quando a conexão volta. Não coleta imagens, áudio, mensagens, títulos de janelas, caminhos, IP/SDP ou credenciais.

Em **Configurações da conta → Diagnósticos do aplicativo**, você pode consultar suas sessões, marcar uma travada, ativar detalhes por 10 minutos ou desativar a coleta. Acesso a outras contas é restrito à operação autorizada. As métricas de CPU/memória desta versão cobrem somente o processo nativo principal; GPU e processos auxiliares não são medidos.

## FFmpeg e licenças

FFmpeg 8.1.3 é distribuído como executável separado, sob LGPL 2.1 ou posterior, com nv-codec-headers 12.1.14.1 sob MIT. Licenças e avisos acompanham o app em `licenses/ffmpeg`. A compilação mínima não habilita GPL/nonfree; usa DLLs do Windows e o driver NVIDIA, sem exigir CUDA toolkit.

**[Fontes completas do FFmpeg e headers, receita, configuração e licenças](https://github.com/multiheros/concord-downloads/releases/download/release-2026-10-22.2/FFmpeg-source.zip)**. As notas de cada release identificam o pacote correspondente. É permitido modificar e substituir `ffmpeg.exe`, inclusive via `CONCORD_FFMPEG`, nos termos das respectivas licenças.

O Concord está em fase de piloto. As notas de cada versão informam novidades e limitações conhecidas.
