# Contador de LEDs  

Na atividade anterior, construímos um simples **Blink**, que fazia um LED do kit FPGA piscar. Agora, vamos dar um passo adiante: nesta atividade, você trabalhará com **múltiplos LEDs**.  

## Atividade  

Seu objetivo é escrever um módulo Verilog chamado **LedCounter**, que deve:  

- Ter um **parâmetro** chamado `CLK_FREQ`, que representa a frequência do clock.  
- Ter como **entradas** os sinais `clk` (clock) e `rst_n` (reset ativo em nível baixo).  
- Ter como **saída** um sinal de 8 bits chamado `leds`.  

O comportamento esperado do módulo é simples: ele deve implementar um **contador de 8 bits**, exibindo seu valor nos LEDs. Esse contador deve:  

- **Incrementar a cada 1 segundo**, utilizando `CLK_FREQ` como referência.  
- **Iniciar com valor 0** quando `rst_n` estiver acionado.  

### Código inicial  

Como ponto de partida, utilize o esqueleto de código abaixo:  

```verilog
module LedCounter #(
    parameter CLK_FREQ = 25_000_000
) (
    input  wire clk,
    input  wire rst_n,
    output wire [7:0] leds
);

endmodule
```

## Entrega

Primeiro, faça o *push* do seu código no repositório do **GitHub Classroom** para que o código seja carregado na placa. Veja o comportamento no site [embarcatechfpga.lsc.ic.unicamp.br](https://embarcatechfpga.lsc.ic.unicamp.br). Se tiver dúvidas de como utilizar a infraestrutura, veja este guia [aqui](guia_remoto.md).

Depois, confira o sistema de correção automática, que irá validar sua implementação e atribuir uma nota com base nos testes.

> **Dica:**  
Não altere os arquivos de correção! Para entender como os testes funcionam, consulte o script `run.sh` disponível no repositório.
