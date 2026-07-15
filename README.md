# Fundamentos de Cloud AWS — Gerenciamento de Instâncias EC2

Repositório criado como entrega do desafio de projeto do bootcamp Fundamentos de Cloud AWS da DIO.

## 🎯 Objetivo do Desafio

Consolidar os conhecimentos adquiridos sobre gerenciamento de instâncias EC2 (Elastic Compute Cloud) na AWS, documentando o processo, os conceitos aprendidos e os principais insights obtidos durante a prática.

## 📚 Sobre o Amazon EC2

O Amazon EC2 é o serviço de computação em nuvem da AWS que permite provisionar servidores virtuais (instâncias) sob demanda, com capacidade escalável, sem a necessidade de investir em hardware físico.

**Principais conceitos abordados**

- **Instância EC2** :Pense na nuvem como um grande data center que a AWS administra para você. Uma instância EC2 é o pedaço desse data center que você reserva pra si — um computador virtual completo, com processador, memória e disco, que você liga, usa e desliga quando quiser. O conceito central aqui é a virtualização: em vez de comprar uma máquina física, você aluga um recurso computacional sob demanda.
- **AMI (Amazon Machine Image)** :Antes de ligar a instância, ela precisa de um sistema operacional e, talvez, alguns programas já instalados. A AMI é justamente esse ponto de partida — um "retrato" congelado de um sistema pronto para uso. O conceito importante aqui é a reprodutibilidade: a mesma AMI pode gerar dezenas de instâncias idênticas, o que é essencial quando você precisa escalar uma aplicação rapidamente.
- **Tipo de instância** :Cada tipo de instância representa uma combinação de poder computacional (CPU, RAM, rede). A ideia central é o dimensionamento sob medida: você não paga por uma máquina genérica, mas escolhe a que melhor se encaixa na carga de trabalho. Uma família t é voltada a uso geral e custo baixo; uma família c é otimizada para processamento pesado. É o mesmo raciocínio de escolher entre um carro econômico ou um caminhão, dependendo da carga que você vai transportar.
- **Par de chaves (Key Pair)** :Esse é um conceito de criptografia assimétrica aplicado à segurança de acesso. Em vez de uma senha (que pode ser descoberta ou vazada), você usa duas chaves matematicamente relacionadas: uma pública, que fica na instância, e uma privada, que só você possui. Só quem tem a chave privada consegue "abrir a porta". É mais seguro porque a chave privada nunca precisa ser transmitida pela rede.
- **Security Group** :Este é o conceito de controle de acesso por regras explícitas — um firewall que trabalha com a lógica de "tudo bloqueado por padrão, libere apenas o necessário". Você define quais portas (SSH, HTTP, HTTPS) e quais origens de IP podem se comunicar com a instância. É o princípio do menor privilégio: expor só o que é estritamente necessário reduz a superfície de ataque.
- **Elastic IP** :Normalmente, o IP público de uma instância é dinâmico — muda a cada reinicialização. O Elastic IP resolve esse problema de persistência de identidade na rede: é um endereço fixo que você associa à instância e mantém, mesmo que ela seja desligada e ligada novamente. É útil quando outros sistemas (como um domínio DNS) precisam sempre encontrar o mesmo endereço.
- **Camada gratuita (Free Tier)** :É o modelo da AWS para reduzir a barreira de entrada de quem está aprendendo. O conceito por trás é simples: um "orçamento" limitado de uso gratuito (geralmente 750 horas/mês de instâncias pequenas, por 12 meses) para você experimentar o serviço sem custo, entendendo na prática o modelo de pagamento sob demanda que rege toda a nuvem — você paga pelo que usa, e o Free Tier é apenas uma cota inicial isenta dessa cobrança.


## 🛠️ O que foi praticado

1. **Criação da instância EC2**
- Escolha da AMI (ex: Amazon Linux, Ubuntu)
- Seleção do tipo de instância
- Configuração do par de chaves
- Configuração do Security Group (portas liberadas, ex: 22 para SSH, 80 para HTTP)
2. **Conexão com a instância**
- Conexão via SSH (terminal) ou via navegador (EC2 Instance Connect)
3. **Gerenciamento da instância**
- Iniciar, parar e reiniciar a instância
- Monitoramento básico (CPU, status checks)
4. **Encerramento dos recursos**
- Encerrar (terminate) a instância para evitar cobranças indevidas

---
📌 Desafio realizado como parte do bootcamp Fundamentos de Cloud AWS promovido pela DIO.
