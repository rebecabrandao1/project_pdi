# Projeto -- Bottles

## Introdução

O link em anexo contém 77 imagens de garrafas. Cada garrafa (no centro da imagem) pode possuir um ou mais dos seguintes 8 defeitos:

1. CONTENT_HIGH,
1. CONTENT_LOW,
1. COVER_NONE,
1. BOTTLE_SMASHED,
1. LABEL_WHITE,
1. LABEL_MISPLACED,
1. LABEL_NONE,
1. BOTTLE_NONE.

Cada discente deverá submeter 1 arquivo do tipo 'notebook' (<nome do indivíduo>.ipynb) contendo **uma função** que receba uma imagem (array numpy) e entregue um array (numpy) contendo 8 valores. Cada valor deve ser:
- **0** (para **ausência** do defeito correspondente), ou;
- **1** (para **presença** do defeito correspondente).

### Exemplo:
- A imagem ```train_1.jpg``` não possui defeitos, portanto, o resultado da inspeção deve ser um array numpy contendo 8 zeros:
```
array([0., 0., 0., 0., 0., 0., 0., 0.])
```
- Já a imagem ```train_4.jpg``` possui 2 defeitos; ```CONTENT_HIGH``` e ```COVER_NONE```, portanto, o resultado da inspeção deve ser um array (numpy) como o que segue:
```
array([1., 0., 1., 0., 0., 0., 0., 0.])
```



## Resolução
Para cada um dos problemas que poderiam ser apresentados para a garrafa existe uma solução:
Para a verificação do nível existe um true or false;
Para a verficação da integridade da garrafa existe um "Garrafa inteira" ou "garrafa quebrada" usando a detecção de bordas e de contorno;
