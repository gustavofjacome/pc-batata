# pc-antigo 

**Guia para maximizar o desempenho de computadores antigos com Linux**

Este repositório é um esforço para consolidar conhecimentos e práticas que permitem revitalizar hardware antigo através do uso inteligente de distribuições Linux leves, otimizações de sistema e uma seleção de software leves. O objetivo é transformar máquinas com poucos recursos em sistemas funcionais, ágeis e úteis para diversas tarefas.

---

## 📑 Sumário

* [🎯 Objetivos Principais](#-objetivos-principais)
* [🖥️ Hardware Alvo Típico](#️-hardware-alvo-típico)
* [🚀 Roteiro Sugerido para Otimização](#-roteiro-sugerido-para-otimização)
* [⚠️ Alerta para Iniciantes](#️-alerta-para-iniciantes)
* [🐧 Escolhendo a Distribuição Linux Ideal](#-escolhendo-a-distribuição-linux-ideal)
    * [✅ Por que Linux para Hardware Antigo?](#-por-que-linux-para-hardware-antigo)
    * [🤔 Critérios para Escolher uma Distro](#-critérios-para-escolher-uma-distro)
    * [📋 Distros Recomendadas: Análise Detalhada](#-distros-recomendadas-análise-detalhada)
        * [Lubuntu](#lubuntu)
        * [Xubuntu](#xubuntu)
        * [Linux Mint (XFCE/MATE)](#linux-mint-xfcemate)
        * [AntiX](#antix)
        * [Bodhi Linux](#bodhi-linux)
        * [Puppy Linux](#puppy-linux)
        * [SliTaz](#slitaz)
        * [Q4OS](#q4os)
        * [Alpine Linux](#alpine-linux)
        * [Void Linux](#void-linux)
        * [Debian (Netinstall com DE Leve)](#debian-netinstall-com-de-leve)
        * [Outras Menções Notáveis](#outras-menções-notáveis)
* [⚙️ Otimizações Essenciais de Sistema](#️-otimizações-essenciais-de-sistema)
    * [🧬 Otimizando Parâmetros de Boot do Kernel (GRUB)](#-otimizando-parâmetros-de-boot-do-kernel-grub)
        * [Mitigações de Segurança vs. Performance (Aviso Importante)](#mitigações-de-segurança-vs-performance-aviso-importante)
    * [🛠️ Gerenciamento de Serviços](#️-gerenciamento-de-serviços)
        * [Identificando Serviços](#identificando-serviços)
        * [Desabilitando Serviços (Systemd, Runit, OpenRC)](#desabilitando-serviços-systemd-runit-openrc)
        * [Exemplos de Serviços Comumente Desabilitáveis](#exemplos-de-serviços-comumente-desabilitáveis)
    * [🗂️ Otimização do Sistema de Arquivos](#️-otimização-do-sistema-de-arquivos)
        * [Escolha do Filesystem (Ext4, XFS, F2FS)](#escolha-do-filesystem-ext4-xfs-f2fs)
        * [Opções de Montagem (noatime, nodiratime)](#opções-de-montagem-noatime-nodiratime)
    * [💾 Swap e Gerenciamento de Memória](#-swap-e-gerenciamento-de-memória)
        * [Ajustando Swappiness](#ajustando-swappiness)
        * [Configurando ZRAM](#configurando-zram)
        * [Swap em Partição vs. Arquivo Swap](#swap-em-partição-vs-arquivo-swap)
    * [🖼️ Ambientes Gráficos (DE) e Gerenciadores de Janelas (WM) Leves](#️-ambientes-gráficos-de-e-gerenciadores-de-janelas-wm-leves)
        * [Recomendações (LXQt, XFCE, Openbox, i3wm, etc.)](#recomendações-lxqt-xfce-openbox-i3wm-etc)
        * [Dicas para Minimizar o Consumo (Compositor, Temas)](#dicas-para-minimizar-o-consumo-compositor-temas)
    * [🚀 Aplicações ao Iniciar (Startup Applications)](#-aplicações-ao-iniciar-startup-applications)
    * [🧹 Limpeza do Sistema](#-limpeza-do-sistema)
* [🔧 Software Leve e Eficiente](#-software-leve-e-eficiente)
    * [🌐 Navegadores Web](#-navegadores-web)
    * [📝 Editores de Texto e IDEs](#-editores-de-texto-e-ides)
    * [🎬 Reprodutores de Mídia](#-reprodutores-de-mídia)
    * [📑 Visualizadores de Documentos (PDF, Office, etc.)](#-visualizadores-de-documentos-pdf-office-etc)
    * [⌨️ Ferramentas Essenciais de Linha de Comando](#️-ferramentas-essenciais-de-linha-de-comando)
    * [🖥️ Emuladores de Terminal Leves](#️-emuladores-de-terminal-leves)
    * [💻 (Opcional) Linguagens de Programação com Baixo Overhead](#-opcional-linguagens-de-programação-com-baixo-overhead)
* [🛠️ Casos de Uso Específicos para Hardware Antigo](#️-casos-de-uso-específicos-para-hardware-antigo)
    * [🎮 Transformando em uma Central de Jogos Retrô](#-transformando-em-uma-central-de-jogos-retrô)
        * [Batocera.linux](#batoceralinux)
        * [Outras Opções (Lakka, RetroArch)](#outras-opções-lakka-retroarch)
        * [Requisitos e Dicas](#requisitos-e-dicas)
    * [🖥️ Configurando um Servidor Doméstico Leve](#️-configurando-um-servidor-doméstico-leve)
        * [Ideias de Servidores (NAS, Web, Pi-hole, Gitea)](#ideias-de-servidores-nas-web-pi-hole-gitea)
        * [Recomendações de Distros Server (Debian Minima, Alpine)](#recomendações-de-distros-server-debian-minima-alpine)
        * [Dicas de Segurança e Manutenção](#dicas-de-segurança-e-manutenção)
    * [📱 Reutilizando Celulares e Tablets Android Antigos](#-reutilizando-celulares-e-tablets-android-antigos)
        * [E-reader com KOReader](#e-reader-com-koreader)
        * [Outros Usos (Monitor de Sistema, Câmera de Segurança Simples)](#outros-usos-monitor-de-sistema-câmera-de-segurança-simples)
* [💡 Dicas Avançadas](#-dicas-avançadas)
    * [Considerações sobre Hardware (SSD, RAM)](#considerações-sobre-hardware-ssd-ram)
    * [Streaming de Jogos (Nware, Steam Link, Moonlight)](#streaming-de-jogos-nware-steam-link-moonlight)
    * [Impressoras e Periféricos Antigos](#impressoras-e-periféricos-antigos)
* [♻️ Descarte Consciente de Hardware](#️-descarte-consciente-de-hardware)
* [❓ FAQ - Perguntas Frequentes](#-faq---perguntas-frequentes)
* [🤝 Como Contribuir](#-como-contribuir)
* [🙏 Agradecimentos e Inspiração](#-agradecimentos-e-inspiração)

---

## 🎯 Objetivos Principais
* **Performance:** Extrair o máximo de desempenho possível de hardware restrito, tornando a experiência de uso fluida e responsiva.

* **Usabilidade:** Garantir que sistemas antigos possam ser utilizados para tarefas cotidianas (navegação web leve, edição de texto, multimídia básica) e específicas (servidores caseiros, emulação de jogos retrô).

* **Minimalismo Consciente:** Promover o uso de software leve e eficiente, focando em funcionalidades essenciais e evitando o "bloatware" (excesso de software e recursos desnecessários).

* **Aprendizado:** Servir como um recurso educacional para usuários que desejam aprofundar seus conhecimentos em Linux, otimização de sistemas e funcionamento interno de um sistema operacional.

* **Sustentabilidade:** Incentivar o reaproveitamento de hardware, prolongando a vida útil de computadores antigos e contribuindo para a redução do lixo eletrônico.

[↑ Sumário](#-sumário)

---

## 🖥️ Hardware Alvo Típico
Este guia é especialmente útil para computadores com características como:

* **Processadores:** Single-core ou dual-core de gerações mais antigas (ex: Intel Pentium III/4/M, Celeron D/M, Core Solo/Duo, Core 2 Duo de baixa frequência; AMD K6/Athlon XP/Sempron/Turion, primeiras gerações de APUs C-Series e E-Series). Suporte a 32-bit (i386/i686) ou 64-bit (amd64/x86_64) inicial.

* **Memória RAM:** Entre 256MB e 2GB. Sistemas com 512MB a 1GB são o foco principal, mas dicas para menos de 512MB (com distros e WMs ultra-leves) e até 4GB (onde otimizações ainda são benéficas) são abordadas.

* **Armazenamento:** Discos Rígidos Mecânicos (HDD IDE/PATA ou SATA I/II) com baixas velocidades de rotação (5400rpm) e cache limitado. SSDs de primeira geração ou de baixo custo também podem se beneficiar.

* **Gráficos:** GPUs integradas antigas (Intel GMA, SiS, VIA, primeiras ATI/AMD Radeon, primeiras NVIDIA GeForce) com suporte limitado a aceleração 2D/3D moderna, ou que dependem de drivers genéricos como VESA.

* **Outros:** Placas-mãe com chipsets antigos, interfaces legadas (PS/2, portas seriais/paralelas), e ausência de recursos modernos como USB 3.0 ou Wi-Fi rápido.

[↑ Sumário](#-sumário)

---

## 🚀 Roteiro Sugerido para Otimização
1.  **Avalie seu Hardware:** Identifique as especificações exatas do seu computador (CPU, RAM, Disco, GPU). Isso ajudará a definir expectativas realistas e escolher as otimizações mais adequadas.
2.  **Backup (Opcional, mas Recomendado):** Se houver dados importantes no disco, faça um backup antes de instalar um novo sistema.
3.  **Escolha a Distro:** Consulte a seção [Escolhendo a Distribuição Linux Ideal](#-escolhendo-a-distribuição-linux-ideal). Para iniciantes, **Lubuntu** ou **Xubuntu** são bons pontos de partida. Para hardware *extremamente* limitado, **AntiX** ou **Bodhi Linux**.
4.  **Crie Mídia de Instalação:** Após baixar o arquivo ISO da distribuição Linux escolhida, você precisará gravá-lo em uma mídia para dar boot no computador antigo. As opções mais comuns são pendrives USB, mas CDs ou DVDs também podem ser usados se o hardware exigir (e você tiver um gravador).

    * **Ventoy (Recomendado pela facilidade e versatilidade):**
        * **O que é:** [Ventoy](https://www.ventoy.net/) é uma ferramenta de código aberto para criar pendrives USB bootáveis para arquivos ISO/WIM/IMG/VHD(x)/EFI. A grande vantagem é que você **não precisa formatar o pendrive repetidamente**. Você instala o Ventoy no pendrive uma vez e depois simplesmente copia quantos arquivos ISO desejar para dentro dele. Ao dar boot pelo pendrive com Ventoy, ele apresentará um menu com todas as ISOs que você copiou, permitindo escolher qual sistema iniciar.

        * **Como usar:**
            1.  Baixe o Ventoy do site oficial e execute o instalador para o seu sistema operacional (Windows ou Linux).

            2.  Instale o Ventoy no pendrive desejado (isso apagará o conteúdo do pendrive na primeira vez).

            3.  Após a instalação do Ventoy no pendrive, ele será montado como um disco normal. Simplesmente copie os arquivos `.iso` das distribuições Linux (ou outras imagens de boot) para dentro deste pendrive.

            4.  Configure o computador antigo para dar boot pela USB e selecione a ISO desejada no menu do Ventoy.

    * **Balena Etcher:**
        * **O que é:** [Balena Etcher](https://www.balena.io/etcher/) é uma ferramenta gráfica popular e fácil de usar, disponível para Windows, macOS e Linux. Ele guia você pelo processo de seleção da ISO e do pendrive, realizando a gravação de forma segura.

        * **Como usar:** Baixe, instale, selecione a ISO, selecione o pendrive e clique em "Flash!".

        * **Nota:** O Etcher formata o pendrive e grava uma única ISO por vez.

    * **Rufus:**
        * **O que é:** [Rufus](https://rufus.ie/) é uma ferramenta leve, rápida e muito popular para criar pendrives bootáveis no Windows. Oferece várias opções avançadas, como escolha de esquema de partição (MBR/GPT) e sistema de arquivos.

        * **Como usar:** Baixe o executável, selecione o pendrive, selecione a ISO e configure as opções conforme necessário antes de iniciar.

        * **Nota:** Assim como o Etcher, grava uma única ISO por vez.

    * **Comando `dd` (Linux/macOS - Avançado):**
        * **O que é:** Uma ferramenta de linha de comando poderosa para cópia e conversão de dados bit a bit. Pode ser usada para gravar ISOs em pendrives, mas é **perigosa se usada incorretamente**, pois um erro no nome do dispositivo de destino pode apagar o disco errado.

        * **Como usar (exemplo, use com extrema cautela):**
            1.  Identifique o dispositivo do pendrive (ex: `/dev/sdb`, `/dev/sdc` - NUNCA `/dev/sda` se este for seu disco principal) com comandos como `lsblk` ou `sudo fdisk -l`. Certifique-se de que o pendrive não está montado (`sudo umount /dev/sdb1` etc.).
            2.  Execute: `sudo dd bs=4M if=/caminho/para/sua/distro.iso of=/dev/sdX status=progress oflag=sync` (substitua `sdX` pelo dispositivo correto do pendrive).

        * **Nota:** Para usuários experientes que preferem a linha de comando.

    * **CD/DVD (se necessário):** Se o computador antigo não dá boot por USB ou você só tem um leitor de CD/DVD, será preciso usar um software de gravação de CD/DVD (como K3b no Linux, InfraRecorder no Windows, ou as ferramentas nativas do sistema) para "queimar" a ISO em um disco. Esta opção é mais lenta e menos flexível.

5.  **Instalação Limpa:** Instale a distribuição. Durante a instalação, se possível, opte por uma "instalação mínima" para evitar pacotes desnecessários. Considere o particionamento manual se tiver experiência.

6.  **Primeiros Passos Pós-Instalação:**
    * Atualize o sistema: `sudo apt update && sudo apt upgrade` (para distros baseadas em Debian/Ubuntu). Para outras famílias de distros, use o gerenciador de pacotes correspondente (ex: `sudo pacman -Syu` para Arch, `sudo dnf upgrade` para Fedora).
    * Instale drivers adicionais, se necessário (geralmente distros leves lidam bem com hardware antigo nativamente).

7.  **Aplique Otimizações Básicas:** Comece com as otimizações de sistema mais seguras e com maior impacto (veja [Otimizações Essenciais de Sistema](#️-otimizações-essenciais-de-sistema)), como ajustar o `swappiness` ou configurar `zram`.

8.  **Instale Software Leve:** Escolha aplicativos da seção [Software Leve e Eficiente](#-software-leve-e-eficiente) para suas necessidades.

9.  **Otimizações Avançadas (Com Cuidado!):** Se você se sentir confortável e entender os riscos, explore otimizações mais avançadas como parâmetros de kernel ou desabilitar serviços manualmente. Leia o [Alerta para Iniciantes](#️-alerta-para-iniciantes).

10. **Monitore e Ajuste:** Use ferramentas como `htop` ou `btop` para monitorar o uso de recursos e ajuste as configurações conforme necessário.

[↑ Sumário](#-sumário)

---

## ⚠️ Alerta para Iniciantes

Muitas otimizações listadas aqui, especialmente aquelas que envolvem alterações em arquivos de configuração do sistema, parâmetros de inicialização do kernel ou desativação manual de serviços, podem ter consequências inesperadas se não forem aplicadas corretamente, podendo levar a um sistema instável ou que não inicializa.

**Se você é iniciante no Linux ou não se sente seguro para realizar modificações profundas no sistema:**

1.  **Comece pelo básico:** A simples escolha de uma distribuição Linux leve (como Lubuntu ou Xubuntu) e de aplicativos leves já trará uma melhoria significativa de desempenho em hardware antigo.

2.  **Não aplique todas as otimizações de uma vez:** Se decidir prosseguir com otimizações mais avançadas, faça uma de cada vez e teste a estabilidade do sistema após cada alteração.

3.  **Pesquise e entenda:** Antes de aplicar qualquer comando ou configuração que não compreenda totalmente, pesquise sobre ele. Entenda o que ele faz e quais os possíveis impactos.

4.  **Backup:** Considere fazer backup de arquivos de configuração importantes antes de modificá-los.

Lembre-se: o objetivo é melhorar o desempenho e a usabilidade, não quebrar o sistema. Prossiga com cautela e curiosidade!

[↑ Sumário](#-sumário)

---

## 🐧 Escolhendo a Distribuição Linux Ideal

### ✅ Por que Linux para Hardware Antigo?

Sistemas operacionais Windows mais antigos, como XP ou 7, não recebem mais atualizações de segurança, tornando-os vulneráveis. Versões modernas do Windows são excessivamente pesadas para hardware legado. O macOS nunca foi uma opção para hardware genérico antigo.

O Linux brilha neste cenário por diversos motivos técnicos:

* **Kernel Modular e Leve:** O kernel Linux é altamente configurável. Muitas distribuições focadas em leveza já vêm com kernels otimizados para baixo consumo de recursos ou permitem fácil customização.

* **Variedade de Ambientes Gráficos (DEs) e Gerenciadores de Janelas (WMs):** Você não está preso a uma única interface. Existem DEs completos e leves (XFCE, LXQt, MATE) e WMs minimalistas (Openbox, Fluxbox, IceWM, i3wm, dwm) que consomem quantias irrisórias de RAM e CPU.

* **Gerenciamento Eficiente de Recursos:** O Linux geralmente possui um gerenciamento de memória e processos mais eficiente, especialmente quando configurado corretamente.

* **Segurança:** Mesmo distros leves recebem atualizações de segurança regulares, mantendo seu sistema protegido.

* **Comunidade e Código Aberto:** A natureza open-source permite que a comunidade audite, modifique e otimize o código. Há vasto suporte online e documentação.

* **Software Leve Disponível:** Existe um ecossistema rico de aplicativos leves e eficientes para todas as tarefas básicas.

* **Controle Total:** Usuários avançados podem "dissecar" o sistema, removendo tudo o que não é essencial e compilando software especificamente para seu hardware.

Em resumo, Linux oferece a flexibilidade e o controle necessários para adaptar o sistema operacional às limitações do hardware, em vez de forçar o hardware a rodar um sistema pesado.

### 🤔 Critérios para Escolher uma Distro

A escolha da "melhor" distro é subjetiva e depende de vários fatores:

* **Especificações do Hardware:** Principalmente RAM, CPU (arquitetura 32-bit ou 64-bit) e capacidade do disco.

* **Nível de Experiência do Usuário:** Iniciantes podem preferir distros com instaladores gráficos amigáveis e mais "prontas para uso", enquanto usuários experientes podem optar por instalações mínimas e maior controle.

* **Interface Gráfica Desejada:** Algumas distros vêm com DEs/WMs específicos. Verifique se a interface padrão agrada ou se é fácil instalar alternativas.

* **Base do Sistema:**
    * **Debian-based (ex: Ubuntu, Mint, AntiX):** Geralmente estáveis, com vastos repositórios de software (`.deb`, `apt`). Boas para iniciantes e servidores.

    * **Arch-based (ex: Manjaro, EndeavourOS, Artix):** Conhecidas por serem rolling-release (sempre atualizadas), com documentação excelente (Arch Wiki). Exigem um pouco mais de conhecimento para manter.

    * **Independentes (ex: Puppy, SliTaz, Void, Alpine):** Têm suas próprias filosofias, gerenciadores de pacotes e comunidades. Podem oferecer soluções únicas para leveza.

* **Suporte à Arquitetura:** Se seu PC é muito antigo (anterior a ~2007), ele pode ser 32-bit (i386, i686). Muitas distros populares estão descontinuando o suporte a 32-bit, então verifique isso. Distros como AntiX, Debian (com ressalvas e suporte limitado pela comunidade para portes 32-bit), e algumas versões do Puppy ainda são boas opções para 32-bit.

* **Comunidade e Documentação:** Uma comunidade ativa e boa documentação são cruciais para solucionar problemas.

* **Propósito do Computador:** Um desktop de uso geral terá necessidades diferentes de um servidor caseiro ou uma central de jogos retrô.

**Recomendação geral:** Se você está em dúvida, comece com uma distro popular e bem documentada que seja conhecida por sua leveza, como **Lubuntu** ou **Xubuntu**. Se o desempenho ainda não for satisfatório, você pode explorar opções mais minimalistas.

### 📋 Distros Recomendadas: Análise Detalhada

Aqui estão algumas das distribuições Linux mais recomendadas para hardware antigo, com uma breve análise técnica:

#### Lubuntu
* **Site Oficial:** [lubuntu.me](https://lubuntu.me/)
* **Base:** Ubuntu (Debian)
* **Ambiente Gráfico:** LXQt
* **RAM Mínima (Prática):** ~512MB para tarefas básicas, 1GB+ recomendado para uma experiência mais suave com navegação web moderna. Suporte oficial a 32-bit foi descontinuado após a versão 18.04 LTS.
* **Análise:** Uma das escolhas mais populares e sólidas para iniciantes que desejam leveza. LXQt é um ambiente de desktop que utiliza Qt, é funcional, visualmente agradável e consome poucos recursos. Beneficia-se da enorme base de pacotes e suporte da comunidade Ubuntu. É uma excelente porta de entrada antes de mergulhar em distros mais "radicais".
* **Ideal para:** Usuários vindos do Windows que buscam familiaridade, máquinas com 1GB+ de RAM, uso geral de desktop (64-bit).

#### Xubuntu
* **Site Oficial:** [xubuntu.org](https://xubuntu.org/)
* **Base:** Ubuntu (Debian)
* **Ambiente Gráfico:** XFCE
* **RAM Mínima (Prática):** ~512MB-1GB. XFCE é um pouco mais pesado que LXQt, mas ainda muito leve comparado a GNOME/KDE.
* **Análise:** Similar ao Lubuntu em termos de base e comunidade. XFCE é um DE clássico, altamente configurável, estável e com bom equilíbrio entre funcionalidades e consumo de recursos. Muitos o consideram mais polido e completo que LXQt, ao custo de um consumo de RAM ligeiramente maior.
* **Ideal para:** Usuários que buscam um desktop tradicional, personalizável e um pouco mais completo que Lubuntu, em máquinas com 1GB+ de RAM (64-bit).

#### Linux Mint (XFCE/MATE)
* **Site Oficial:** [linuxmint.com](https://linuxmint.com/)
* **Base:** Ubuntu (Debian)
* **Ambiente Gráfico:** XFCE ou MATE (fork do GNOME 2)
* **RAM Mínima (Prática):** ~1GB. MATE é similar ao XFCE em consumo.
* **Análise:** Conhecido por sua facilidade de uso e por vir "com tudo incluído" (codecs, drivers). As edições XFCE e MATE são significativamente mais leves que a edição principal (Cinnamon). Ótima experiência out-of-the-box.
* **Ideal para:** Iniciantes que querem uma transição suave, com um sistema que funciona bem "da caixa", em máquinas com pelo menos 1-2GB de RAM (64-bit).

#### AntiX
* **Site Oficial:** [antixlinux.com](https://antixlinux.com/)
* **Base:** Debian Stable (sem systemd - usa sysVinit ou runit por padrão)
* **Ambiente Gráfico:** IceWM, Fluxbox, JWM (extremamente leves)
* **RAM Mínima (Prática):** ~192-256MB para uma interface gráfica funcional. Roda até em máquinas com 128MB (modo CLI ou WMs muito básicos). Excelente suporte a 32-bit.
* **Análise:** Projetado especificamente para hardware antigo e muito antigo. É incrivelmente rápido e responsivo. A ausência de systemd é um grande atrativo para alguns usuários que buscam simplicidade ou discordam da filosofia do systemd. Vem com muitas ferramentas úteis e scripts para facilitar a configuração. A curva de aprendizado pode ser um pouco maior para quem está acostumado com systemd.
* **Ideal para:** Hardware *realmente* antigo (Pentium II/III, Celerons antigos), máquinas com pouquíssima RAM (abaixo de 512MB), usuários que preferem sistemas sem systemd, e necessitam de suporte 32-bit.

#### Bodhi Linux
* **Site Oficial:** [bodhilinux.com](https://bodhilinux.com/)
* **Base:** Ubuntu LTS
* **Ambiente Gráfico:** Moksha Desktop (um fork do Enlightenment E17, otimizado para ser leve)
* **RAM Mínima (Prática):** ~256-512MB. Oferece versões 32-bit e 64-bit.
* **Análise:** Oferece uma experiência visualmente atraente e única com o Moksha, que é surpreendentemente leve e configurável. É uma boa opção para quem quer algo diferente das interfaces tradicionais baseadas em GTK ou Qt. Mantém compatibilidade com repositórios Ubuntu.
* **Ideal para:** Usuários que buscam um desktop leve, mas com um visual distinto e moderno, em máquinas com 512MB+ de RAM, incluindo suporte a 32-bit.

#### Puppy Linux
* **Site Oficial:** [puppylinux.com](https://puppylinux-woof-ce.github.io/)
* **Base:** Independente (pode ser construído a partir de pacotes de outras distros como Ubuntu ou Slackware - "Woof-CE")
* **Ambiente Gráfico:** JWM por padrão, mas outros WMs leves são comuns.
* **RAM Mínima (Prática):** ~128-256MB. Muitas versões podem rodar inteiramente da RAM. Amplo suporte a 32-bit.
* **Análise:** Uma família de distribuições leves projetadas para serem rápidas, fáceis de usar e pequenas. Carrega o sistema operacional inteiro na memória RAM (se houver RAM suficiente), o que o torna incrivelmente rápido, mesmo em hardware com discos lentos. O sistema de arquivos em camadas (AUFS/OverlayFS) e o gerenciamento de "save files/folders" são únicos. Excelente para pendrives bootáveis e recuperação de sistemas.
* **Ideal para:** Hardware muito antigo, uso em modo "live" a partir de um pendrive, portabilidade, máquinas com HDs defeituosos ou muito lentos, e forte suporte a 32-bit.

#### SliTaz
* **Site Oficial:** [slitaz.org](https://www.slitaz.org/)
* **Base:** Independente
* **Ambiente Gráfico:** Openbox por padrão, com painel LXPanel.
* **RAM Mínima (Prática):** ~48MB para o modo "core" (CLI), ~128-192MB para Openbox. Suporte a 32-bit.
* **Análise:** Uma das menores distribuições Linux existentes em termos de tamanho de ISO (geralmente ~50MB). É incrivelmente leve e rápida. Possui seu próprio gerenciador de pacotes (TazPkg) e ferramentas de configuração. A seleção de pacotes nos repositórios pode ser mais limitada em comparação com distros maiores.
* **Ideal para:** Hardware extremamente limitado, entusiastas de minimalismo, uso embarcado ou como sistema de recuperação muito leve, com suporte 32-bit.

#### Q4OS
* **Site Oficial:** [q4os.org](https://q4os.org/)
* **Base:** Debian Stable
* **Ambiente Gráfico:** Trinity Desktop Environment (TDE - um fork do KDE 3.5) ou KDE Plasma (este último não recomendado para hardware muito antigo).
* **RAM Mínima (Prática):** ~256MB para TDE. Oferece versões 32-bit.
* **Análise:** Focado em estabilidade e na experiência clássica do desktop. O TDE é surpreendentemente leve e rápido, oferecendo um ambiente rico em recursos que remete ao KDE 3.5, mas com atualizações e melhorias. Ótima opção para quem gostava do KDE antigo e precisa de algo leve.
* **Ideal para:** Usuários que apreciam a estabilidade do Debian e a interface clássica do KDE3/Trinity, em máquinas com 512MB+ de RAM, com suporte 32-bit.

#### Alpine Linux
* **Site Oficial:** [alpinelinux.org](https://alpinelinux.org/)
* **Base:** Independente (usa musl libc e BusyBox em vez de glibc e coreutils GNU)
* **Ambiente Gráfico:** Nenhuma por padrão (CLI). Pode-se instalar XFCE, MATE, etc.
* **RAM Mínima (Prática):** ~64-128MB para CLI, ~256MB+ para um DE leve. Suporta diversas arquiteturas, incluindo 32-bit.
* **Análise:** Orientada à segurança e extremamente minimalista. Muito popular para containers Docker devido ao seu tamanho reduzido e foco em segurança. Usar como desktop requer mais configuração manual. A mudança de libc (musl) pode apresentar incompatibilidades com alguns softwares proprietários ou compilados para glibc.
* **Ideal para:** Servidores, containers, dispositivos embarcados, usuários avançados que buscam segurança e minimalismo extremo e não se importam em configurar o sistema do zero.

#### Void Linux
* **Site Oficial:** [voidlinux.org](https://voidlinux.org/)
* **Base:** Independente (usa Runit como init system por padrão)
* **Ambiente Gráfico:** Nenhuma por padrão (CLI). Várias opções disponíveis durante a instalação ou via pacotes.
* **RAM Mínima (Prática):** ~128MB para CLI, ~256-512MB+ para um DE leve. Suporta 32-bit (glibc apenas).
* **Análise:** Uma distribuição rolling-release construída do zero, conhecida por seu gerenciador de pacotes binário (XBPS) e o uso do Runit como sistema de init, que é mais simples e leve que systemd. Oferece versões com glibc ou musl libc. É rápida, estável e oferece bom controle ao usuário.
* **Ideal para:** Usuários com alguma experiência em Linux que buscam uma alternativa ao systemd, um sistema rolling-release leve e um gerenciador de pacotes eficiente.

#### Debian (Netinstall com DE Leve)
* **Site Oficial:** [debian.org](https://www.debian.org/)
* **Base:** Debian
* **Ambiente Gráfico:** Escolhido durante a instalação ou instalado posteriormente (LXQt, XFCE, Openbox, etc.)
* **RAM Mínima (Prática):** Varia muito com a escolha do DE/WM. ~64MB para CLI, ~192MB+ para um WM como Openbox. O suporte oficial para i386 foi descontinuado para novas instalações em versões recentes, mas a comunidade mantém portes e é possível instalar versões mais antigas ou usar portes não oficiais.
* **Análise:** A "distribuição universal". Usando a imagem de instalação via rede (netinstall) e desmarcando a opção de instalar um ambiente de desktop durante la instalação, você obtém um sistema base mínimo. A partir daí, pode instalar apenas os componentes necessários e um gerenciador de janelas ou DE leve. Oferece estabilidade incomparável e vastos repositórios. Requer mais configuração inicial se optar por este caminho.
* **Ideal para:** Usuários que querem controle total sobre os pacotes instalados, buscam máxima estabilidade e estão dispostos a configurar o ambiente gráfico manualmente.

#### Outras Menções Notáveis
* **Tiny Core Linux:** Para os minimalistas extremos, com ISOs a partir de ~16MB. Requer bastante conhecimento.
* **Slax:** Portátil, baseada em Debian, pode rodar da RAM.
* **Artix Linux:** Arch-based sem systemd (OpenRC, Runit, S6). Para usuários experientes que querem Arch sem systemd.

[↑ Sumário](#-sumário)

---

## ⚙️ Otimizações Essenciais de Sistema

**Importante:** Antes de aplicar otimizações avançadas, leia o [Alerta para Iniciantes](#️-alerta-para-iniciantes). Faça alterações uma de cada vez e teste a estabilidade.

### 🧬 Otimizando Parâmetros de Boot do Kernel (GRUB)

O GRUB (GRand Unified Bootloader) é o carregador de inicialização mais comum em sistemas Linux. Podemos passar parâmetros para o kernel através dele para influenciar o processo de boot e o comportamento do sistema.

**Como Editar:**
1.  Abra o arquivo de configuração do GRUB com um editor de texto e privilégios de root. O local mais comum é `/etc/default/grub`:
    ```bash
    sudo nano /etc/default/grub
    ```

2.  Procure pela linha que começa com `GRUB_CMDLINE_LINUX_DEFAULT`. Geralmente já contém opções como `quiet` ou `splash`.

3.  Adicione os novos parâmetros dentro das aspas existentes, separados por espaços.
    * Exemplo original: `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`
    * Exemplo modificado: `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash loglevel=3 pcie_aspm=force"`

4.  Salve o arquivo (Ctrl+O e Enter no nano, depois Ctrl+X).

5.  Atualize a configuração do GRUB para que as alterações sejam aplicadas no próximo boot:
    * Para sistemas baseados em Debian/Ubuntu (que usam `update-grub`):
        ```bash
        sudo update-grub
        ```
    * Para outras distros (Fedora, Arch, etc., que usam `grub-mkconfig` diretamente):
        ```bash
        sudo grub-mkconfig -o /boot/grub/grub.cfg
        # Ou, em sistemas EFI:
        # sudo grub-mkconfig -o /boot/efi/EFI/NOME_DA_DISTRO/grub.cfg
        # (Verifique o caminho correto para sua distro)
        ```

6.  Reinicie o computador.

**Parâmetros Úteis (teste individualmente):**
* `quiet`: Suprime a maioria das mensagens de boot (geralmente já presente).

* `splash`: Usado para exibir uma tela gráfica durante o boot. Removê-lo pode acelerar um pouco, mostrando mensagens de texto.

* `loglevel=3` ou `loglevel=4`: Reduz a quantidade de mensagens do kernel mostradas no console durante o boot. Níveis menores são mais silenciosos. (Padrão é geralmente 4 ou 7).

* `pcie_aspm=force`: Habilita forçadamente o Active State Power Management para dispositivos PCIe, podendo economizar energia e reduzir calor, mas em raros casos pode causar instabilidade com hardware específico.

* `elevator=noop` ou `elevator=deadline` (para HDDs): Altera o escalonador de I/O. `noop` é simples e pode ser bom para SSDs ou sistemas com CPU muito fraca. `deadline` é geralmente bom para HDDs. (Em kernels mais recentes, `none` e `mq-deadline` são os equivalentes para o framework multi-queue). Verifique o que seu kernel suporta: `cat /sys/block/sda/queue/scheduler` (substitua `sda` pelo seu disco).

* `threadirqs`: Força o threading de todas as interrupções, o que pode melhorar a responsividade em alguns sistemas.

#### Mitigações de Segurança vs. Performance (Aviso Importante)
Vulnerabilidades de CPU como Spectre, Meltdown, L1TF, MDS, etc., levaram à implementação de "mitigações" no kernel Linux. Essas mitigações protegem contra ataques, mas podem ter um impacto significativo na performance, especialmente em CPUs mais antigas.

**Desabilitar essas mitigações pode resultar em ganhos de performance, mas expõe seu sistema a riscos de segurança conhecidos.** Esta é uma troca que você deve considerar cuidadosamente. **NÃO é recomendado para sistemas que lidam com dados sensíveis, que são multiusuário, ou que estão constantemente conectados à internet sem outras camadas de proteção.** Use por sua conta e risco, idealmente em máquinas isoladas ou para propósitos específicos onde a performance é crítica e os riscos são compreendidos e aceitos.

Se decidir prosseguir, os seguintes parâmetros podem ser adicionados à linha `GRUB_CMDLINE_LINUX_DEFAULT`:
* Opção geral para desabilitar a maioria das mitigações:
    ```
    mitigations=off
    ```
* Ou uma combinação mais granular (exemplos, podem variar entre kernels e CPUs):
    ```
    noibrs noibpb nopti nospectre_v2 nospectre_v1 l1tf=off nospec_store_bypass_disable no_stf_barrier mds=off
    ```
A opção `mitigations=off` é um "atalho" mais abrangente. As opções granulares oferecem mais controle, mas são mais complexas de gerenciar e entender individualmente. A eficácia e disponibilidade dessas flags podem depender da sua versão do kernel e da arquitetura da CPU.

**Sempre verifique o impacto na performance e estabilidade após aplicar essas mudanças.** Consulte a documentação do kernel para os parâmetros mais atualizados e específicos da sua CPU.

### 🛠️ Gerenciamento de Serviços
Serviços (ou *daemons*) são programas que rodam em segundo plano. Desabilitar aqueles que você não usa pode liberar RAM e CPU.

#### Identificando Serviços
* **Systemd:**
    ```bash
    systemctl list-unit-files --type=service --state=enabled  # Ver serviços habilitados para iniciar no boot
    systemctl list-units --type=service --state=active      # Ver serviços atualmente rodando
    ```
* **Runit:**
    ```bash
    ls -l /etc/service/  # Serviços gerenciados e habilitados (links para /etc/sv/)
    sudo sv status /etc/service/* # Status dos serviços
    ```
* **OpenRC:**
    ```bash
    rc-update show -v # Ver serviços habilitados por runlevel
    rc-status --servicelist # Ver serviços e seus status
    ```

#### Desabilitando Serviços (Systemd, Runit, OpenRC)
* **Systemd:**
    ```bash
    sudo systemctl stop nome-do-servico.service      # Para o serviço agora
    sudo systemctl disable nome-do-servico.service   # Impede de iniciar no próximo boot
    # Para fazer ambos de uma vez:
    sudo systemctl disable --now nome-do-servico.service
    ```
* **Runit:** (O "serviço" é um diretório em `/etc/sv/`)
    ```bash
    sudo sv down /etc/service/nome-do-servico  # Para o serviço
    sudo rm /etc/service/nome-do-servico       # Remove o link, desabilitando
    # Para reabilitar: sudo ln -s /etc/sv/nome-do-servico /etc/service/
    ```
* **OpenRC:**
    ```bash
    sudo rc-service nome-do-servico stop             # Para o serviço agora
    sudo rc-update del nome-do-servico default     # Remove do runlevel padrão
    ```

#### Exemplos de Serviços Comumente Desabilitáveis
(Pesquise sobre cada um antes de desabilitar para ter certeza que não o utiliza)
* `cups.service` / `cupsd`: Sistema de impressão. Desabilite se não usa impressoras.

* `bluetooth.service` / `bluetoothd`: Suporte a Bluetooth.

* `ModemManager.service`: Gerencia modems (3G/4G/etc.).

* `avahi-daemon.service`: Descoberta de serviços em rede (mDNS/DNS-SD, similar ao Bonjour). Pode ser desnecessário em um desktop simples.

* `speech-dispatcher.service`: Serviço de conversão de texto em fala.

* `accounts-daemon.service`: Gerencia contas de usuário (D-Bus). Geralmente necessário para DEs completos, mas pode ser dispensável em WMs muito mínimos.

* `bolt.service`: Gerenciamento de dispositivos Thunderbolt.

* `lvm2-monitor.service`: Monitoramento de LVM (Logical Volume Management). Se não usa LVM.

* `irqbalance.service`: Distribui interrupções de hardware entre CPUs. Em sistemas single-core ou dual-core muito antigos, pode não trazer benefício ou até ter um pequeno overhead. Teste o impacto.

* `smartmontools.service` / `smartd`: Monitoramento S.M.A.R.T. de discos. Útil, mas pode ser desabilitado se performance for crítica e você monitora discos de outra forma.

* Serviços de rede específicos que você não usa (ex: `nfs-server.service`, `sshd.service` se não precisa de acesso SSH).

### 🗂️ Otimização do Sistema de Arquivos

#### Escolha do Filesystem (Ext4, XFS, F2FS)
* **Ext4:** Padrão na maioria das distros. Maduro, estável, bom para uso geral. Journaling ajuda na recuperação de falhas.

* **XFS:** Conhecido por bom desempenho com arquivos grandes e em operações paralelas. Pode ser uma boa opção para discos maiores ou servidores de arquivos. Journaling robusto.

* **F2FS (Flash-Friendly File System):** Projetado para dispositivos de armazenamento baseados em flash (SSDs, eMMC, cartões SD). Pode oferecer melhor desempenho e durabilidade para esses dispositivos.

* **Btrfs:** Filesystem moderno com muitos recursos (snapshots, CoW, etc.), mas pode ter um overhead maior em hardware muito antigo.

Para HDDs antigos, Ext4 é uma escolha segura e geralmente boa. XFS pode oferecer vantagens em cenários específicos. Se estiver usando um SSD (mesmo antigo), F2FS pode valer a pena ser considerado, mas verifique o suporte da sua distro. Algumas distros como AntiX oferecem a opção de formatar com F2FS durante a instalação.

#### Opções de Montagem (noatime, nodiratime)
Podem ser adicionadas ao seu arquivo `/etc/fstab` para reduzir as escritas em disco.
* `noatime`: Impede a atualização do tempo de acesso aos arquivos toda vez que são lidos. Isso pode reduzir significativamente as escritas em disco, especialmente em servidores ou sistemas com muita leitura de arquivos pequenos.

* `nodiratime`: Similar ao `noatime`, mas apenas para diretórios. `noatime` geralmente implica `nodiratime`.

**Como Adicionar:**
1.  Faça backup do seu `/etc/fstab`: `sudo cp /etc/fstab /etc/fstab.bak`

2.  Edite o arquivo: `sudo nano /etc/fstab`

3.  Para a partição desejada (ex: `/` ou `/home`), adicione `noatime` às opções de montagem, separada por vírgula.

    * Exemplo de linha original:
        `UUID=xxxx-xxxx / ext4 errors=remount-ro 0 1`

    * Exemplo modificado:
        `UUID=xxxx-xxxx / ext4 defaults,noatime,errors=remount-ro 0 1` (adicionar `defaults` se não houver outras opções além de `errors` e `dump/pass`).
        Se já houver `defaults`, substitua-o ou adicione `noatime` à lista:
        `UUID=xxxx-xxxx / ext4 defaults,noatime 0 1`
        Ou se já há outras opções:
        `UUID=xxxx-xxxx / ext4 rw,noatime,errors=remount-ro 0 1`
4.  Salve e reinicie, ou remonte a partição: `sudo mount -o remount /` (ou a partição específica).

**Cuidado:** Algumas raras aplicações podem depender do `atime` (como alguns sistemas de backup incremental ou `mutt` para detectar novos e-mails). Na prática, é raramente um problema para desktops.

### 💾 Swap e Gerenciamento de Memória

Swap é uma área no disco rígido usada quando a memória RAM física está cheia. Em HDDs lentos, o uso excessivo de swap degrada drasticamente a performance.

#### Ajustando Swappiness
O parâmetro `vm.swappiness` controla o quão "agressivamente" o kernel tentará mover dados da RAM para o swap. Varia de 0 a 200 (em kernels mais recentes, mas historicamente 0-100).
* **Valores altos (ex: 60, padrão comum):** Swap mais frequente.

* **Valores baixos (ex: 10, 5, 1):** Swap menos frequente, o kernel tentará manter mais coisas na RAM. `1` é geralmente o mínimo recomendado para evitar problemas de Out-Of-Memory (OOM) em situações de memória muito baixa, em vez de `0`.

Em desktops com HDDs lentos, um valor mais baixo (ex: 10 ou 20) é geralmente recomendado para priorizar o uso da RAM.
1.  Verificar valor atual: `cat /proc/sys/vm/swappiness`

2.  Mudar temporariamente: `sudo sysctl vm.swappiness=10`

3.  Tornar permanente: Crie/edite um arquivo em `/etc/sysctl.d/` (ex: `/etc/sysctl.d/99-swappiness.conf`) e adicione a linha:
    ```
    vm.swappiness=10
    ```
    Depois, aplique com `sudo sysctl -p /etc/sysctl.d/99-swappiness.conf` ou reinicie.

#### Configurando ZRAM
ZRAM cria um dispositivo de bloco compactado na RAM, que pode ser usado como swap. Acessar dados compactados na RAM é muito mais rápido do que acessar o swap no disco. É altamente recomendado para sistemas com pouca RAM e/ou HDDs lentos.

1.  **Instalação:**
    * Muitas distros modernas já vêm com ZRAM ou facilitam sua instalação.

    * Debian/Ubuntu: `sudo apt install zram-tools` ou `systemd-zram-generator` (este último é mais moderno e geralmente preferido se disponível).

    * Outras distros: Verifique a documentação. `zram-generator` é um projeto systemd que simplifica a configuração.

2.  **Configuração (exemplo com `zram-tools` em `/etc/default/zramswap`):**

    * `ALGO=zstd` (algoritmo de compressão, zstd é rápido e eficiente, lz4 também é bom)

    * `PERCENT=50` (usar 50% da RAM para zram, ajuste conforme necessário)
    Ou, para `systemd-zram-generator`, crie `/etc/systemd/zram-generator.conf` com:
    ```ini
    [zram0]
    zram-size = ram / 2  # Ou um valor fixo como 1G
    compression-algorithm = zstd
    ```
3.  **Habilitar e Iniciar:**

    * `zram-tools`: `sudo systemctl enable --now zramswap`

    * `systemd-zram-generator`: Geralmente é ativado automaticamente no boot após a instalação e criação do arquivo de configuração.

4.  **Verificar:** Use `swapon -s` ou `zramctl` para ver os dispositivos zram ativos.

**Prioridade do Swap:** Se você tem zram e swap em disco, configure a prioridade do zram para ser maior, para que ele seja usado primeiro. `swapon -s` mostra as prioridades. ZRAM geralmente já é configurado com alta prioridade.

#### Swap em Partição vs. Arquivo Swap
* **Partição Swap:** Tradicional. Criada durante a instalação.

* **Arquivo Swap:** Um arquivo no seu filesystem usado como swap. Mais flexível para criar, redimensionar ou remover. A performance é geralmente comparável à de uma partição swap em discos modernos, mas em HDDs muito fragmentados uma partição contígua *poderia* ter uma leve vantagem.

Para hardware antigo, se já tem uma partição swap, pode usá-la como último recurso após o ZRAM. Se não tem, criar um arquivo swap é mais fácil.

### 🖼️ Ambientes Gráficos (DE) e Gerenciadores de Janelas (WM) Leves

A escolha da interface gráfica é uma das que mais impacta o consumo de recursos.

#### Recomendações (LXQt, XFCE, Openbox, i3wm, etc.)

* **Desktop Environments (DEs) Leves:**
    * **LXQt:** Usa Qt. Leve, modular, visual moderno. Consumo de RAM ~150-250MB.

    * **XFCE:** Usa GTK. Estável, configurável, visual clássico. Consumo de RAM ~200-350MB.

    * **MATE:** Fork do GNOME 2 (GTK). Similar ao XFCE em recursos e consumo.

* **Window Managers (WMs) Minimalistas (empilháveis):**

    * **Openbox:** Altamente configurável via arquivos XML. Muito leve. Consumo de RAM ~50-150MB (com um painel leve como Tint2 ou LXPanel). Requer configuração manual de menus, painéis, etc.

    * **Fluxbox:** Similar ao Openbox, também muito leve e configurável.

    * **IceWM:** Leve, com foco em imitar o visual de interfaces mais antigas (Windows 95/NT). Fácil de usar.

    * **JWM (Joe's Window Manager):** Extremamente leve, usado no Puppy Linux e SliTaz.

* **Window Managers (WMs) Minimalistas (dinâmicos/tiling):**

    * **i3wm:** Popular tiling WM. Configurado via arquivo de texto. Eficiente para quem usa muito o teclado. Curva de aprendizado maior. Consumo de RAM ~20-100MB.

    * **dwm (Dynamic Window Manager):** Filosofia "suckless". Configurado editando o código fonte em C e recompilando. Ultra minimalista.

    * **AwesomeWM:** Tiling WM altamente configurável via Lua.

Para iniciantes, LXQt ou XFCE são recomendados. Para mais performance, Openbox (com algum painel) é um bom próximo passo. Tiling WMs são para usuários que buscam máxima eficiência e minimalismo, dispostos a investir tempo na configuração.

#### Dicas para Minimizar o Consumo (Compositor, Temas)
* **Compositor:** Responsável por efeitos visuais (transparências, sombras). Pode consumir recursos.

    * Desabilitar completamente o compositor se não precisar de efeitos.

    * Usar um compositor leve como `picom` (fork do Compton) ou `xcompmgr` com configurações mínimas. Evite configurações pesadas de blur ou animações.

* **Temas e Ícones:** Temas GTK/Qt e conjuntos de ícones complexos podem consumir mais RAM. Opte por temas simples e leves.

* **Papel de Parede:** Use uma cor sólida ou uma imagem leve. Evite papéis de parede animados ou slideshows.

* **Fontes:** Use fontes padrão e evite instalar muitas fontes desnecessárias.

* **Notificações:** Configure o daemon de notificação (ex: `dunst` para leveza) para ser discreto.

### 🚀 Aplicações ao Iniciar (Startup Applications)
Muitos DEs permitem gerenciar quais aplicativos iniciam automaticamente com a sessão. Verifique as configurações do seu DE (ex: "Sessão e Inicialização" no XFCE/LXQt) e desabilite o que não for essencial.
Para WMs minimalistas, você controla isso no seu script de inicialização (ex: `~/.config/openbox/autostart`, `~/.xinitrc`, `~/.config/i3/config`).

### 🧹 Limpeza do Sistema
Remover pacotes órfãos, cache de pacotes e arquivos desnecessários pode liberar espaço em disco e, em alguns casos, melhorar um pouco a performance.

* **Para sistemas baseados em Debian/Ubuntu (apt):**
    ```bash
    sudo apt update
    sudo apt autoremove  # Remove dependências órfãs
    sudo apt clean       # Remove arquivos .deb baixados do cache
    sudo apt autoclean   # Remove arquivos .deb antigos do cache
    ```
* **Para sistemas baseados em Arch (pacman):**
    ```bash
    # Remover pacotes órfãos (não mais requeridos)
    sudo pacman -Rns $(pacman -Qtdq)
    # Limpar cache de pacotes (exceto as 3 últimas versões de cada)
    sudo paccan -Sc
    # Limpar todo o cache de pacotes (libera mais espaço, mas precisará baixar novamente se reinstalar)
    sudo pacman -Scc
    ```
* **Para Fedora (dnf):**
    ```bash
    sudo dnf autoremove
    sudo dnf clean all
    ```
* **BleachBit (use com MUITA cautela):** Ferramenta gráfica que pode limpar caches de navegadores, sistema, etc. Se não souber o que uma opção faz, NÃO a marque, pois pode remover dados importantes ou quebrar configurações.

[↑ Sumário](#-sumário)

---

## 🔧 Software Leve e Eficiente

A escolha do software tem um impacto enorme. Priorize alternativas leves.

### 🌐 Navegadores Web
Esta é a categoria mais desafiadora, pois a web moderna é pesada.
* **Falkon:** Baseado no QtWebEngine (motor do Chromium/Blink). Relativamente leve e com boa compatibilidade.

* **Pale Moon:** Fork do Firefox (motor Goanna, um fork do Gecko). Focado em eficiência e customização. Pode ser mais leve que o Firefox moderno em alguns casos.

* **Midori:** Historicamente um navegador leve baseado em WebKitGTK.

* **GNOME Web (Epiphany):** Usa WebKitGTK. Pode ser surpreendentemente leve e bem integrado se você usa um ambiente GTK.

* **Links2 / ELinks / Lynx / w3m:** Navegadores de modo texto ou com interface gráfica muito simples (Links2). Excelentes para acesso rápido a informação, documentação, ou sites simples. Consomem pouquíssimos recursos. `w3m-img` pode até exibir imagens no terminal.

* **Firefox (com otimizações):** Se precisar de um navegador completo, use com poucas abas, bloqueadores de scripts/anúncios (uBlock Origin), e extensões para suspender abas inativas (The Great Suspender/Discarder). Desative a reprodução automática de mídia. Em `about:config`, procure por configurações que reduzam o consumo de memória (ex: `browser.sessionstore.interval`).

* **Dica:** Use `yt-dlp` para baixar vídeos do YouTube e assistir offline com `mpv` em vez de no navegador.

### 📝 Editores de Texto e IDEs

* **Editores de Texto GUI Leves:**
    * **Leafpad / Mousepad:** Editores GTK muito simples e leves, similar ao Bloco de Notas.

    * **FeatherPad:** Baseado em Qt, leve e com mais recursos que Leafpad (abas, verificação ortográfica, etc.).

    * **Geany:** Editor de texto rápido e leve com funcionalidades básicas de IDE (compilação, terminal integrado, autocompletar simples). Excelente para scripts e projetos pequenos.

* **Editores de Texto CLI (Terminal):**
    * **Nano:** Simples, fácil de usar, bom para iniciantes no terminal.

    * **Vim / NeoVim:** Poderosos, eficientes, mas com curva de aprendizado íngreme. Altamente customizáveis.

    * **Micro:** Similar ao Nano em facilidade, mas com mais recursos modernos (suporte a mouse, atalhos comuns, plugins).

    * **Helix:** Editor modal inspirado no Kakoune/Neovim, escrito em Rust, focado em "zero configuration".

* **IDEs Leves (se Geany não for suficiente):**

    * **VSCodium / VSCode (com extensões desabilitadas):** Podem ser usados com cuidado, desabilitando extensões pesadas e telemetria (VSCodium é a versão sem telemetria da Microsoft). Ainda serão mais pesados que Geany.

    * Para linguagens específicas, podem existir IDEs leves dedicadas.

### 🎬 Reprodutores de Mídia
* **MPV:** Reprodutor de vídeo e áudio minimalista, mas extremamente poderoso e configurável via linha de comando ou arquivos de configuração. Leve e eficiente. Altamente recomendado.

* **VLC (com moderação):** Embora mais pesado que MPV, ainda é mais leve que muitos outros players GUI e lida com uma vasta gama de formatos. Use skins simples e desabilite recursos desnecessários.

* **Audacious / qmmp:** Reprodutores de áudio leves, com interfaces que lembram o Winamp.

* **cmus / moc:** Reprodutores de áudio para o terminal. Extremamente leves e eficientes para gerenciamento de bibliotecas de música.

### 📑 Visualizadores de Documentos (PDF, Office, etc.)
* **PDF:**
    * **Zathura:** Visualizador de PDF (e outros formatos como DjVu, PostScript) minimalista, controlado pelo teclado (estilo Vim). Muito leve e rápido.

    * **MuPDF:** Similar ao Zathura em leveza e filosofia, também com renderizador próprio muito rápido. `mupdf-gl` é a versão GUI.

    * **qpdfview:** Visualizador de PDF em abas, baseado em Qt, leve e com boas funcionalidades.

    * **Xpdf:** Um dos visualizadores de PDF mais antigos e leves, interface simples.

    * Evite visualizadores de PDF completos e pesados baseados em Electron ou engines de navegadores.

* **Documentos Office (ODT, DOCX, etc.):**

    * **AbiWord (para .doc, .docx, .odt):** Processador de texto leve.

    * **Gnumeric (para .xls, .xlsx, .ods):** Planilha eletrônica leve.

    * **LibreOffice (com ressalvas):** É uma suíte completa e pode ser pesada. No entanto, para visualização rápida ou edições simples, pode ser aceitável se você tiver pelo menos 1-2GB de RAM. Use `libreoffice --writer nome_do_arquivo.odt` para abrir apenas o componente necessário. Configure para usar menos RAM (desabilitar Java, reduzir cache de imagens).

    * Para visualização, considere converter para PDF se possível.

* **Markdown:** `glow`, `mdless` (terminal), ou editores de texto com preview (Geany, FeatherPad).
* **Ebooks (EPUB, MOBI):**

    * **FBReader:** Leitor de ebook leve e multiplataforma.
    
    * **Calibre (E-book viewer):** A suíte Calibre é pesada, mas seu visualizador (`ebook-viewer`) pode ser usado separadamente e é razoável.

    * **Zathura** com plugins pode ler EPUB.

    * **KOReader** (para Android, mas mencionado aqui pela relevância).

### ⌨️ Ferramentas Essenciais de Linha de Comando
Aprender a usar o terminal pode economizar muitos recursos.

* **Gerenciador de Arquivos:**

    * `ranger`: Estilo Vim, com previews.
    * `nnn` (Nnn's Not Noice): Extremamente rápido e leve, muitas funcionalidades.
    * `mc` (Midnight Commander): Interface de dois painéis, estilo Norton Commander.
* **Monitoramento de Sistema:**
    * `htop` / `btop` / `bpytop`: Monitores de processo interativos. `htop` é o mais clássico e leve.
    * `vmstat`, `iostat`, `free`, `df`: Comandos para informações específicas do sistema.
* **Rede:** `curl`, `wget`, `ping`, `ip`, `nmap` (com cautela).
* **Busca de Arquivos:** `find`, `locate`, `grep`, `ripgrep` (rg - muito rápido).
* **Edição de Texto:** Já mencionados (nano, vim, micro, helix).
* **Multiplexadores de Terminal:**
    * `tmux`: Permite múltiplas sessões, painéis e janelas em um único terminal.
    * `screen`: Clássico, similar ao tmux.

### 🖥️ Emuladores de Terminal Leves
O terminal padrão do seu DE pode ser leve o suficiente (ex: `lxterminal`, `xfce4-terminal`). Se precisar de algo ainda mais leve:
* `st` (Simple Terminal - suckless.org): Extremamente minimalista, configurado via patch e recompilação do código C.
* `urxvt` (rxvt-unicode): Leve, rápido e altamente configurável via `~/.Xresources`. Bom suporte a Unicode.
* `alacritty`: Acelerado por GPU (pode ou não ser benéfico em GPUs muito antigas), escrito em Rust. Rápido.
* `kitty`: Também acelerado por GPU, com muitos recursos.

### 💻 (Opcional) Linguagens de Programação com Baixo Overhead
Para scripts, automação ou desenvolvimento leve no próprio PC antigo.

* **Shell Script (Bash, Dash, sh):** Já presente no sistema. Ideal para automação de tarefas. `dash` é mais leve que `bash`.

* **Awk / Sed:** Poderosas para processamento de texto.

* **Lua:** Linguagem de script leve, rápida e fácil de embutir.

* **C / C++:** Para máxima performance e controle, mas com ciclo de desenvolvimento mais longo (compilação).

* **Python (com ressalvas):** Embora o interpretador em si possa ser pesado para hardware *muito* antigo, para scripts simples e usando apenas a biblioteca padrão ou módulos leves, pode ser aceitável. Evite frameworks pesados ou bibliotecas com muitas dependências C.

* **Perl:** Similar ao Python em termos de uso de recursos para scripts.

* **Tcl/Tk:** Bom para GUIs simples e leves.

Evite rodar ambientes de desenvolvimento pesados (grandes IDEs Java/Node.js) diretamente na máquina antiga, se possível. Considere desenvolvimento cruzado ou acesso remoto a uma máquina mais potente.

[↑ Sumário](#-sumário)

---

## 🛠️ Casos de Uso Específicos para Hardware Antigo

### 🎮 Transformando em uma Central de Jogos Retrô
Hardware antigo é perfeito para emular consoles clássicos.

#### Batocera.linux
* **Site Oficial:** [batocera.org](https://batocera.org/)

* **O que é:** Uma distribuição Linux completa, focada e otimizada para retrogaming. Inicializa diretamente na interface EmulationStation.

* **Vantagens:** Fácil de configurar (gravar no pendrive/HD e dar boot), detecta controles automaticamente, interface amigável, suporta uma vasta gama de emuladores.

* **Como usar:**
    1.  Baixe a imagem para x86 (32-bit ou 64-bit) do site.

    2.  Use Balena Etcher ou similar para gravar em um pendrive ou HD dedicado.

    3.  Dê boot pela mídia criada.

    4.  Adicione suas ROMs (jogos) e BIOS (se necessário para alguns emuladores) via rede ou conectando o dispositivo de armazenamento a outro PC.
* **Importante:** Batocera assume o controle total da máquina para focar nos jogos. Não é para uso como desktop geral simultaneamente.

#### Outras Opções (Lakka, RetroArch)
* **Lakka:** Similar ao Batocera, também uma distro Linux dedicada ao RetroArch. ([lakka.tv](https://www.lakka.tv/))

* **RetroArch em uma Distro Leve:** Você pode instalar o RetroArch (frontend para emuladores Libretro) em qualquer uma das distros leves mencionadas (Lubuntu, AntiX, etc.). Dá mais flexibilidade para usar o PC para outras coisas, mas requer mais configuração manual dos emuladores e da interface.

#### Requisitos e Dicas
* **CPU e RAM:**
    * Consoles 8-bit e 16-bit (NES, SNES, Mega Drive): Roda em praticamente qualquer coisa (Pentium III, 256MB RAM).

    * PlayStation 1, N64 (parcial), GBA: Pentium 4/Athlon XP, 512MB RAM.
    * Dreamcast, PSP, Nintendo DS: Core 2 Duo fraco ou Athlon X2, 1-2GB RAM.
    * GameCube, PS2: Requerem CPUs e GPUs significativamente mais potentes, geralmente inviável para hardware *realmente* antigo.
* **Controles:** Controles USB genéricos, controles de PS3/PS4 (via USB ou Bluetooth), Xbox 360/One.

* **Armazenamento:** Um pendrive rápido ou um SSD pequeno (mesmo antigo) para o sistema e ROMs mais acessadas faz diferença.

* **Dica:** Organize suas ROMs e BIOS corretamente. Verifique a documentação do Batocera/Lakka/RetroArch para as pastas corretas e nomes de BIOS.

### 🖥️ Configurando um Servidor Doméstico Leve
Um PC antigo pode ser um excelente servidor para tarefas simples, rodando 24/7 com baixo consumo de energia (comparado a um desktop moderno).

#### Ideias de Servidores
* **NAS (Network Attached Storage):** Compartilhamento de arquivos na rede local.
    * Software: Samba (para compatibilidade com Windows), NFS (para Linux/macOS).
    * Use `rsync` para backups.
* **Servidor Web Leve:** Para hospedar sites estáticos, um blog pessoal simples, ou uma aplicação web leve.
    * Software: Nginx, Lighttpd, Caddy.
* **Servidor de Mídia (DLNA/UPnP):** Stream de vídeos e músicas para TVs, consoles, etc.
    * Software: MiniDLNA (ReadyMedia), Rygel, Gerbera.
* **Pi-hole:** Bloqueador de anúncios e rastreadores para toda a sua rede (DNS sinkhole).
* **Servidor Git Pessoal:** Para hospedar seus próprios repositórios Git.
    * Software: Gitea (escrito em Go, leve), Gogs, ou `git daemon` simples.
* **Servidor VPN:** Para acesso seguro à sua rede doméstica de qualquer lugar.
    * Software: WireGuard (moderno e eficiente), OpenVPN.
* **Servidor de Impressão (CUPS):** Compartilhar uma impressora na rede.

* **Servidor de Testes/Desenvolvimento:** Para rodar pequenos bancos de dados, aplicações web em desenvolvimento.
* **Monitoramento de Rede/Serviços:** Zabbix (agent), Nagios (agent), Monit.

#### Recomendações de Distros Server (Debian Minima, Alpine)
* **Debian (Netinstall, sem GUI):** Extremamente estável e confiável. Instale apenas os pacotes essenciais.

* **Alpine Linux:** Muito seguro e com pegada de recursos minúscula. Ideal para appliances e servidores dedicados.
* **Ubuntu Server (LTS):** Mais recursos e pode ser mais pesado, mas com boa documentação e suporte.
* Qualquer distro leve configurada sem interface gráfica e com serviços otimizados.

#### Dicas de Segurança e Manutenção
* **Instalação Headless:** Sem monitor, teclado ou mouse, acessado via SSH.

* **SSH Seguro:** Use chaves SSH em vez de senhas, mude a porta padrão (opcional), configure `fail2ban`.
* **Firewall:** Configure `ufw` (Uncomplicated Firewall) ou `iptables`.
* **Atualizações Regulares:** Mantenha o sistema e os softwares atualizados.
* **Monitoramento:** Verifique logs, uso de disco e recursos.
* **Backups:** Faça backup de configurações importantes e dados.

### 📱 Reutilizando Celulares e Tablets Android Antigos
Tem um Android velho esquecido na gaveta? Dá para transformá-lo em um **e-reader**

#### E-reader com KOReader
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

### 📱 Como instalar e configurar

Assista ao tutorial completo para orientação passo-a-passo:  
🎥 [Como transformar um celular Android antigo em e-reader](https://youtu.be/p2AnbPfqYpQ?si=CadMHOH0TcGXK8gC)

#### Outros Usos (Monitor de Sistema, Câmera de Segurança Simples)

* **Monitor de Sistema Remoto:** Apps como `Termux` (para rodar `htop`, `ssh` para seus outros PCs) ou apps específicos de monitoramento.

* **Câmera de Segurança IP Simples:** Apps como "IP Webcam" podem transformar um celular antigo em uma câmera acessível pela rede. A qualidade dependerá da câmera do celular.
* **Rádio/Player de Música Online:** Com Wi-Fi, pode ser um player dedicado para Spotify, TuneIn Radio, etc., conectado a caixas de som.
* **Relógio de Cabeceira Inteligente:** Apps de relógio com informações de tempo, alarmes.
* **Painel de Controle para Casa Inteligente (muito básico):** Se você usa Home Assistant ou similar, pode usar um tablet antigo para exibir uma interface web simples.
* **Porta-retrato Digital:** Apps de slideshow de fotos.

[↑ Sumário](#-sumário)

---

## 💡 Dicas Avançadas

### Considerações sobre Hardware (SSD, RAM)
* **SSD (Solid State Drive):** A atualização de hardware que mais impacta a sensação de velocidade, especialmente em PCs com HDDs lentos. Mesmo um SSD SATA antigo e pequeno (60-120GB) para o sistema operacional fará uma diferença brutal nos tempos de boot e abertura de aplicativos.

* **RAM (Memória):** Se sua placa-mãe suportar e você encontrar pentes de memória compatíveis e baratos (DDR1, DDR2, DDR3), aumentar a RAM para 1GB, 2GB ou até 4GB pode permitir o uso de softwares um pouco mais pesados ou mais abas no navegador. Verifique o tipo e a capacidade máxima suportada pela sua placa-mãe.

* **Limpeza Física:** Poeira acumulada pode causar superaquecimento e reduzir o desempenho (throttling). Limpe os coolers e dissipadores.

* **Pasta Térmica:** Se o PC tem muitos anos, a pasta térmica entre o processador/GPU e o dissipador pode estar ressecada. Substituí-la pode melhorar as temperaturas. (Procedimento delicado, pesquise antes).

### Streaming de Jogos (Nware, Steam Link, Moonlight)
Se o PC antigo tem uma boa conexão de rede (idealmente cabeada), mas hardware gráfico fraco, você pode usá-lo como um cliente para streaming de jogos de um PC mais potente na mesma rede ou de serviços na nuvem.

* **Steam Link:** Permite jogar jogos da sua biblioteca Steam de um PC gamer em outro dispositivo na rede local. O cliente Steam Link para Linux é leve.

* **Moonlight:** Cliente open-source para o NVIDIA GameStream (se você tem um PC com GPU NVIDIA compatível). Funciona muito bem.

* **Serviços de Cloud Gaming (ex: GeForce NOW, Xbox Cloud Gaming):** Alguns podem funcionar via navegador web ou cliente Linux leve. Requerem excelente conexão com a internet e assinatura.

* **Parsec:** Outra opção para streaming de desktop/jogos com baixa latência. (Tambem permite jogar coop localmente, muito usado em emuladores)

### Impressoras e Periféricos Antigos
* **CUPS (Common Unix Printing System):** O sistema de impressão padrão no Linux. Geralmente detecta impressoras USB automaticamente. Pode ser acessado via interface web (`http://localhost:631`).

* **Drivers:**
    * Muitas impressoras antigas são suportadas nativamente ou pelo projeto `gutenprint`.

    * Para HP, `hplip` (HP Linux Imaging and Printing) oferece bom suporte.

    * Para Brother, a empresa costuma fornecer drivers Linux em seu site.

* **Scanners:** `SANE` (Scanner Access Now Easy) é o framework padrão. Ferramentas GUI como `simple-scan` ou `xsane`.

* **Portas Seriais/Paralelas:** Linux tem excelente suporte. Ferramentas como `minicom` ou `setserial` para configurar.

[↑ Sumário](#-sumário)

---

## ♻️ Descarte Consciente de Hardware
Se, mesmo após todas as tentativas, o hardware estiver verdadeiramente inutilizável ou se você tiver componentes que não podem ser reaproveitados, é importante descartá-los corretamente. Lixo eletrônico contém materiais tóxicos que podem contaminar o solo e a água se descartados em aterros comuns.

* **Procure Pontos de Coleta:** Muitas cidades e empresas possuem programas de reciclagem de lixo eletrônico. Pesquise por "descarte lixo eletrônico [sua cidade]" ou "reciclagem eletrônicos [sua cidade]".

* **ABREE (Associação Brasileira de Reciclagem de Eletroeletrônicos e Eletrodomésticos):** No Brasil, a ABREE possui um site que ajuda a localizar pontos de recebimento: [abree.org.br/pontos-de-recebimento](https://abree.org.br/pontos-de-recebimento)
* **Fabricantes e Varejistas:** Algumas empresas de eletrônicos e grandes varejistas têm programas de coleta de produtos antigos.
* **Doação (se ainda funcional para algo):** Mesmo que não sirva para você, talvez uma peça (como um HD pequeno, memória, ou até o gabinete) possa ser útil para projetos de estudantes, hackerspaces ou alguém com necessidades ainda mais básicas.

**Não jogue eletrônicos no lixo comum!**

[↑ Sumário](#-sumário)

---

## ❓ FAQ - Perguntas Frequentes

* **Qual a curva de aprendizado do Linux para hardware antigo?**
    * R: Para uso básico com distros como Lubuntu ou Xubuntu, a curva é suave, similar a aprender qualquer novo sistema operacional. A interface é gráfica e intuitiva. O desafio aumenta se você quiser otimizações profundas via terminal, mas isso é opcional. A comunidade Linux é vasta e prestativa.
* **Preciso mesmo usar o terminal (linha de comando)?**
    * R: Para uso básico e com distros amigáveis, não necessariamente. No entanto, o terminal é uma ferramenta poderosa para otimizações, diagnósticos e automação, e muitas dicas avançadas o utilizam. Aprender o básico do terminal pode ser muito recompensador e economizar recursos do sistema.
* **Como sair do Vim/NeoVim?**
    * R: Pressione a tecla `Esc` para garantir que está no modo Normal. Depois:
        * Para sair sem salvar as alterações: digite `:q!` e pressione `Enter`.

        * Para salvar as alterações e sair: digite `:wq` e pressione `Enter`.
        * Para aprender o básico do Vim, digite `vimtutor` no terminal e siga o tutorial interativo.
* **Vale a pena o esforço de otimizar um PC tão antigo?**
    * R: Sim, por vários motivos:
        * **Aprendizado:** Você aprenderá muito sobre Linux e como os sistemas funcionam.

        * **Sustentabilidade:** Reduz o lixo eletrônico.
        * **Utilidade:** O PC pode se tornar útil para tarefas específicas (servidor, jogos retrô, máquina de escrever digital).
        * **Satisfação:** É gratificante ver uma máquina antiga rodando de forma fluida.
        * **Custo:** É uma forma de ter um computador funcional sem gastar (ou gastando muito pouco).
* **Posso assistir YouTube/Netflix em um PC muito antigo com Linux?**
    * R: Depende muito do quão antigo. Navegadores modernos são pesados.
        * Para YouTube, usar `yt-dlp` para baixar o vídeo e `mpv` para assistir é a forma mais leve. Alguns clientes de YouTube alternativos e leves podem existir, mas a API do YouTube muda frequentemente.

        * Netflix e outros serviços de streaming com DRM podem ser desafiadores. Um navegador leve com bom suporte a HTML5 e Widevine CDM (como Firefox ou um derivado do Chromium) será necessário, e mesmo assim, a performance da CPU para decodificação de vídeo pode ser um gargalo. Resoluções mais baixas (480p, 360p) terão mais chance de funcionar.
* **E se eu quebrar o sistema tentando otimizar?**
    * R: Faz parte do aprendizado!
        * **Prevenção:** Faça uma otimização de cada vez e teste. Faça backup de arquivos de configuração importantes antes de editá-los.

        * **Recuperação:** Use um Live USB da sua distro para acessar o sistema de arquivos e reverter alterações. Aprenda a usar o modo de recuperação do GRUB (se disponível) para acessar um console de root ou um kernel anterior.

        * **Reinstalação:** Em último caso, reinstalar uma distro Linux leve é rápido. Mantenha seus dados pessoais em uma partição separada (`/home`) para facilitar.
* **Como posso deixar a aparência mais "moderna" sem pesar?**
    * R: Use temas GTK/Qt e conjuntos de ícones leves, mas com design limpo (ex: Arc, Numix, Papirus). Um compositor leve como `picom` com sombras sutis e transparências (sem blur excessivo) pode adicionar um toque de modernidade. Um bom papel de parede e fontes legíveis também ajudam.

[↑ Sumário](#-sumário)

---

## 🤝 Como Contribuir
Contribuições são muito bem-vindas! Se você tem dicas, correções, sugestões de software leve ou novas otimizações, por favor:
1.  Abra uma [Issue](https://github.com/gustavofjacome/pc-batata/issues) para discutir a mudança.
2.  Ou, se preferir, faça um Fork do repositório, crie um branch para sua modificação (`git checkout -b minha-nova-feature`) e abra um [Pull Request](https://github.com/gustavofjacome/pc-batata/pulls) detalhando suas alterações.

[↑ Sumário](#-sumário)

---

## 🙏 Agradecimentos e Inspiração

* Fortemente inspirado pelo repositório [terremoth/pc-carroca](https://github.com/terremoth/pc-carroca)
* Agradecimentos a [Diolinux](https://www.diolinux.com.br/), [Arch Wiki](https://wiki.archlinux.org/), e inúmeros fóruns e blogs da comunidade Linux brasileira e internacional.

[↑ Sumário](#-sumário)

---
