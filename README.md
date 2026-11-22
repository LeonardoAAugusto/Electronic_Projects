# Micromouse - Eletrônica e Controle

Subsistema de eletrônica embarcada, alimentação, sensoriamento, acionamento de motores e firmware de baixo nível para o robô Micromouse.

## Visão Geral

Descrição do papel da eletrônica no robô: leitura de sensores de parede e odometria, execução da malha de controle e comando dos atuadores para navegação e solução de labirinto.

## Arquitetura de Hardware

- **MCU:** modelo, clock e interfaces utilizadas (GPIO, ADC, PWM, I2C, SPI, UART, timers/quadrature encoders).
- **Alimentação:** faixa de tensão da bateria, reguladores (buck/boost/LDO), trilhos de potência e lógica, proteção contra inversão de polaridade e consumo médio/de pico.
- **Sensores:** sensores de distância/parede (IR, ToF, etc.), encoders de roda e IMU (se aplicável), incluindo endereçamento ou canais de leitura.
- **Acionamento de Motores:** driver de ponte H, motores DC/com encoders, limites de corrente e frequência de PWM.
- **PCB e Pinagem:** referência ao projeto de placa (esquemático, Gerber, BOM) e tabela ou mapa de pinos atualizado.

## Firmware e Controle

- **Ambiente de Desenvolvimento:** compilador, framework ou IDE (ex.: PlatformIO, VS Code, SDK do fabricante).
- **Módulos Principais:**
  - Leitura e filtragem de sensores
  - Odometria e estimativa de posição/velocidade
  - Controle de velocidade e alinhamento/centralização (ex.: PID)
  - Interface de depuração (serial/telemetria, LEDs, botões)
- **Estrutura do Repositório:**
  - `hardware/` — esquemáticos, layout de PCB, lista de materiais (BOM) e pinagem
  - `firmware/` — código-fonte, bibliotecas locais e configuração de build
  - `docs/` — datasheets, registros de calibração e medições de bancada

## Montagem, Gravação e Calibração

1. Inspecionar soldas, trilhas, continuidade e ausência de curto entre alimentação e GND antes de conectar a bateria.
2. Conferir níveis lógicos (3.3 V / 5 V) e polaridade de sensores, encoders e driver de motores.
3. Compilar e gravar o firmware no microcontrolador.
4. Calibrar leituras dos sensores de parede, offset/escala dos encoders e ganhos da malha de controle.

## Testes e Validação

- **Bancada:** medição de tensões reguladas, corrente em repouso e sob carga, aquecimento de reguladores e drivers, e verificação de sinais PWM/encoders.
- **Pista / Labirinto:** repetibilidade de leitura, resposta em curvas, estabilidade de controle em diferentes velocidades e autonomia.
- **Limitações Conhecidas:** saturação de sensores, ruído elétrico, limitações de tração ou pontos em aberto para revisão de hardware/firmware.

## Referências e Licença

Datasheets dos componentes, notas de aplicação, bibliotecas utilizadas e licença do projeto.
