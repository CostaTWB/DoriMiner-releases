# DoriMiner (versão de teste)

Gestor de mineração para placas **NVIDIA**, em **Windows** e **Linux**. Instala os miners, cria perfis
(moeda, pool, a tua carteira) e põe a minerar a partir de uma página no browser, sem editar ficheiros.
Mostra o estado das placas, mede o que cada perfil rende, limita potência, ventoinhas e overclock, e
pode trocar de moeda sozinho. Também se controla pelo telemóvel.

> **Isto é uma versão de teste (beta).** Está a ser experimentada em poucas máquinas. Pode ter erros.
> Usa-a se queres ajudar a testar, e diz o que correu mal.

## Descarregar

Vai a **[Releases](../../releases/latest)** e descarrega o ficheiro do teu sistema:

| Sistema | Ficheiro | Como arrancar |
|---|---|---|
| Windows 10/11 | `DoriMiner-windows-….zip` | Extrai o zip para uma pasta do disco e dá dois cliques em `DoriMiner` |
| Linux | `DoriMiner-linux-….tar.gz` | `tar -xzf DoriMiner-linux-….tar.gz`, entra na pasta e `bash doriminer.sh` |

Não é preciso instalar mais nada: o kit já traz o que precisa. O [LEIA-ME](LEIA-ME.txt) explica o arranque
passo a passo e o que fazer se algo correr mal. Cada release tem o SHA-256 dos ficheiros, para confirmares
que o que descarregaste é o que foi publicado.

## O que precisas

- Uma ou mais placas **NVIDIA** com o driver instalado. Placas AMD não são suportadas.
- **Windows:** abrir o DoriMiner como administrador (ele pergunta), para o limite de potência, as ventoinhas
  e o overclock funcionarem. Sem isso minera na mesma.
- Um **endereço público** de carteira da moeda que queres minerar.
- Para várias máquinas e para o telemóvel: o **Tailscale** (gratuito, tailscale.com) em cada máquina e no
  telemóvel, com a mesma conta. Sem Tailscale, o DoriMiner só se usa no próprio computador: não abre portas
  na tua rede.

## O que deves saber antes de usar

- **O Windows e o antivírus podem avisar.** O Windows mostra "O Windows protegeu o seu PC" porque o
  programa ainda não é conhecido da Microsoft ("Mais informações" > "Executar mesmo assim"). Os antivírus
  costumam marcar os programas de mineração como indesejados, mesmo os legítimos; se apagar um miner, o
  DoriMiner diz que pasta acrescentar às exclusões.
- **Overclock, limite de potência e ventoinhas são por tua conta e risco.** O DoriMiner tem proteção
  térmica ligada por defeito e repõe os valores de fábrica quando para, mas forçar uma placa pode
  avariá-la. Começa com valores conservadores.
- **Fecha os outros programas que mexem na placa** (MSI Afterburner e parecidos, a aplicação da Kryptex,
  NiceHash): com eles abertos, desfazem o que o DoriMiner aplica.
- **Sem garantia.** É software de teste, fornecido como está.

## O que o DoriMiner nunca faz

- Pedir a seed, chaves privadas ou chaves de exchange. Só usa o **endereço público** da carteira.
- Cobrar taxas escondidas. Os miners que ele instala (PeakMiner, Rigel, BzMiner, WildRig, XMRig, SRBMiner)
  são de terceiros e têm as taxas que os autores anunciam.
- Abrir o teu computador à internet. A página só responde no próprio computador.
- Executar miners de origem desconhecida: só os de uma lista aprovada, descarregados das páginas dos
  autores e conferidos por checksum.

## Para quem testa numa rig com várias placas

Há uma [folha de teste](FOLHA-DE-TESTE-RIG.md) de cerca de 20 minutos, com o que fazer e o que fotografar.

## Dizer o que correu mal

Abre uma [issue](../../issues) com o que aconteceu, o que esperavas, as placas e o sistema. Ajuda muito o
relatório da máquina: na página, separador **Hardware** > **Criar relatório para enviar** (não tem
carteiras nem tokens). **Nunca publiques o endereço com o token da tua página nem seeds.**

## Sobre este repositório

Aqui ficam só os instaladores e estas instruções. O código-fonte não está publicado, por agora. Podes
descarregar e usar o DoriMiner para o experimentar; não o redistribuas modificado nem com outro nome.
