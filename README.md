# HEARTBEAT

Data logger para o monitoramento de condições ambientais em espaços controlados, feito com o Arduino.

## Descrição

Implementação de um dispositivo de registro de dados (data logger) dedicado ao monitoramento da temperatura, umidade e luminosidade do ambiente, voltado para uso em ambientes controlados, como uma adega de vinhos. O projeto foi elaborado para aplicação no Arduino Uno R3, sendo um trabalho para a disciplina de Sistemas Embarcados do curso de Engenharia de Computação.

## Participantes

- Henrique Alves Ferreira
- Gabriel Melo Santos
- Matheus da Silva Souza
- Pedro Henrique Simões Reys
- Rafael Ruppert Barrocal

## Expecificações Técnicas

### Componentes Utilizados

- Arduino Uno R3;
- LDR + Resistor 10kOhm;
- DHT11;
- LED RGB;
- Buzzer;
- Tela LCD 16x2 com entrada I2C;
- RTC;
- 2 botões;

### Diagrama Elétrico


## Manual de Operação

Ao ligar o dispositivo, as condições do ambiente são medidas. Se alguma delas estiver fora do padrão, é exibido um aviso na tela com uma alerta sonoro. Seguem as faixas de condição padrão:

- Temperatura: T > 15°C; T < 25°C;
- Umidade: U > 30%; U < 50%;
- Luminosidade: L < 30%;

Em seguida são exibidos cada um dos dados registrados pelos sensores; Depois, o dispositivo segue em loop, sempre medindo, alertando e exibindo os dados.

### Configurações
Manter o botão 2 pressionado até o início do próximo loop entra nas **configurações** de **luminosidade** e **unidade de temperatura**. Ambas podem ser ignoradas apertando o botão 2 para cada uma.

#### Luminosidade
Após o carregamento da tela, o dispositivo pergunta se o usuário deseja ajustar as definições de luminosidade mínima e máxima, com base nas quais se determina a porcentagem de luz. Para aceitar, deve-se apertar o botão 1; para recusar e pular para a próxima config., deve-se apertar o botão 2. 

Na definição de luminosidade, o dispositivo primeiro pede a lum. mínima. O usuário pode colocar o sensor em um ambiente escuro, e então apertar o botão 1 para registrar as luminosidade como mínima. Depois disso o usuário deve fazer o mesmo com a lum. máxima, pondo o sensor em ambiente iluminado e apertando o botão 1 para registrar.

#### Unidade de Temperatura
Terminada a definição da luminosidade, ou tendo-na pulado com o botão 2, segue-se para a definição da unidade de temperatura. O dispositivo pergunta se o usuário deseja converter a temperatura entre as unidades de graus fahrenheit e graus celsius. Apertando o botão 1, a temperatura passará a ser exibida em °F se antes estava em °C, e vice-versa. O usuário também pode pular essa definição e voltar ao loop apertando o botão 2;