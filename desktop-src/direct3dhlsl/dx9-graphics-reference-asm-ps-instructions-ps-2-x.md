---
title: Istruzioni ps_2_x
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ x.
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 047067d26f9b85ef981a007059d9f2e87ae28ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976759"
---
# <a name="ps_2_x-instructions"></a>\_istruzioni PS 2 \_ x

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ x.

Sono disponibili diversi tipi di istruzioni di pixel shader, come illustrato nella tabella. Le colonne a destra indicano quanto segue:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: un pixel shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetico: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni vengono usate per caricare e campionare i dati di trama e per modificare le coordinate di trama.
-   Controllo di flusso: queste istruzioni forniscono il controllo di flusso statico e dinamico all'esecuzione delle istruzioni.
-   Novità: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                             | Descrizione                                                                                      | Slot di istruzioni | Configurazione | Aritmetico | Trama | Controllo di flusso | Nuova |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Valore assoluto                                                                                   | 1                 |       | x          |         |              |     |
| [Add-PS](add---ps.md)                                         | Aggiungere due vettori                                                                                  | 1                 |       | x          |         |              |     |
| [Break-PS](break---ps.md)                                     | Interrompi un rep... blocco endrep                                                                | 1                 |       |            |         | x            | x   |
| [Interrompi \_ comp-PS](break-comp---ps.md)                          | Interrompi in modo condizionale da una Rep... blocco endrep con confronto                               | 3                 |       |            |         | x            | x   |
| [Breakp-PS](break-p---ps.md)                                  | Interrompi un rep... blocco endrep, basato su un predicato                                          | 3                 |       |            |         | x            | x   |
| [chiamata a PS](call---ps.md)                                       | Chiamare una subroutine                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool-PS](callnz-bool---ps.md)                         | Chiamare una subroutine se un registro booleano non è zero                                              | 3                 |       |            |         | x            | x   |
| [callnz prede-PS](callnz-pred---ps.md)                         | Chiamare una subroutine se un registro predicato non è zero                                            | 3                 |       |            |         | x            | x   |
| [CMP-PS](cmp---ps.md)                                         | Confronta origine con 0                                                                              | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Prodotto incrociato                                                                                    | 2                 |       | x          |         |              |     |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Dichiarare la dimensione di trama per un campionatore                                                      | 0                 | x     |            |         |              |     |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Dichiarare l'associazione tra i registri di output del vertex shader e i registri di input pixel shader. | 0                 | x     |            |         |              |     |
| [def-PS](def---ps.md)                                         | Definisci costanti                                                                                 | 0                 | x     |            |         |              |     |
| [defb-PS](defb---ps.md)                                       | Definire una costante booleana                                                                        | 0                 | x     |            |         |              | x   |
| [defi-PS](defi---ps.md)                                       | Definire una costante Integer                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add-PS](dp2add---ps.md)                                   | prodotto a virgola 2D e aggiunta                                                                           | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | prodotto punto 3D                                                                                   | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | prodotto 4D dot                                                                                   | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Frequenza delle modifiche nella direzione x                                                                | 2                 |       | x          |         |              | x   |
| [DSY-PS](dsy---ps.md)                                         | Frequenza delle modifiche nella direzione y                                                                | 2                 |       | x          |         |              | x   |
| [else-PS](else---ps.md)                                       | Inizia un blocco Else                                                                              | 1                 |       |            |         | x            | x   |
| [endif-PS](endif---ps.md)                                     | Termina un if... blocco Else                                                                           | 1                 |       |            |         | x            | x   |
| [endrep-PS](endrep---ps.md)                                   | Fine di un blocco di ripetizione                                                                            | 2                 |       |            |         | x            | x   |
| [exp-PS](exp---ps.md)                                         | Precisione completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Componente frazionario                                                                             | 1                 |       | x          |         |              |     |
| [Se bool-PS](if-bool---ps.md)                                 | Inizia un blocco if                                                                                | 3                 |       |            |         | x            | x   |
| [Se \_ comp-PS](if-comp---ps.md)                                | Inizia un blocco if con un confronto                                                              | 3                 |       |            |         | x            | x   |
| [Se prede-PS](if-pred---ps.md)                                 | Inizia un blocco if con predicazione                                                               | 3                 |       |            |         | x            | x   |
| [etichetta-PS](label---ps.md)                                     | Etichetta                                                                                            | 0                 |       |            |         | x            | x   |
| [log-PS](log---ps.md)                                         | ₂ di log con precisione completa (x)                                                                           | 1                 |       | x          |         |              |     |
| [LRP-PS](lrp---ps.md)                                         | Interpolazione lineare                                                                               | 2                 |       | x          |         |              |     |
| [M3X2-PS](m3x2---ps.md)                                       | 3x2 Multiply                                                                                     | 2                 |       | x          |         |              |     |
| [M3X3-PS](m3x3---ps.md)                                       | moltiplicazione 3x3                                                                                     | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 Multiply                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 Multiply                                                                                     | 3                 |       | x          |         |              |     |
| [M4x4-PS](m4x4---ps.md)                                       | moltiplicazione 4x4                                                                                     | 4                 |       | x          |         |              |     |
| [MAD-PS](mad---ps.md)                                         | Moltiplica e Aggiungi                                                                                 | 1                 |       | x          |         |              |     |
| [max-PS](max---ps.md)                                         | Massimo                                                                                          | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Minima                                                                                          | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Spostamento                                                                                             | 1                 |       | x          |         |              |     |
| [Mul-PS](mul---ps.md)                                         | Moltiplicazione                                                                                         | 1                 |       | x          |         |              |     |
| [NOP-PS](nop---ps.md)                                         | Nessuna operazione                                                                                     | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizzare                                                                                        | 3                 |       | x          |         |              |     |
| [POW-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [ps](ps---ps.md)                                                | Versione                                                                                          | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Reciproco                                                                                       | 1                 |       | x          |         |              |     |
| [Rep-PS](rep---ps.md)                                         | Repeat                                                                                           | 3                 |       |            |         | x            | x   |
| [RET-PS](ret---ps.md)                                         | Fine di una subroutine                                                                              | 1                 |       |            |         | x            | x   |
| [RSQ-PS](rsq---ps.md)                                         | Radice quadrata reciproca                                                                           | 1                 |       | x          |         |              |     |
| [setp \_ comp](setp-comp---ps.md)                                 | Impostare il registro del predicato                                                                       | 1                 |       |            |         | x            | x   |
| [SinCos-PS](sincos---ps.md)                                   | Seno e coseno                                                                                  | 8                 |       | x          |         |              |     |
| [Sub-PS](sub---ps.md)                                         | Sottrazione                                                                                         | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Rendering Kill pixel                                                                                | Vedere la nota 1        |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 e su](texld---ps-2-0.md)                    | Campionare una trama                                                                                 | Vedere la nota 2        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Campionamento di trama con distorsione del livello di dettaglio dal componente w                                      | Vedere la nota 3        |       |            | x       |              |     |
| [texldd-PS](texldd---ps.md)                                   | Campionamento di trama con sfumature fornite dall'utente                                                    | 3                 |       |            | x       |              | x   |
| [texldp-PS](texldp---ps.md)                                   | Campionamento di trama con divisione proiezioni per w-Component                                           | Vedere la nota 4        |       |            | x       |              |     |



 

Note:

1.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato, slot = 2. in caso contrario, slot = 1.
2.  Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) e la trama è una mappa cubo, slot = 4; in caso contrario, slot = 1.
3.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato, slot = 6; in caso contrario, slot = 1.
4.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) non è impostato, slot = 1; in caso contrario:
    -   Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) e la trama è una mappa cubo, slot = 4.
    -   Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) e la trama non è una mappa cubo, slot = 3.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 