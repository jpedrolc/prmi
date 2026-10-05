# PRMI — Interface modular prevista

As interfaces abaixo são propostas de projeto; a implementação e a validação física estão pendentes.

## Base e módulo inicial

A base R/C prevista combina tração e bateria central. O módulo inicial previsto é uma garra com servos, fixada em uma interface comum e alimentada pela base. Os canais auxiliares do receptor comandariam um Arduino Nano ou ESP32, que acionaria o módulo.

O primeiro MVP previsto é teleoperado. Navegação autônoma e coordenação de frota ficam fora desse escopo.

## Interface mecânica

A proposta usa um trilho tipo rabo de andorinha com trava. Os contatos elétricos seriam alinhados pelo encaixe; pogo pins e conectores JST aparecem como alternativas no planejamento.

Ainda faltam CAD, tolerâncias, retenção sob vibração, capacidade de carga e testes de ciclos de conexão. Não há arquivos STL publicados.

## Alimentação e sinais

O conceito prevê derivar energia da bateria central para o módulo, com proteção e regulação. O planejamento menciona barramentos de 5 V e 12 V, mas estes não constituem uma especificação elétrica fechada.

Antes da montagem, é necessário definir:

- Química e faixa de tensão da bateria, incluindo estado carregado e descarregado.
- Correntes de partida, operação e bloqueio de motores/servos.
- Conversores e proteções compatíveis com essas cargas.
- Capacidade dos contatos, cabos e conectores.
- Pinagem, referências de GND e separação entre potência e sinais.

Não foi publicada uma pinagem final nem um circuito reproduzível.

## Troca de módulos

Troca mecânica rápida e conexão elétrica energizada são requisitos distintos. A meta de hot-swap depende de proteção contra curto, transientes e contato parcial durante o encaixe; não está demonstrada.

A identificação automática por resistor é uma extensão proposta, ainda não implementada.

## Evidências necessárias

O primeiro conjunto de resultados deve registrar tensão sob carga, reinicializações, aquecimento e falhas da interface. Depois, avaliar autonomia da bateria e tempo de troca em condições documentadas.

As metas descritas no planejamento são objetivos de ensaio, não resultados obtidos.
