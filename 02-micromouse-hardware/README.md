# Arquitetura de Hardware - Robo Micromouse

Projeto de esquematico desenvolvido no KiCad para a eletrônica de um robo autonomo do tipo Micromouse[cite: 2].

## Principais Blocos e Componentes

- Microcontrolador: ESP32-WROOM-32D[cite: 2].
- Sensoriamento de distancia: tres sensores a laser VL53L0X conectados ao barramento I2C, utilizando pinos XSHUT para controle de habilitacao e enderecamento individual[cite: 2].
- Acionamento de motores: driver de ponte H dupla TB6612FNG para micromotores DC com encoder (750 RPM)[cite: 2].
- Alimentacao e monitoramento: conversor DC-DC buck para geracao de barramento regulado a partir de bateria de 7,4 V e circuito de leitura de tensao da bateria[cite: 2].

## Arquivos na Pasta

- Esquemático em PDF/imagem e arquivos do projeto no KiCad[cite: 2].
