# Global-Solution
Trabalho Gs
Este projeto utiliza um display LCD 16x2 e sensores de tensão e corrente para medir e exibir o consumo instantâneo de energia, além de calcular a média de consumo diário. O código está implementado para rodar em uma placa Arduino e foi projetado para monitorar o consumo elétrico em uma carga conectada aos pinos de entrada analógica.

Componentes Necessários
Arduino (Uno, Mega ou similar)
Display LCD 16x2 (com interface I2C ou paralela)
Sensor de Tensão (conectado ao pino A1)
Sensor de Corrente (conectado ao pino A3)
Potenciômetro (se aplicável para ajuste de corrente)
Resistores e fios para conexões
Descrição do Código
O código realiza as seguintes funções:

Leitura de Tensão e Corrente:

A tensão é lida através do sensor conectado ao pino A1 do Arduino.
A corrente é lida através do sensor conectado ao pino A3.
Cálculo de Potência Instantânea:

A potência instantânea é calculada multiplicando a tensão (em Volts) pela corrente (em Amperes) usando a função PotInst(). O valor é exibido no display LCD.
Exibição no LCD:

O valor da tensão e corrente são exibidos no display LCD.
A potência instantânea (em Watts) é atualizada a cada 5 segundos.
Cálculo do Consumo Diário:

A cada 7 medições de potência (aproximadamente 35 segundos), o consumo médio em Watt-hora (Wh) é calculado e exibido no LCD.
O valor do consumo médio também é impresso no monitor serial para monitoramento em tempo real.
Comando de Controle (Opcional):

O pino 8 pode ser usado para controle de um dispositivo, como um relé, com base no valor da leitura de corrente.
Como Usar
Carregue o código no seu Arduino.
Conecte os sensores de tensão e corrente nas portas apropriadas (A1 e A3).
Conecte o display LCD nos pinos especificados (12, 11, 5, 4, 3, 2).
Abra o Monitor Serial no IDE do Arduino para visualizar os dados de consumo.
O LCD irá exibir a tensão, corrente, potência instantânea e o consumo médio em Wh.

Considerações Finais
Este projeto é ideal para medir e monitorar o consumo de energia em sistemas simples. Você pode adaptar o código para controlar dispositivos com base no consumo de energia ou para integrar com outros sistemas de automação.
