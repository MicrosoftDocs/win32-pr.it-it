---
title: Istruzioni ps_2_0
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bac2a70ed0147885174c2290d5e58c92ae3347e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992880"
---
# <a name="ps_2_0-instructions"></a>\_istruzioni PS 2 \_ 0

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ 0.

Sono disponibili diversi tipi di istruzioni di pixel shader, come illustrato nella tabella. Le colonne a destra indicano quanto segue:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: un pixel shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetico: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni vengono usate per caricare e campionare i dati di trama e per modificare le coordinate di trama.
-   Novità: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                             | Descrizione                                                                                      | Slot di istruzioni | Configurazione | Aritmetico | Trama | Nuova |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [ABS-PS](abs---ps.md)                                         | Valore assoluto                                                                                   | 1                 |       | x          |         | x   |
| [Add-PS](add---ps.md)                                         | Aggiungere due vettori                                                                                  | 1                 |       | x          |         |     |
| [CMP-PS](cmp---ps.md)                                         | Confronta origine con 0                                                                              | 1                 |       | x          |         |     |
| [CRS-PS](crs---ps.md)                                         | Prodotto incrociato                                                                                    | 2                 |       | x          |         | x   |
| [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Dichiarare la dimensione di trama per un campionatore                                                      | 0                 | x     |            |         | x   |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Dichiarare l'associazione tra i registri di output del vertex shader e i registri di input pixel shader. | 0                 | x     |            |         | x   |
| [def-PS](def---ps.md)                                         | Definisci costanti                                                                                 | 0                 | x     |            |         |     |
| [dp2add-PS](dp2add---ps.md)                                   | prodotto a virgola 2D e aggiunta                                                                           | 2                 |       | x          |         | x   |
| [DP3-PS](dp3---ps.md)                                         | prodotto punto 3D                                                                                   | 1                 |       | x          |         |     |
| [DP4-PS](dp4---ps.md)                                         | prodotto 4D dot                                                                                   | 1                 |       | x          |         |     |
| [exp-PS](exp---ps.md)                                         | Precisione completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [FRC-PS](frc---ps.md)                                         | Componente frazionario                                                                             | 1                 |       | x          |         | x   |
| [log-PS](log---ps.md)                                         | ₂ di log con precisione completa (x)                                                                           | 1                 |       | x          |         | x   |
| [LRP-PS](lrp---ps.md)                                         | Interpolazione lineare                                                                               | 2                 |       | x          |         |     |
| [M3X2-PS](m3x2---ps.md)                                       | 3x2 Multiply                                                                                     | 2                 |       | x          |         | x   |
| [M3X3-PS](m3x3---ps.md)                                       | moltiplicazione 3x3                                                                                     | 3                 |       | x          |         | x   |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 Multiply                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 Multiply                                                                                     | 3                 |       | x          |         | x   |
| [M4x4-PS](m4x4---ps.md)                                       | moltiplicazione 4x4                                                                                     | 4                 |       | x          |         | x   |
| [MAD-PS](mad---ps.md)                                         | Moltiplica e Aggiungi                                                                                 | 1                 |       | x          |         |     |
| [max-PS](max---ps.md)                                         | Massimo                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Minima                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Spostamento                                                                                             | 1                 |       | x          |         |     |
| [Mul-PS](mul---ps.md)                                         | Moltiplicazione                                                                                         | 1                 |       | x          |         |     |
| [NOP-PS](nop---ps.md)                                         | Nessuna operazione                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizzare                                                                                        | 3                 |       | x          |         | x   |
| [POW-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [ps](ps---ps.md)                                                | Versione                                                                                          | 0                 | x     |            |         |     |
| [RCP-PS](rcp---ps.md)                                         | Reciproco                                                                                       | 1                 |       | x          |         | x   |
| [RSQ-PS](rsq---ps.md)                                         | Radice quadrata reciproca                                                                           | 1                 |       | x          |         | x   |
| [SinCos-PS](sincos---ps.md)                                   | Seno e coseno                                                                                  | 8                 |       | x          |         | x   |
| [Sub-PS](sub---ps.md)                                         | Sottrazione                                                                                         | 1                 |       | x          |         |     |
| [texkill-PS](texkill---ps.md)                                 | Rendering Kill pixel                                                                                | 1                 |       |            | x       |     |
| [texld-PS \_ 2 \_ 0 e su](texld---ps-2-0.md)                    | Campionare una trama                                                                                 | 1                 |       |            | x       | x   |
| [texldb-PS](texldb---ps.md)                                   | Campionamento di trama con distorsione del livello di dettaglio dal componente w                                      | 1                 |       |            | x       | x   |
| [texldp-PS](texldp---ps.md)                                   | Campionamento di trama con divisione proiezioni per w-Component                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




