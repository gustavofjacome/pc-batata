# 🥔 PC Batata - Guia para Ressuscitar Máquinas Velhas

## 📑 Sumário
- [🔧 Ressuscite a sua batata com outro sistema operacional](#-ressuscite-a-sua-batata-com-outro-sistema-operacional)
- [🎮 Ressuscite sua batata como Central de Jogos Retrô](#-ressuscite-sua-batata-como-central-de-jogos-retrô)
- [🧪 Ressuscite sua batata como um Servidor](#-ressuscite-sua-batata-como-um-servidor)
- [📱 BÔNUS: Ressuscite Celulares Antigos como E-readers](#-ressuscite-celulares-antigos-como-e-readers)
- [♻️ E se nada disso funcionar?](#️-e-se-nada-disso-funcionar)
- [❓ FAQ - Perguntas Frequentes](#-faq---perguntas-frequentes)
- [👏 Agradecimentos](#-agradecimentos)

Ressuscitar batatas eletrônicas virou meu hobby. Se você tem um computador que parece ter vindo da Idade da Pedra, respira fundo. Com as dicas certas, ele pode virar uma máquina utilizável.

> ⚠️ Esse guia é voltado para quem quer performance, usabilidade e minimalismo. Se você quer usar Windows XP para "jogar GTA San Andreas", este não é o seu lugar.

---

## 🔧 Ressuscite a sua batata com outro sistema operacional 

### ✅ Por que Linux?
**Use Linux. Ponto final.**

Windows antigos não são mais seguros, nem otimizados, e sistemas modernos da Microsoft simplesmente não rodam bem em PC fraco. O Linux, com a distro certa, é o paraíso das máquinas velhas.

### 🔄 Qual distro escolher?

**Se você não sabe qual distro escolher ou não sabe o que está fazendo, recomendo fortemente que vá de Lubuntu!** 

O Lubuntu é baseado no Ubuntu, possivelmente a distro mais famosa de Linux, e por isso tem muito mais suporte da comunidade e tutoriais disponíveis. Além disso, a interface LXQt lembra bastante a do Windows, facilitando a adaptação para quem vem desse sistema. Na maioria das vezes, o Lubuntu servirá bem para computadores antigos. Caso não dê certo, teste outras opções da lista abaixo ou procure outras finalidades para a máquina.

### 📋 Distros Recomendadas

| Distro | RAM mínima | Interface | Observações |
|-------|------------|-----------|-------------|
| [Lubuntu](https://lubuntu.me/) | ~512MB | LXQt | Melhor escolha se você é iniciante. Estável e leve. Baseado no Ubuntu com muitos tutoriais e suporte disponível. |
| [Slax](https://www.slax.org/) | 128MB | Fluxbox | Incrivelmente leve e portátil. Não recomendado para dual boot. |
| [SliTaz](https://www.slitaz.org/) | 192MB | Openbox | Extremamente rápida, mas com menos pacotes disponíveis. |
| [TinyCore](http://tinycorelinux.net/) | 64MB | GUI ou CLI | Ultra minimalista. Requer paciência para configurar. |
| [NanoLinux](https://sourceforge.net/p/nanolinux/wiki/Home/) | ~16MB | FLTK | Para batatas que nem ligam mais direito. |
| [Void Linux](https://voidlinux.org/) | ~512MB | LXDE/Openbox/CLI | Rápida, independente e sem systemd. Boa pra quem já tem experiência. |
| [Artix Linux](https://artixlinux.org/) | ~512MB | dwm/Openbox | Arch-like sem systemd. Total liberdade com performance. |
| [Alpine Linux](https://alpinelinux.org/) | 128MB | CLI | Ultra leve, ideal para servidores e usos específicos. |

### 🌍 Aprenda mais

**Recomendação importante**:  
Antes de instalar algumas das distros ou de montar um servidor, recomendo fortemente que você procure estudar um pouco mais sobre o assunto. Há muitos recursos disponíveis no YouTube, além de discussões no Reddit, especialmente na comunidade **r/linux**. Para suporte em português, a comunidade **r/linuxbrasil** no Reddit é bastante ativa e pode te ajudar com dicas, problemas e orientações!
> ⚠️ E não esqueça de sempre **consultar a documentação oficial** da distro que escolher!
Ela costuma ter instruções detalhadas de instalação, requisitos mínimos, pacotes disponíveis, dicas de configuração e soluções para problemas comuns.

### 🌐 Navegadores Leves

| Navegador | Interface | Observações |
|-----------|-----------|-------------|
| [Brave](https://brave.com/) | GUI | Base Chromium, mas menos pesado |
| [Falkon](https://apps.kde.org/falkon/) | GUI | Leve e prático |
| [Palemoon](https://www.palemoon.org/) | GUI | Fork leve do Firefox |
| [Midori](https://www.midori-browser.org/) | GUI | Super leve, mas limitado |
| [Dillo](https://www.dillo.org/) | GUI | Quase sem suporte a JS |
| [surf](https://surf.suckless.org/) | GUI | Navegador suckless |
| [lynx](https://lynx.invisible-island.net/) / [w3m](http://w3m.sourceforge.net/) / [netsurf](https://www.netsurf-browser.org/) | Terminal | Navegação minimalista |


### 📚 Ferramentas Essenciais

#### 🎨 Editores de Texto
- GUI: [LeafPad](https://github.com/tarot231/leafpad), [FeatherPad](https://github.com/tsujan/FeatherPad)
- CLI: `nano`, `vim`, `micro`

#### 👨‍💻 Desenvolvimento
- Terminal: [NeoVim](https://neovim.io), [Helix](https://helix-editor.com/)
- GUI: [VSCodium](https://vscodium.com/), [Geany](https://www.geany.org/), [Lapce](https://lapce.dev/)

#### 🎥 Reprodutores de Mídia
- Vídeo: `mpv`
- Áudio: `mpv` ou `cmus`
- YouTube: `yt-dlp` + `mpv`

#### 🎬 Edição de Vídeo
- Terminal: `ffmpeg`

#### 📂 Leitura de Documentos
- PDF: `zathura`, `xpdf`, `qpdfview`
- Markdown: `glow`, `mdless`, `retext`
- Office:
  - `.doc` / `.docx`: `abiword`
  - `.ppt` / `.pptx`: `impressive`, `libreoffice --impress` (mais pesado)
  - `.xls` / `.xlsx`: `gnumeric`
  - `.odt`, `.odp`: `libreoffice` (usar só se tiver RAM suficiente)
- `.mobi` / `.epub`: `fbreader`, `calibre` (modo leve), `foliate`
- `.cdr` (CorelDraw): `inkscape` (suporte parcial), `libcdr` para conversões

### 🎮 Jogos na Batata

#### Steam? Sim, dá!
Instale o cliente Steam com `Proton` para rodar jogos do Windows.

#### Emuladores e Alternativas:
- `DOSBox` – para jogos MS-DOS
- `Wine` – roda jogos e programas Windows leves
- `bsdgames` – coleção de joguinhos em terminal

> Para instalar esses pacotes, use o gerenciador de pacotes da sua distribuição. 
> ***No Lubuntu e derivados do Ubuntu:*** `sudo apt install nome-do-pacote`
> ***No Arch/Artix:*** `sudo pacman -S nome-do-pacote`
> ***No Void Linux:*** `sudo xbps-install nome-do-pacote`
> ***No Alpine:*** `sudo apk add nome-do-pacote`

#### 🎮 Jogos de Terminal:
- `nethack`
- `moon-buggy`
- `greed`
- `cataclysm-dda`
- `crawl`

### 🛠 Linguagens de Programação Minimalistas

| Linguagem | Observações |
|----------|-------------|
| C | Rápida, nativa no Linux |
| Lua | Pequena e poderosa |
| Awk | Para automação de textos |
| ShellScript | Já vem no Linux |
| Forth | Ultra leve |
| V | Moderna, leve e compilada |
| Wren, Squirrel, Rebol, Potion | Alternativas pequenas e interessantes |
| GnuCOBOL | Porque não? 😄 |

**Evite:** Python, Java, C#, Node.js – são pesados demais pra máquinas antigas.

### ⚙️ Dicas de Otimização (para diversas distros)

- Desabilite serviços desnecessários:
  - No systemd (Ubuntu/Lubuntu/Debian): `systemctl disable nome-do-serviço`
  - No runit (Void/Artix): `sudo rm /var/service/nome-do-serviço`
  - No OpenRC (Alpine/Gentoo): `rc-update del nome-do-serviço`

- Use `zram` para compressão de RAM (disponível em quase todas distros)

- Use um compositor leve ou nenhum (ex: desative `picom` ou `compton`)

- Edite o GRUB para otimizar boot (se sua distro usar GRUB):
  Adicione `quiet mitigations=off` às opções de boot e atualize o GRUB

### 🌐 Plataformas de Streaming Remoto

- **[Nware](https://www.playnware.com/)** – Cloud gaming direto no navegador
- **[Steam Link](https://store.steampowered.com/steamlink)** – Espelha seu PC gamer em outro dispositivo
- **[Moonlight](https://moonlight-stream.org/)** – Baseado no NVIDIA GameStream, funciona até em Raspberry Pi

Requer conexão boa

### 🖨️ Impressoras e Periféricos Antigos

- Use o **CUPS** (`localhost:631`) para configurar impressoras via web
- Impressoras antigas (LPT/USB 1.1): verifique drivers no `gutenprint`
- Utilitários: `escputil`, `hp-setup`, `brother-driver-*`
- Scanners: `sane`, `xsane`, `simple-scan`

> Para instalar o CUPS e ferramentas relacionadas, use o gerenciador de pacotes da sua distribuição.
> Por exemplo, no Lubuntu ou derivados Ubuntu: `sudo apt install cups gutenprint simple-scan`

- Periféricos seriais (porta COM/ttyS): `minicom`, `picocom`, `screen`

[↑ Voltar ao sumário](#-sumário)

---

## 🎮 Ressuscite sua batata como Central de Jogos Retrô

Sim, dá pra jogar na batata! Se você tem um PC antigo e quer reviver clássicos do Super Nintendo, Mega Drive, PlayStation 1 (e até Dreamcast e PSP, dependendo do hardware), o **Batocera** é uma das melhores opções.

### 🎲 O que é Batocera?

Batocera.linux é um sistema operacional focado em **emulação e retro gaming**. Ele vem pronto pra usar — basta gravar em um pendrive ou HD e dar boot. Com ele, você pode jogar direto com joystick, teclado ou controle USB/Bluetooth.

> ⚠️ **Importante:** Ao instalar o Batocera, o computador se tornará uma central de jogos. Você não poderá usá-lo como um sistema operacional tradicional (como navegar na internet ou editar documentos). Isso, porém, **melhora muito o desempenho**, já que a máquina será totalmente dedicada aos jogos.

### ✅ Vantagens

- Interface amigável (estilo console)
- Suporte a dezenas de consoles e arcades
- Atualizações frequentes
- Plugins, filtros e shaders retrô
- Fácil de configurar e customizar
- Suporte a redes SMB para transferir jogos via Wi-Fi/LAN

### 💾 Requisitos mínimos

| Componente        | Mínimo Recomendado                  |
|-------------------|--------------------------------------|
| RAM               | 2GB (4GB para melhor desempenho)     |
| Armazenamento     | 16GB livre (mínimo), 32GB ou mais ideal |
| CPU               | Dual-Core (Pentium, Athlon ou superior) |
| GPU integrada     | Intel HD Graphics ou similar         |

> 📌 Em PCs com 2GB de RAM e processadores antigos (ex: Core2Duo, AMD Turion), o sistema roda bem consoles clássicos (SNES, Mega Drive, PS1).  
> Para consoles mais exigentes como **PS2, GameCube ou Wii**, é necessário um processador mais moderno (i3/i5, Ryzen) e no mínimo 4GB de RAM.  
> Emuladores de **PS3 e Xbox** exigem hardware muito potente — geralmente inviável em PCs antigos.

### 🚀 Como instalar?

Assista ao vídeo tutorial completo (em português):  
🎥 [Transforme um PC velho em um console retrô com Batocera](https://youtu.be/bBjoMQtn-nE?si=96Gfg6qLwW9VHY29)

Ou siga o passo a passo básico:

1. Baixe a imagem do Batocera: [batocera.org/download](https://batocera.org/download)
2. Use o [Balena Etcher](https://etcher.io/) para gravar a imagem em um pendrive ou HD externo
3. Dê boot pelo dispositivo gravado
4. Plugue um controle e explore!
5. Para adicionar jogos, conecte em um PC ou rede local e jogue as ROMs nas pastas correspondentes

> 🔍 **Observação importante:** o Batocera **não vem com jogos**. Você precisará **baixar as ROMs por conta própria**. Verifique sempre a legalidade e direitos autorais dos jogos que você deseja usar.

### 🎮 Dicas de uso e melhorias

- Utilize **pendrives/HDs rápidos** (USB 3.0, se possível)
- Configure **saves automáticos**, shaders e overlays retrô
- Plugue um controle USB ou Bluetooth compatível (PS3, PS4, Xbox, etc)
- Personalize com **temas e trilhas sonoras retrô**
- Use **resoluções baixas (720p)** para melhorar o desempenho em hardwares mais antigos
- Conecte a uma TV via **cabo HDMI** para imersão total
- Configure o **Wi-Fi ou rede cabeada** para transferir jogos pela rede local

### 🛠️ Melhorias recomendadas para a Central de Jogos

- Trocar HD mecânico por SSD (mesmo usado, faz diferença)
- Aumentar a RAM para 4GB ou mais
- Usar um **no-break ou filtro de linha** para proteger a máquina
- Ter um **controle USB** melhora MUITO a experiência
- Aproveitar **caixas de som antigas ou caixas Bluetooth**
- Usar um **cooler externo ou base refrigerada** se for notebook antigo

[↑ Voltar ao sumário](#-sumário)

---

## 🧪 Ressuscite sua batata como um Servidor!

Antes de desistir da sua máquina velha...
Ela pode não abrir 10 abas no navegador... mas talvez possa virar um **servidor pessoal**!

### 📺 Tutorial em vídeo

Para um passo a passo prático, confira este vídeo que ensina a transformar qualquer PC em um servidor:

[Transformei meu Notebook ANTIGO em um Servidor PROXMOX](https://www.youtube.com/watch?v=Dpj0RU6tvk4)

### 🏗️ Passo a passo básico para montar seu servidor

1. **Escolha uma distribuição leve e estável**:
   - `Debian Netinstall`: clássico, robusto, excelente para servidores.
   - `Alpine Linux`: absurdamente leve (~50MB), ideal para quem já tem alguma experiência.
   - `Void Linux`: leve, rápido, sem systemd.
   - `Devuan`: para quem quer algo estável como Debian mas sem systemd.
   - `Arch Linux`: não recomendado pra iniciantes, mas dá controle total se bem configurado.
   - `Ubuntu Server`: se você quer algo mais conhecido, mas cuidado com o peso.

2. **Instale sem interface gráfica (headless)**:
   - Isso economiza muita RAM e CPU.
   - Tudo será feito via terminal.

3. **Configure rede e acesso remoto**:
   - Ative e teste o `ssh` para acessar via outro computador.
   - Coloque IP fixo se for usar em rede local com frequência.

4. **Instale só o que precisa**:
   - Servidores simples rodam com menos de 256MB de RAM, se bem otimizados.
   - Use `htop`, `ncdu` e os comandos do seu gerenciador de serviços para monitorar recursos.

### 💡 Ideias de servidores que rodam em batatas

| Tipo de Servidor | Software Recomendado | Observações |
|------------------|----------------------|-------------|
| **Web estático** | `lighttpd`, `nginx`  | Ideal para hospedar sites simples em HTML |
| **Servidor de arquivos (NAS)** | `Samba`, `NFS` | Compartilhe arquivos com sua rede local |
| **Servidor SSH pessoal** | `openssh-server` | Acesse sua batata remotamente para estudos ou dev |
| **Servidor de mídia** | `MiniDLNA`, `MPD`  | Stream local de áudio ou vídeo leve |
| **Servidor Git pessoal** | `git`, `gitea`, `cgit` | Tenha seu próprio GitHub local (leve com `cgit`) |
| **Servidor VPN** | `WireGuard`, `OpenVPN` | Crie uma rede privada com acesso seguro |
| **Servidor DNS local** | `dnsmasq`, `bind` | Gerencie nomes na sua rede, útil pra LAN parties ou labs |
| **Servidor de monitoramento** | `netdata`, `monit` | Veja como sua batata sofre em tempo real 😅 |

### ⚙️ Melhorias para seu servidor caseiro

- **Armazenamento adicional**: Adicione um HD maior ou SSD para mais espaço e desempenho.
- **Nobreak (UPS)**: Proteja contra quedas de energia e mantenha o servidor funcionando.
- **Refrigeração adequada**: Garanta uma boa ventilação para evitar superaquecimento.
- **Backup regular**: Utilize ferramentas como `rsync` ou `borg` para backups automáticos.
- **Segurança**: Mantenha o sistema atualizado e configure firewalls para proteção.

### ☑️ Dicas para Servidor Leve

- Use distros mínimas e evite instalar "metapacotes" cheios de dependências.
- Monte seu sistema com `base`, `openssh`, `htop`, `nano/vim`, `ncdu` e o que mais for **essencial**.
- Use SSD ou pendrive rápido, se possível.
- Mantenha-o conectado via cabo (Ethernet) para melhor desempenho.
- Desabilite serviços desnecessários com o gerenciador de serviços da sua distro.

### 🔥 Quer brincar com containers?

Até Docker pode rodar em batata com 2GB de RAM! Ou experimente:
- `podman` – mais leve e seguro.
- `lxc` – estilo máquina virtual super leve.
- `systemd-nspawn` – bom pra isolar ambientes em distros com systemd.


[↑ Voltar ao sumário](#-sumário)

---

## 📱 Ressuscite Celulares Antigos como E-readers

Tem um Android velho esquecido na gaveta? Dá para transformá-lo em um **e-reader** e dar nova vida a ele!

### 🔍 Por que fazer isso?

- Aproveitar telas que já existem ao invés de comprar um Kindle
- Salvar um aparelho do lixo eletrônico
- Ter um e-reader personalizado com muito mais opções que os convencionais
- Reutilizar sem gastar quase nada

### 📋 Requisitos Mínimos

| Item | Recomendação |
|------|--------------|
| Android | 4.4+ (KitKat ou superior) |
| Memória RAM | 1GB ou mais |
| Espaço interno | Pelo menos 500MB livre |
| Bateria | Ainda funcional (mesmo com autonomia reduzida) |
| Tela | Intacta, com no mínimo 4 polegadas |

### 🛠️ KOReader: A melhor opção para leitura em Android antigo

O [KOReader](https://koreader.rocks/) é um aplicativo open-source especializado em leitura, com foco em performance e personalização. Ele é **muito mais leve** que apps como Kindle ou Google Books e oferece várias opções avançadas.

### 📱 Como instalar e configurar

Assista ao tutorial completo para orientação passo-a-passo:  
🎥 [Como transformar um celular Android antigo em e-reader](https://youtu.be/p2AnbPfqYpQ?si=CadMHOH0TcGXK8gC)

Ou siga este guia rápido:

1. **Prepare o celular**:
   * Faça backup dos dados importantes
   * Realize uma restauração de fábrica para limpar o sistema
   * Desative atualizações automáticas e notificações desnecessárias

2. **Instalação minimalista**:
   * Não faça login em contas Google (pule esta etapa na configuração)
   * Desative todos os serviços Google desnecessários
   * Instale apenas o essencial: F-Droid (loja de apps open source)
   * Pelo F-Droid, instale o KOReader
   * Ou baixe o `.apk` pela página oficial do github [KOReader](https://github.com/koreader/koreader/releases)

3. **Configurações recomendadas**:
   * Ative o modo avião ou desative dados móveis e Wi-Fi quando não estiver baixando livros
   * Configure o brilho no mínimo confortável
   * No KOReader, ative modo noturno ou tema escuro para economizar bateria

### 📚 Como transferir e organizar seus ebooks

* **Conecte via USB** e transfira diretamente os arquivos para a pasta `/KOReader` ou `/Books`
* **Conecte via Wi-Fi** usando o KOReader e seu recurso de transferência sem fio (temporariamente)
* **Use cartão SD** externo para expandir a capacidade de armazenamento

### 📖 Formatos suportados pelo KOReader

* `.epub` (o melhor formato para leitura)
* `.mobi`, `.azw3` (formatos Kindle)
* `.pdf` (com ferramentas de recorte e reformatação inteligente)
* `.djvu`, `.cbz`, `.cbr` (quadrinhos e documentos digitalizados)
* `.txt`, `.md` (textos simples e markdown)

### ⚙️ Dicas para otimizar a experiência

* **Desative sincronização automática** e outras funções em segundo plano
* **Active o "Don't keep activities"** nas opções de desenvolvedor
* **Instale apenas o KOReader** e talvez um gerenciador de arquivos leve como o `Simple File Manager`
* **Use modo leitura** com fundo bege/cinza ao invés de branco puro (consome menos bateria)
* **Configure gestos** para navegar sem usar os botões do celular
* **Ative o modo "E-ink"** se seu celular tiver tela AMOLED para economizar bateria

### 🧰 Acessórios úteis para seu novo e-reader

* **Capa stand** para deixar em pé ao ler em mesa
* **Power bank** para estender a autonomia
* **Película fosca** ("matte") para reduzir reflexos e simular textura de e-ink
* **Suporte de cama/mesa** para leitura sem segurar o aparelho


[↑ Voltar ao sumário](#-sumário)

---

## ♻️ E se nada disso funcionar?

Se mesmo com todas as dicas, distros leves, tunagens e reusos criativos, **seu pc realmente é uma batata... Mas ainda tem uma última missão nobre pra ela.**

Não descarte seu computador antigo ou peças eletrônicas no lixo comum. Isso polui o meio ambiente e pode conter metais pesados tóxicos.

🛑 **Nem pense em jogar no lixo doméstico.**  

### ✅ Descarte corretamente

Acesse o site da **ABREE (Associação Brasileira de Reciclagem de Eletroeletrônicos e Eletrodomésticos)** e procure um ponto de coleta próximo da sua casa:

🌐 [https://abree.org.br/pontos-de-recebimento](https://abree.org.br/pontos-de-recebimento)

No site, basta colocar o seu endereço e o sistema irá mostrar os pontos mais próximos para o **descarte consciente de eletrônicos.**


> Mesmo que sua batata não reviva, ela ainda pode renascer em outras formas. 🌍💻

[↑ Voltar ao sumário](#-sumário)

---

## ❓ FAQ - Perguntas Frequentes

**"Linux é difícil."**  
> Você já tentou? O terminal não morde. Dê uma chance.

**"Não consigo sair do Vim."**  
> Pressione `ESC`, digite `:q!` e pressione `Enter`.  
> Quer aprender Vim? Digite: `vimtutor pt`

**"Vale a pena ressuscitar?"**  
> Muito! Dá uma sensação gratificante ver a máquina funcionando suave. E se não for pra você, doe.

**"VLC é melhor?"**  
> É bom, mas pesado. Prefira o `mpv`.

**"Posso melhorar o hardware?"**  
> Sim! SSD + RAM extra fazem milagre. OLX, Facebook Marketplace, e grupos de Telegram têm peças baratas.

**"Consigo assistir YouTube em batata?"**  
> Sim, com o `mpv` via terminal ou usando o `yt-dlp`. Navegadores tradicionais engasgam.


**"Tem como usar o WhatsApp?"**  
> Sim, acesse [Whatsapp Web](https://web.whatsapp.com).


**"Qual interface gráfica consome menos?"**  
> `Openbox`, `i3`, `Fluxbox`, `XFCE` e `LXQt` são campeãs de leveza. Evite `GNOME` e `KDE` em PCs fracos.

**"Como economizar memória RAM?"**  
> Desative serviços desnecessários, use `zram`, evite navegador pesado, e rode tudo que puder no terminal.

**"Preciso mesmo usar o terminal?"**  
> Não, mas ele economiza recursos e faz milagres. Você vai se acostumar. É só questão de prática.


**"Tem como deixar com aparência moderna?"**  
> Sim! Temas `gtk`, ícones bonitos, `picom` com transparência, papéis de parede estilosos. Dá pra deixar chique e leve.

**"E se eu quebrar o sistema?"**  
> Parabéns, você está aprendendo! Formatar é rápido. Faça backup dos seus dotfiles e siga em frente. Errar faz parte.

[↑ Voltar ao sumário](#-sumário)

---

## 👏 Agradecimentos

Este guia foi inspirado e construído com base em conteúdos da comunidade de software livre e de entusiastas da tecnologia. Gratidão a todos que compartilham conhecimento.

#### 📚 Créditos especiais:

- 🔗 **[pc-carroça](https://github.com/terremoth/pc-carroca)**  
  Repositório que serviu de base e inspiração para várias seções deste guia.

&nbsp; 
- 🎥 **[Diolinux](https://www.diolinux.com.br/)**  
  Canal/blog referência em Linux e open source no Brasil. Alguns tutoriais linkados aqui foram produzidos por eles.

🙌 E a todos que compartilham conhecimento livremente na internet

*Feito para ajudar quem quer dar um novo propósito a computadores e celulares antigos* 



