# Backups S7 - Projetos STEP 7

Repositório de backups de projetos **SIMATIC STEP 7** para testes de automação industrial com CLPs Siemens S7-300.

## 📋 Sobre

Este repositório contém configurações de teste para integração de sistemas de automação industrial, incluindo comunicação com inversores de frequência e módulos de I/O remotos via PROFIBUS-DP.

## 🗂️ Projetos

### MX_CPU_2
**Configuração de teste: S7-300 315-2DP + Sinamics S120 CU310**

- **Objetivo:** Teste de comunicação e acionamento de inversor
- **CLP:** SIEMENS S7-300 CPU 315-2DP
- **Dispositivo:** Inversor Sinamics S120 CU310
- **Protocolo:** PROFIBUS-DP
- **Inclui:**
  - Configuração de rede PROFIBUS
  - Parâmetros de comunicação
  - Setup de hardware
  - Metadados para testes de integração

### S7_Pro4
**Configuração de teste: Entradas Analógicas via ET200**

- **Objetivo:** Aquisição de sinais analógicos
- **CLP:** SIEMENS S7-300 CPU 315-2DP
- **Módulos:**
  - ET200 (153-2BA02-0XB0) - Acoplador remoto
  - 331-1KF01-0AB0 - Módulo de entrada analógica
- **Protocolo:** PROFIBUS-DP
- **Inclui:**
  - Configuração de I/O remoto
  - Setup de rede PROFIBUS
  - Parâmetros de aquisição analógica

### S7_Pro5
**Configuração de teste: Saídas Analógicas com Calibração**

- **Objetivo:** Teste e calibração de saídas analógicas
- **CLP:** SIEMENS S7-300 CPU 315-2DP
- **Módulo:** 332-5HF00-0AB0 - Módulo de saída analógica
- **Protocolo:** PROFIBUS-DP
- **Calibração com valores fixos de tensão:**
  - +10V: PQW256 (27648 DEC / 0x6C00 HEX)
  - +5V: PQW258 (13824 DEC / 0x3600 HEX)
  - 0V: PQW260 (0 DEC / 0x0000 HEX)
  - -5V: PQW262 (-13824 DEC / 0xC9C0 HEX)
  - -10V: PQW264 (-27648 DEC / 0x9400 HEX)
  - Duplicação de valores em PQW266-PQW270 para múltiplos canais
- **Inclui:**
  - Configuração de saídas analógicas
  - Tabela de variáveis de calibração
  - Setup de rede PROFIBUS
  - Parâmetros para testes de integração

### S7_Pro6
**Configuração de teste: Entradas Analógicas Mistas (Tensão e Corrente)**

- **Objetivo:** Aquisição de sinais analógicos mistos (tensão e corrente)
- **CLP:** SIEMENS S7-300 CPU 315-2DP
- **Módulo:** 6ES7331-7KF02-0AB0 - Módulo de entrada analógica
- **Protocolo:** PROFIBUS-DP
- **Sinais de teste aplicados:**
  - Tensão: 0-10V
  - Corrente: 0-20mA
- **Inclui:**
  - Configuração de entrada analógica
  - Parâmetros de conversão A/D
  - Setup de rede PROFIBUS
  - Suporte para medições simultâneas de tensão e corrente

## 🔧 Tecnologias

- **Software:** SIMATIC STEP 7 v5.7
- **Hardware:** 
  - Siemens S7-300 (CPU 315-2DP)
  - Sinamics S120 CU310
  - ET200 (153-2BA02-0XB0)
  - Módulos 331-1KF01-0AB0 (entrada), 332-5HF00-0AB0 (saída) e 6ES7331-7KF02-0AB0 (entrada mista)
- **Protocolo:** PROFIBUS-DP

## 🚀 Como Usar

1. Abra o **SIMATIC Manager** (STEP 7 v5.x)
2. Vá em `File` → `Open Project`
3. Navegue até a pasta do projeto desejado
4. Selecione o arquivo `.s7p`
5. Configure a comunicação com o hardware real ou simulador

## ⚠️ Requisitos

- SIMATIC STEP 7 v5.5 ou superior
- Conhecimento em programação de CLPs Siemens
- Hardware compatível ou simulador (PLCSIM)

## 📝 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 👤 Autor

**MX Drives**
- Email: fernando@mxdrive.com.br

---

*Última atualização: 1º de dezembro de 2025*
