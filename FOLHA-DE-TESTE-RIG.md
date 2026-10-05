# Folha de teste: rig com várias placas (Windows)

Para quem tem uma rig com várias placas NVIDIA e pouco tempo. São cerca de 20 minutos. O objetivo é
confirmar duas coisas que ainda não foram vistas em hardware: que o DoriMiner **mexe na placa certa**
quando há várias, e **qual é o sensor da temperatura da memória** em cada modelo.

Em cada passo: tira uma fotografia (ou captura de ecrã) ao que aparece. No fim envia as fotografias e
o ficheiro do passo 7. Se alguma coisa parecer errada, **para e envia o que tens**: não insistas.

## Antes de começar

1. **Fecha os outros programas que mexem nas placas ou que mineram** (MSI Afterburner, HiveOS/outro
   gestor, a aplicação da Kryptex, NiceHash) e tira-os do arranque do Windows durante o teste.
2. Descompacta `DoriMiner-windows-….zip` numa pasta do disco (não dentro do zip).
3. Dois cliques em `DoriMiner.cmd`. Se o Windows mostrar "O Windows protegeu o seu PC": **Mais
   informações > Executar assim mesmo**. Quando perguntar se abre como administrador, responde **S**
   (sem isso não há limite de potência, ventoinhas nem overclock).
4. Se o antivírus apagar um miner mais à frente, o DoriMiner diz que pasta acrescentar às exclusões.

## Os passos

| # | O que fazer | O que fotografar |
|---|---|---|
| 1 | Separador **Hardware**. | A lista das placas (nome, temperatura, ventoinhas, "Temp. da memória"). |
| 2 | Em **Hardware**, carrega em **Testar as placas** e espera 2 a 3 minutos. As ventoinhas vão ao máximo, uma placa de cada vez: é normal. | O cartão "Teste das placas" no fim (a tabela com certo / ERRADO / não testado). |
| 3 | Numa das placas carrega em **Identificar** e vê na rig qual acelera durante 10 segundos. Repete para outra. | Só dizer: "a GPU 2 do DoriMiner é a 3.ª placa a contar da esquerda", por exemplo. |
| 4 | Separador **Resumo** > **Começar: criar o primeiro perfil**. Moeda Pearl (ou a que costumas minerar), a tua pool, **o teu endereço público**. Deixa instalar o miner e carrega em **Iniciar agora**. Espera 3 minutos. | O cartão do perfil a minerar (hashrate, temperaturas, shares) e o separador **Hardware** com todas as placas a trabalhar. |
| 5 | No cartão do perfil, **Editar**: liga "Limitar a potência de cada placa" e baixa uns 20 W; em Ventoinhas escolhe **Curva por temperatura**; **Guardar e reiniciar**. Espera 2 minutos. | O separador **Hardware**: os limites de potência e as ventoinhas de todas as placas. |
| 6 | Com a rig a minerar há pelo menos 5 minutos, abre outro programa que mostre a temperatura da memória (HWiNFO, ou o que usares) **só para ler**. | Lado a lado: a "Temp. da memória" do DoriMiner e a do outro programa, para 2 ou 3 placas. Se o DoriMiner disser "sem leitura", fotografa na mesma. |
| 7 | **Hardware** > **Criar relatório para enviar** (1 a 2 minutos, pode ser com a rig a minerar). | Envia o ficheiro que ele indica (`data\doctor-….json`). Não tem carteiras nem tokens. |
| 8 | **Parar** no cartão do perfil. | O separador **Hardware** um minuto depois: os limites de potência voltaram ao de fábrica? |

## Se houver tempo

- **Um perfil só para algumas placas:** em Editar, na secção "Placas", desmarca metade. Guardar,
  iniciar, e fotografar o Hardware: só as marcadas trabalham?
- **Afinar placa:** com o perfil parado, botão **Benchmark** > "Afinar placa". Demora uns 20 minutos;
  no fim fotografar as sugestões.
- **Telemóvel:** com o Tailscale no PC da rig e no telemóvel, **Definições > Máquinas e telemóvel > Acesso remoto**.

## O que dizer no fim

- Que placas são (marca e modelo de cada uma, pela ordem física) e que versão do Windows.
- O que foi confuso, o que demorou, e o que esperavas ver e não viste.
- Qualquer mensagem de erro, tal como apareceu.
