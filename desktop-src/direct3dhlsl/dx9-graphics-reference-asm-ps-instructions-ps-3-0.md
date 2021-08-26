---
title: ps_3_0 istruzioni
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 3 \_ 0.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e44d13bfc726830a8c3fb770b34d5563fde2684f5c8bdf3fea54dec2312af4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982861"
---
# <a name="ps_3_0-instructions"></a>Ps \_ 3 \_ 0 Istruzioni

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 3 \_ 0.

Esistono diversi tipi di istruzioni pixel shader, come illustrato nella tabella. Le colonne a destra sono le seguenti:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: un pixel shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetica: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni vengono usate per caricare e campionare i dati delle trame e per modificare le coordinate della trama.
-   Flow controllo dinamico: queste istruzioni forniscono il controllo di flusso statico e dinamico all'esecuzione delle istruzioni.
-   Nuovo: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                             | Descrizione                                                                          | Slot di istruzioni | Eseguire la configurazione | Aritmetico | Trama | Controllo di flusso | Nuovo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs - ps](abs---ps.md)                                         | Valore assoluto                                                                       | 1                 |       | x          |         |              |     |
| [add - ps](add---ps.md)                                         | Aggiungere due vettori                                                                      | 1                 |       | x          |         |              |     |
| [break - ps](break---ps.md)                                     | Interruzione di un ciclo... endloop o rep... endrep block                                  | 1                 |       |            |         | x            |     |
| [break \_ comp - ps](break-comp---ps.md)                          | Interruzione condizionale di un ciclo... endloop o rep... endrep block, con un confronto | 3                 |       |            |         | x            |     |
| [breakp - ps](break-p---ps.md)                                  | interruzione di un ciclo... endloop o rep... blocco endrep, basato su un predicato            | 3                 |       |            |         | x            |     |
| [call - ps](call---ps.md)                                       | Chiamare una subroutine                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool - ps](callnz-bool---ps.md)                         | Chiamare una subroutine se un registro booleano è diverso da zero                                  | 3                 |       |            |         | x            |     |
| [callnz pred - ps](callnz-pred---ps.md)                         | Chiamare una subroutine se un registro del predicato è diverso da zero                                | 3                 |       |            |         | x            |     |
| [cmp - ps](cmp---ps.md)                                         | Confrontare l'origine con 0                                                                  | 1                 |       | x          |         |              |     |
| [crs - ps](crs---ps.md)                                         | Prodotto incrociato                                                                        | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Dichiarare la dimensione della trama per un campionatore                                          | 0                 | x     |            |         |              |     |
| [Semantica dcl \_ (sm3 - ps asm)](dcl-usage---ps.md)              | Dichiarare registri di input e output                                                   | 0                 | x     |            |         |              | x   |
| [def - ps](def---ps.md)                                         | Definire costanti                                                                     | 0                 | x     |            |         |              |     |
| [defb - ps](defb---ps.md)                                       | Definire una costante booleana                                                            | 0                 | x     |            |         |              |     |
| [defi - ps](defi---ps.md)                                       | Definire una costante integer                                                           | 0                 | x     |            |         |              |     |
| [dp2add - ps](dp2add---ps.md)                                   | Prodotto punto 2D e aggiunta                                                               | 2                 |       | x          |         |              |     |
| [dp3 - ps](dp3---ps.md)                                         | Prodotto punto 3D                                                                       | 1                 |       | x          |         |              |     |
| [dp4 - ps](dp4---ps.md)                                         | Prodotto punto 4D                                                                       | 1                 |       | x          |         |              |     |
| [dsx - ps](dsx---ps.md)                                         | Frequenza di modifica nella direzione x                                                    | 2                 |       | x          |         |              |     |
| [dsy - ps](dsy---ps.md)                                         | Frequenza di modifica nella direzione y                                                    | 2                 |       | x          |         |              |     |
| [else - ps](else---ps.md)                                       | Iniziare un blocco else                                                                  | 1                 |       |            |         | x            |     |
| [endif - ps](endif---ps.md)                                     | Terminare un'operazione if... blocco else                                                               | 1                 |       |            |         | x            |     |
| [endloop - ps](endloop---ps.md)                                 | Terminare un ciclo                                                                           | 2                 |       |            |         | x            | x   |
| [endrep - ps](endrep---ps.md)                                   | Fine di un blocco di ripetizione                                                                | 2                 |       |            |         | x            |     |
| [exp - ps](exp---ps.md)                                         | Precisione completa 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [frc - ps](frc---ps.md)                                         | Componente frazionario                                                                 | 1                 |       | x          |         |              |     |
| [if bool - ps](if-bool---ps.md)                                 | Iniziare un blocco if                                                                    | 3                 |       |            |         | x            |     |
| [if \_ comp - ps](if-comp---ps.md)                                | Iniziare un blocco if con un confronto                                                  | 3                 |       |            |         | x            |     |
| [if pred - ps](if-pred---ps.md)                                 | Iniziare un blocco if con predicazione                                                   | 3                 |       |            |         | x            |     |
| [label - ps](label---ps.md)                                     | Etichetta                                                                                | 0                 |       |            |         | x            |     |
| [log - ps](log---ps.md)                                         | Log con precisione completa(x)                                                               | 1                 |       | x          |         |              |     |
| [loop - ps](loop---ps.md)                                       | Ciclo                                                                                 | 3                 |       |            |         | x            | x   |
| [lrp - ps](lrp---ps.md)                                         | Interpolazione lineare                                                                   | 2                 |       | x          |         |              |     |
| [m3x2 - ps](m3x2---ps.md)                                       | Moltiplicazione 3x2                                                                         | 2                 |       | x          |         |              |     |
| [m3x3 - ps](m3x3---ps.md)                                       | Moltiplicazione 3x3                                                                         | 3                 |       | x          |         |              |     |
| [m3x4 - ps](m3x4---ps.md)                                       | Moltiplicazione 3x4                                                                         | 4                 |       | x          |         |              |     |
| [m4x3 - ps](m4x3---ps.md)                                       | Moltiplicazione 4x3                                                                         | 3                 |       | x          |         |              |     |
| [m4x4 - ps](m4x4---ps.md)                                       | Moltiplicazione 4x4                                                                         | 4                 |       | x          |         |              |     |
| [mad - ps](mad---ps.md)                                         | Moltiplicare e aggiungere                                                                     | 1                 |       | x          |         |              |     |
| [max - ps](max---ps.md)                                         | Massimo                                                                              | 1                 |       | x          |         |              |     |
| [min - ps](min---ps.md)                                         | Minimo                                                                              | 1                 |       | x          |         |              |     |
| [mov - ps](mov---ps.md)                                         | Spostamento                                                                                 | 1                 |       | x          |         |              |     |
| [mul - ps](mul---ps.md)                                         | Moltiplicazione                                                                             | 1                 |       | x          |         |              |     |
| [nop - ps](nop---ps.md)                                         | Nessuna operazione                                                                         | 1                 |       | x          |         |              |     |
| [nrm - ps](nrm---ps.md)                                         | Normalizzare                                                                            | 3                 |       | x          |         |              |     |
| [pow - ps](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [Ps](ps---ps.md)                                                | Versione                                                                              | 0                 | x     |            |         |              |     |
| [rcp - ps](rcp---ps.md)                                         | Reciproco                                                                           | 1                 |       | x          |         |              |     |
| [rep - ps](rep---ps.md)                                         | Repeat                                                                               | 3                 |       |            |         | x            |     |
| [ret - ps](ret---ps.md)                                         | Fine di una subroutine                                                                  | 1                 |       |            |         | x            |     |
| [rsq - ps](rsq---ps.md)                                         | Radice quadrata reciproca                                                               | 1                 |       | x          |         |              |     |
| [setp \_ comp](setp-comp---ps.md)                                 | Impostare il registro del predicato                                                           | 1                 |       |            |         | x            |     |
| [sincos - ps](sincos---ps.md)                                   | Seno e coseno                                                                      | 8                 |       | x          |         |              |     |
| [sub - ps](sub---ps.md)                                         | Sottrazione                                                                             | 1                 |       | x          |         |              |     |
| [texkill - ps](texkill---ps.md)                                 | Kill pixel render (Kill Pixel Render)                                                                    | 2                 |       |            | x       |              |     |
| [texld - ps \_ 2 \_ 0 e up](texld---ps-2-0.md)                    | Campionare una trama                                                                     | Vedere la nota 1        |       |            | x       |              |     |
| [texldb - ps](texldb---ps.md)                                   | Campionamento delle trame con distorsione del livello di dettaglio da w-component                          | 6                 |       |            | x       |              |     |
| [texldl - ps](texldl---ps.md)                                   | Campionamento trame con livello di dettaglio dal componente w                               | Vedere la nota 2        |       |            | x       |              | x   |
| [texldd - ps](texldd---ps.md)                                   | Campionamento di trame con sfumature fornite dall'utente                                        | 3                 |       |            | x       |              |     |
| [texldp - ps](texldp---ps.md)                                   | Campionamento di trame con divisione proiettata per componente W                               | Vedere la nota 3        |       |            | x       |              |     |



 

Note:

1.  Se la trama è una mappa cubo, slot = 4; in caso contrario, slot = 1.
2.  Se la trama è una mappa cubo, slot = 5; in caso contrario, slot = 2.
3.  Se la trama è una mappa cubo, slot = 4; in caso contrario, slot = 3.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




