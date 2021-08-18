---
title: ps_2_x istruzioni
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ x.
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3e1fcb16cace82118d153412ba5471876d4ebcc58c342466ff86db016189a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744671"
---
# <a name="ps_2_x-instructions"></a>Ps \_ 2 \_ x Istruzioni

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ x.

Esistono diversi tipi di istruzioni pixel shader, come illustrato nella tabella. Le colonne a destra sono le seguenti:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: un pixel shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetica: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni vengono usate per caricare e campionare i dati delle trame e per modificare le coordinate della trama.
-   Flow controllo dinamico: queste istruzioni forniscono il controllo di flusso statico e dinamico all'esecuzione delle istruzioni.
-   Nuovo: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                             | Descrizione                                                                                      | Slot di istruzioni | Eseguire la configurazione | Aritmetico | Trama | Controllo di flusso | Nuovo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs - ps](abs---ps.md)                                         | Valore assoluto                                                                                   | 1                 |       | x          |         |              |     |
| [add - ps](add---ps.md)                                         | Aggiungere due vettori                                                                                  | 1                 |       | x          |         |              |     |
| [break - ps](break---ps.md)                                     | Break out of a rep... endrep block                                                                | 1                 |       |            |         | x            | x   |
| [break \_ comp - ps](break-comp---ps.md)                          | Interruzione condizionale di un rappresentante... endrep block, con un confronto                               | 3                 |       |            |         | x            | x   |
| [breakp - ps](break-p---ps.md)                                  | Break out of a rep... blocco endrep, basato su un predicato                                          | 3                 |       |            |         | x            | x   |
| [call - ps](call---ps.md)                                       | Chiamare una subroutine                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool - ps](callnz-bool---ps.md)                         | Chiamare una subroutine se un registro booleano è diverso da zero                                              | 3                 |       |            |         | x            | x   |
| [callnz pred - ps](callnz-pred---ps.md)                         | Chiamare una subroutine se un registro del predicato è diverso da zero                                            | 3                 |       |            |         | x            | x   |
| [cmp - ps](cmp---ps.md)                                         | Confrontare l'origine con 0                                                                              | 1                 |       | x          |         |              |     |
| [crs - ps](crs---ps.md)                                         | Prodotto incrociato                                                                                    | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Dichiarare la dimensione della trama per un campionatore                                                      | 0                 | x     |            |         |              |     |
| [dcl - (sm2, sm3 - ps asm)](dcl---ps.md)                        | Dichiarare l'associazione tra i registri di output del vertex shader e pixel shader di input. | 0                 | x     |            |         |              |     |
| [def - ps](def---ps.md)                                         | Definire costanti                                                                                 | 0                 | x     |            |         |              |     |
| [defb - ps](defb---ps.md)                                       | Definire una costante booleana                                                                        | 0                 | x     |            |         |              | x   |
| [defi - ps](defi---ps.md)                                       | Definire una costante integer                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add - ps](dp2add---ps.md)                                   | Prodotto punto 2D e aggiunta                                                                           | 2                 |       | x          |         |              |     |
| [dp3 - ps](dp3---ps.md)                                         | Prodotto punto 3D                                                                                   | 1                 |       | x          |         |              |     |
| [dp4 - ps](dp4---ps.md)                                         | Prodotto punto 4D                                                                                   | 1                 |       | x          |         |              |     |
| [dsx - ps](dsx---ps.md)                                         | Frequenza di modifica nella direzione x                                                                | 2                 |       | x          |         |              | x   |
| [dsy - ps](dsy---ps.md)                                         | Frequenza di modifica nella direzione y                                                                | 2                 |       | x          |         |              | x   |
| [else - ps](else---ps.md)                                       | Iniziare un blocco else                                                                              | 1                 |       |            |         | x            | x   |
| [endif - ps](endif---ps.md)                                     | Terminare un'operazione if... blocco else                                                                           | 1                 |       |            |         | x            | x   |
| [endrep - ps](endrep---ps.md)                                   | Fine di un blocco di ripetizione                                                                            | 2                 |       |            |         | x            | x   |
| [exp - ps](exp---ps.md)                                         | Precisione completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [frc - ps](frc---ps.md)                                         | Componente frazionario                                                                             | 1                 |       | x          |         |              |     |
| [if bool - ps](if-bool---ps.md)                                 | Iniziare un blocco if                                                                                | 3                 |       |            |         | x            | x   |
| [if \_ comp - ps](if-comp---ps.md)                                | Iniziare un blocco if con un confronto                                                              | 3                 |       |            |         | x            | x   |
| [if pred - ps](if-pred---ps.md)                                 | Iniziare un blocco if con predicazione                                                               | 3                 |       |            |         | x            | x   |
| [label - ps](label---ps.md)                                     | Etichetta                                                                                            | 0                 |       |            |         | x            | x   |
| [log - ps](log---ps.md)                                         | Logodato di precisione completa(x)                                                                           | 1                 |       | x          |         |              |     |
| [lrp - ps](lrp---ps.md)                                         | Interpolazione lineare                                                                               | 2                 |       | x          |         |              |     |
| [m3x2 - ps](m3x2---ps.md)                                       | Moltiplicazione 3x2                                                                                     | 2                 |       | x          |         |              |     |
| [m3x3 - ps](m3x3---ps.md)                                       | Moltiplicazione 3x3                                                                                     | 3                 |       | x          |         |              |     |
| [m3x4 - ps](m3x4---ps.md)                                       | Moltiplicazione 3x4                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3 - ps](m4x3---ps.md)                                       | Moltiplicazione 4x3                                                                                     | 3                 |       | x          |         |              |     |
| [m4x4 - ps](m4x4---ps.md)                                       | Moltiplicazione 4x4                                                                                     | 4                 |       | x          |         |              |     |
| [mad - ps](mad---ps.md)                                         | Moltiplicare e aggiungere                                                                                 | 1                 |       | x          |         |              |     |
| [max - ps](max---ps.md)                                         | Massimo                                                                                          | 1                 |       | x          |         |              |     |
| [min - ps](min---ps.md)                                         | Minimo                                                                                          | 1                 |       | x          |         |              |     |
| [mov - ps](mov---ps.md)                                         | Spostamento                                                                                             | 1                 |       | x          |         |              |     |
| [mul - ps](mul---ps.md)                                         | Moltiplicazione                                                                                         | 1                 |       | x          |         |              |     |
| [nop - ps](nop---ps.md)                                         | Nessuna operazione                                                                                     | 1                 |       | x          |         |              |     |
| [nrm - ps](nrm---ps.md)                                         | Normalizzare                                                                                        | 3                 |       | x          |         |              |     |
| [pow - ps](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [Ps](ps---ps.md)                                                | Versione                                                                                          | 0                 | x     |            |         |              |     |
| [rcp - ps](rcp---ps.md)                                         | Reciproco                                                                                       | 1                 |       | x          |         |              |     |
| [rep - ps](rep---ps.md)                                         | Repeat                                                                                           | 3                 |       |            |         | x            | x   |
| [ret - ps](ret---ps.md)                                         | Fine di una subroutine                                                                              | 1                 |       |            |         | x            | x   |
| [rsq - ps](rsq---ps.md)                                         | Radice quadrata reciproca                                                                           | 1                 |       | x          |         |              |     |
| [setp \_ comp](setp-comp---ps.md)                                 | Impostare il registro predicati                                                                       | 1                 |       |            |         | x            | x   |
| [sincos - ps](sincos---ps.md)                                   | Seno e coseno                                                                                  | 8                 |       | x          |         |              |     |
| [sub - ps](sub---ps.md)                                         | Sottrazione                                                                                         | 1                 |       | x          |         |              |     |
| [texkill - ps](texkill---ps.md)                                 | Uccidi rendering pixel                                                                                | Vedere la nota 1        |       |            | x       |              |     |
| [texld - ps \_ 2 \_ 0 e up](texld---ps-2-0.md)                    | Campionare una trama                                                                                 | Vedere la nota 2        |       |            | x       |              |     |
| [texldb - ps](texldb---ps.md)                                   | Campionamento trame con distorsione del livello di dettaglio dal componente w                                      | Vedere la nota 3        |       |            | x       |              |     |
| [texldd - ps](texldd---ps.md)                                   | Campionamento trame con sfumature fornite dall'utente                                                    | 3                 |       |            | x       |              | x   |
| [texldp - ps](texldp---ps.md)                                   | Campionamento delle trame con divisione proiettativa per w-component                                           | Vedere la nota 4        |       |            | x       |              |     |



 

Note:

1.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato, slot = 2; in caso contrario, slot = 1.
2.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato e la trama è una mappa del cubo, slot = 4; in caso contrario slot = 1.
3.  Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) slot = 6; in caso contrario, slot = 1.
4.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) non è impostato, slot = 1; in caso contrario:
    -   se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato e la trama è una mappa del cubo, slot = 4.
    -   se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato e la trama non è una mappa del cubo, slot = 3.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 