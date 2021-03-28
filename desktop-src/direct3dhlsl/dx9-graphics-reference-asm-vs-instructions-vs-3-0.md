---
title: Istruzioni-vs_3_0
description: Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione 3 \_ 0.
ms.assetid: 2309a643-dec8-4f2a-a217-e7f1e90b5f43
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f134c47f5697381c211808ce5a46ab5ee23031b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955616"
---
# <a name="instructions---vs_3_0"></a>Istruzioni-vs \_ 3 \_ 0

Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione 3 \_ 0.

Sono disponibili diversi tipi di istruzioni vertex shader, come illustrato nella tabella. Le colonne a destra indicano quanto segue:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: istruzioni non aritmetiche. Ogni shader deve avere un'istruzione version e deve essere la prima istruzione.
-   Aritmetico: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni supportano la ricerca dell'indirizzo della trama.
-   Controllo di flusso: queste istruzioni aggiungono il controllo di flusso, ad esempio cicli, ripetizioni e [if bool-vs](if-bool---vs.md)... [altrimenti](else---vs.md)... confronti [endif](endif---vs.md) .
-   Novità: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                                           | Descrizione                                                                                                                                                            | Slot di istruzioni | Configurazione | Aritmetico | Trama | Controllo di flusso | Nuova |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-vs](abs---vs.md)                                                       | Valore assoluto                                                                                                                                                         | 1                 |       | x          |         |              |     |
| [Aggiungi-vs](add---vs.md)                                                       | Aggiungere due vettori                                                                                                                                                        | 1                 |       | x          |         |              |     |
| [Break-vs](break---vs.md)                                                   | Interrompi un [ciclo-vs](loop---vs.md)... [EndLoop-vs](endloop---vs.md) o [Rep](rep---vs.md)... blocco [endrep](endrep---vs.md)                                  | 1                 |       |            |         | x            |     |
| [Interrompi \_ comp-vs](break-comp---vs.md)                                        | Interrompi in modo condizionale da un [ciclo-vs](loop---vs.md)... [EndLoop-vs](endloop---vs.md) o [Rep](rep---vs.md)... blocco [endrep](endrep---vs.md) con confronto | 3                 |       |            |         | x            |     |
| [Breakp-vs](breakp---vs.md)                                                 | Interrompi un [ciclo-vs](loop---vs.md)... [EndLoop-vs](endloop---vs.md) o [Rep](rep---vs.md)... blocco [endrep](endrep---vs.md) , basato su un predicato            | 3                 |       |            |         | x            |     |
| [Call-vs](call---vs.md)                                                     | Chiamare una subroutine                                                                                                                                                      | 2                 |       |            |         | x            |     |
| [callnz bool-vs](callnz-bool---vs.md)                                       | Chiamare una subroutine se un registro booleano non è zero                                                                                                                    | 3                 |       |            |         | x            |     |
| [callnz Predator-vs](callnz-pred---vs.md)                                       | Chiamare una subroutine se un registro predicato non è zero                                                                                                                  | 3                 |       |            |         | x            |     |
| [CRS-vs](crs---vs.md)                                                       | Prodotto incrociato                                                                                                                                                          | 2                 |       | x          |         |              |     |
| [\_input utilizzo DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Dichiarare i registri vertici di input (vedere [registri-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md))                                                        | 0                 | x     |            |         |              |     |
| [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)                    | Dichiarare la dimensione di trama per un campionatore                                                                                                                            | 0                 | x     |            |         |              | x   |
| [def-vs](def---vs.md)                                                       | Definisci costanti                                                                                                                                                       | 0                 | x     |            |         |              |     |
| [defb-vs](defb---vs.md)                                                     | Dichiarare una costante booleana                                                                                                                                             | 0                 | x     |            |         |              |     |
| [defi-vs](defi---vs.md)                                                     | Dichiarare una costante Integer                                                                                                                                            | 0                 | x     |            |         |              |     |
| [DP3-vs](dp3---vs.md)                                                       | Prodotto dot a tre componenti                                                                                                                                            | 1                 |       | x          |         |              |     |
| [DP4-vs](dp4---vs.md)                                                       | Prodotto a quattro componenti                                                                                                                                             | 1                 |       | x          |         |              |     |
| [DST-vs](dst---vs.md)                                                       | Distanza                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [else-vs](else---vs.md)                                                     | Inizia un blocco [else](else---vs.md)                                                                                                                                   | 1                 |       |            |         | x            |     |
| [endif-vs](endif---vs.md)                                                   | Termina [se bool-vs](if-bool---vs.md)... blocco [else](else---vs.md)                                                                                                  | 1                 |       |            |         | x            |     |
| [endloop-vs](endloop---vs.md)                                               | Fine di un blocco [loop-vs](loop---vs.md)                                                                                                                              | 2                 |       |            |         | x            |     |
| [endrep-vs](endrep---vs.md)                                                 | Fine di un blocco di ripetizione                                                                                                                                                  | 2                 |       |            |         | x            |     |
| [exp-vs](exp---vs.md)                                                       | Precisione completa 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |         |              |     |
| [exp-vs](exp---vs.md)                                                       | Precisione parziale 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |         |              |     |
| [FRC-vs](frc---vs.md)                                                       | Componente frazionario                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [Se bool-vs](if-bool---vs.md)                                               | Inizia un blocco [if bool-vs](if-bool---vs.md) (usando una condizione booleana)                                                                                            | 3                 |       |            |         | x            |     |
| [Se \_ comp-vs](if-comp---vs.md)                                              | Inizia un blocco [if bool-vs](if-bool---vs.md) con un confronto                                                                                                     | 3                 |       |            |         | x            |     |
| [Se prede-vs](if-pred---vs.md)                                               | Inizia un blocco [if bool-vs](if-bool---vs.md) con una condizione del predicato                                                                                             | 3                 |       |            |         | x            |     |
| [etichetta-vs](label---vs.md)                                                   | Etichetta                                                                                                                                                                  | 0                 |       |            |         | x            |     |
| [Lit-vs](lit---vs.md)                                                       | Calcola illuminazione                                                                                                                                                     | 3                 |       | x          |         |              |     |
| [log-vs](log---vs.md)                                                       | ₂ di log con precisione completa (x)                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [LogP-vs](logp---vs.md)                                                     | ₂ di log con precisione parziale (x)                                                                                                                                              | 1                 |       | x          |         |              |     |
| [ciclo-vs](loop---vs.md)                                                     | Ciclo                                                                                                                                                                   | 3                 |       |            |         | x            |     |
| [LRP-vs](lrp---vs.md)                                                       | Interpolazione lineare                                                                                                                                                   | 2                 |       | x          |         |              |     |
| [M3X2-vs](m3x2---vs.md)                                                     | 3x2 Multiply                                                                                                                                                           | 2                 |       | x          |         |              |     |
| [M3X3-vs](m3x3---vs.md)                                                     | moltiplicazione 3x3                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 Multiply                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 Multiply                                                                                                                                                           | 3                 |       | x          |         |              |     |
| [M4x4-vs](m4x4---vs.md)                                                     | moltiplicazione 4x4                                                                                                                                                           | 4                 |       | x          |         |              |     |
| [MAD-vs](mad---vs.md)                                                       | Moltiplica e Aggiungi                                                                                                                                                       | 1                 |       | x          |         |              |     |
| [Max-vs](max---vs.md)                                                       | Massimo                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [min-vs](min---vs.md)                                                       | Minima                                                                                                                                                                | 1                 |       | x          |         |              |     |
| [MOV-vs](mov---vs.md)                                                       | Spostamento                                                                                                                                                                   | 1                 |       | x          |         |              |     |
| [mova-vs](mova---vs.md)                                                     | Spostare i dati da un registro a virgola mobile a un registro Integer                                                                                                        | 1                 |       | x          |         |              |     |
| [Mul-vs](mul---vs.md)                                                       | Moltiplicazione                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [NOP-vs](nop---vs.md)                                                       | Nessuna operazione                                                                                                                                                           | 1                 |       | x          |         |              |     |
| [NRM-vs](nrm---vs.md)                                                       | Normalizzare                                                                                                                                                              | 3                 |       | x          |         |              |     |
| [POW-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |         |              |     |
| [RCP-vs](rcp---vs.md)                                                       | Reciproco                                                                                                                                                             | 1                 |       | x          |         |              |     |
| [Rep-vs](rep---vs.md)                                                       | Repeat                                                                                                                                                                 | 3                 |       |            |         | x            |     |
| [RET-vs](ret---vs.md)                                                       | Fine di una subroutine                                                                                                                                                    | 1                 |       |            |         | x            |     |
| [RSQ-vs](rsq---vs.md)                                                       | Radice quadrata reciproca                                                                                                                                                 | 1                 |       | x          |         |              |     |
| [setp \_ comp-vs](setp-comp---vs.md)                                          | Impostare il registro del predicato                                                                                                                                             | 1                 |       |            |         | x            |     |
| [SGE-vs](sge---vs.md)                                                       | Confronto maggiore o uguale a                                                                                                                                          | 1                 |       | x          |         |              |     |
| [SGN-vs](sgn---vs.md)                                                       | Sign                                                                                                                                                                   | 3                 |       | x          |         |              |     |
| [SinCos-vs](sincos---vs.md)                                                 | Seno e coseno                                                                                                                                                        | 8                 |       | x          |         |              |     |
| [SLT-vs](slt---vs.md)                                                       | Minore di compare                                                                                                                                                      | 1                 |       | x          |         |              |     |
| [Sub-vs](sub---vs.md)                                                       | Sottrazione                                                                                                                                                               | 1                 |       | x          |         |              |     |
| [texldl-vs](texldl---vs.md)                                                 | Carico di trama con livello di dettaglio regolabile dall'utente                                                                                                                      | Vedere la nota 1        |       |            | x       |              | x   |
| [vs](vs---vs.md)                                                              | Versione                                                                                                                                                                | 0                 | x     |            |         |              |     |



 

Note:

-   Se la trama è una mappa cubo, slot = 5; in caso contrario, slot = 2

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




