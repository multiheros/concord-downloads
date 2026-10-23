# Concord

Downloads oficiais para Windows. Este repositório distribui instaladores; o código do aplicativo é mantido separadamente.

## Baixar

**[Baixar Concord v0.1.7 para Windows (64 bits)](https://github.com/multiheros/concord-downloads/releases/download/v0.1.7/Concord-0.1.7-Setup.exe)**

[Versões e novidades](https://github.com/multiheros/concord-downloads/releases/latest) · [SHA-256](https://github.com/multiheros/concord-downloads/releases/latest/download/SHA256SUMS.txt)

## Instalar e usar

1. Feche o Concord caso esteja aberto.
2. Execute **Concord-0.1.7-Setup.exe** e abra o app. Confira **Concord v0.1.7** na barra do aplicativo ou no menu da conta.
3. Entre em um canal de voz e escolha explicitamente a janela ou monitor que deseja compartilhar.

O pacote inclui **FFmpeg e instalador offline do WebView2**, comprimidos em um único instalador de aproximadamente 220 MiB. O WebView2 é instalado silenciosamente quando necessário. Não é preciso instalar pacote de codecs, Visual C++ Redistributable, Windows SDK ou CUDA toolkit separadamente. O uso do Concord continua exigindo conexão com o servidor.

## Atualizações pelo app

A partir da **v0.1.7**, o Concord consulta atualizações ao abrir e oferece download com progresso e o botão **Reiniciar e atualizar**. A instalação é bloqueada durante chamadas e transmissões. Pacotes e versões são verificados por assinatura digital antes de instalar.

Instale esta versão manualmente uma vez para ativar o recurso. As próximas atualizações chegam pelo próprio app, com pacote de aproximadamente **12 MiB**, sem baixar novamente o instalador offline do WebView2. O instalador completo de cerca de 220 MiB continua disponível para primeira instalação e recuperação. Os arquivos vêm deste GitHub; a VPS não hospeda os instaladores.

## Compartilhamento

- Se a captura da janela falhar, o app informa o motivo e encerra a tentativa. **Não troca automaticamente para monitor ou recorte de monitor.** Motores antigos que ainda trocam a fonte precisam ser atualizados antes de iniciar uma janela pela interface nova.
- A grade mostra duas transmissões por linha e usa qualidade econômica. Ao ampliar/tela cheia/PiP, a escolhida recebe máxima e as outras telas/áudios compartilhados pausam; retornar restaura a grade. Os microfones da chamada continuam ativos.
- A faixa auxiliar nativa tem até 720p, 30 fps e teto nominal de 2,5 Mbps. Quem transmite precisa instalar a nova versão e reiniciar sua transmissão para fornecê-la. Atualizar somente quem assiste não cria essa faixa no publicador antigo. Vídeos fora da área visível são pausados.
- Para jogos, prefira janela sem bordas. O perfil de jogos oferece até 1440p60, dependendo de máquina, cena e conexão.
- O áudio do sistema ainda não está disponível no compartilhamento nativo.

## Requisitos

Windows 10 1903 (build 18362) ou posterior; GPU NVIDIA com NVENC H.264 e driver compatível com API 12.1 para o modo nativo. WGC é componente do próprio Windows; o driver da GPU continua sendo instalado pelo fabricante. O instalador verifica o build mínimo e o app informa falhas de suporte/driver.

## Diagnósticos técnicos

O app identifica separadamente a versão da interface e a versão instalada do desktop, e envia dados técnicos de funcionamento: falhas por etapa, FPS de captura/encode/recepção/exibição e métricas de conexão disponíveis. A fila limitada tenta reenviar após queda da conexão. Não coleta imagens, áudio, mensagens, títulos de janelas, caminhos, IP/SDP ou credenciais.

Em **Configurações da conta → Diagnósticos do aplicativo**, você pode consultar suas sessões, marcar uma travada, ativar detalhes por 10 minutos ou desativar a coleta. Outras contas são acessíveis somente à operação autorizada. CPU/memória desta versão cobrem o processo nativo principal; GPU e processos auxiliares não são medidos.

## FFmpeg e licenças

FFmpeg 8.1.3 é executável separado sob LGPL 2.1 ou posterior; nv-codec-headers 12.1.14.1 sob MIT. A compilação mínima não habilita GPL/nonfree. Licenças e manifesto acompanham o app em `licenses/ffmpeg`.

**[Fontes completas do FFmpeg e headers, receita, configuração e licenças correspondentes](https://github.com/multiheros/concord-downloads/releases/latest/download/FFmpeg-source.zip)**. A receita contém integralmente os ajustes de escala D3D11 usados nesta versão. É permitido modificar e substituir `ffmpeg.exe`, inclusive via `CONCORD_FFMPEG`, nos termos das respectivas licenças.

O Concord está em piloto. Confira as notas de cada versão para validação e limitações conhecidas.
