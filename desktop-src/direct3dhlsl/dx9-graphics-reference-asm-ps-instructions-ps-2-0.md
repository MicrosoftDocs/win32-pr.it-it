---
title: ps_2_0 istruzioni
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 292263ed6331c8cc878d6dbd9cfa3e4d766c193d2242b841afb926b296675ccf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067991"
---
# <a name="ps_2_0-instructions"></a>Istruzioni \_ ps 2 \_ 0

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 2 \_ 0.

Esistono diversi tipi di istruzioni pixel shader, come illustrato nella tabella. Le colonne a destra sono le seguenti:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: un pixel shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetica: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Trama: queste istruzioni vengono usate per caricare e campionare i dati delle trame e per modificare le coordinate della trama.
-   Nuovo: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                             | Descrizione                                                                                      | Slot di istruzioni | Eseguire la configurazione | Aritmetico | Trama | Nuovo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [abs - ps](abs---ps.md)                                         | Valore assoluto                                                                                   | 1                 |       | x          |         | x   |
| [add - ps](add---ps.md)                                         | Aggiungere due vettori                                                                                  | 1                 |       | x          |         |     |
| [cmp - ps](cmp---ps.md)                                         | Confrontare l'origine con 0                                                                              | 1                 |       | x          |         |     |
| [crs - ps](crs---ps.md)                                         | Prodotto incrociato                                                                                    | 2                 |       | x          |         | x   |
| [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) | Dichiarare la dimensione della trama per un campionatore                                                      | 0                 | x     |            |         | x   |
| [dcl - (sm2, sm3 - ps asm)](dcl---ps.md)                        | Dichiarare l'associazione tra i registri di output del vertex shader e pixel shader di input. | 0                 | x     |            |         | x   |
| [def - ps](def---ps.md)                                         | Definire costanti                                                                                 | 0                 | x     |            |         |     |
| [dp2add - ps](dp2add---ps.md)                                   | Prodotto punto 2D e aggiunta                                                                           | 2                 |       | x          |         | x   |
| [dp3 - ps](dp3---ps.md)                                         | Prodotto punto 3D                                                                                   | 1                 |       | x          |         |     |
| [dp4 - ps](dp4---ps.md)                                         | Prodotto punto 4D                                                                                   | 1                 |       | x          |         |     |
| [exp - ps](exp---ps.md)                                         | Precisione completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [frc - ps](frc---ps.md)                                         | Componente frazionario                                                                             | 1                 |       | x          |         | x   |
| [log - ps](log---ps.md)                                         | Logodato di precisione completa(x)                                                                           | 1                 |       | x          |         | x   |
| [lrp - ps](lrp---ps.md)                                         | Interpolazione lineare                                                                               | 2                 |       | x          |         |     |
| [m3x2 - ps](m3x2---ps.md)                                       | Moltiplicazione 3x2                                                                                     | 2                 |       | x          |         | x   |
| [m3x3 - ps](m3x3---ps.md)                                       | Moltiplicazione 3x3                                                                                     | 3                 |       | x          |         | x   |
| [m3x4 - ps](m3x4---ps.md)                                       | Moltiplicazione 3x4                                                                                     | 4                 |       | x          |         | x   |
| [m4x3 - ps](m4x3---ps.md)                                       | Moltiplicazione 4x3                                                                                     | 3                 |       | x          |         | x   |
| [m4x4 - ps](m4x4---ps.md)                                       | Moltiplicazione 4x4                                                                                     | 4                 |       | x          |         | x   |
| [mad - ps](mad---ps.md)                                         | Moltiplicare e aggiungere                                                                                 | 1                 |       | x          |         |     |
| [max - ps](max---ps.md)                                         | Massimo                                                                                          | 1                 |       | x          |         | x   |
| [min - ps](min---ps.md)                                         | Minimo                                                                                          | 1                 |       | x          |         | x   |
| [mov - ps](mov---ps.md)                                         | Spostamento                                                                                             | 1                 |       | x          |         |     |
| [mul - ps](mul---ps.md)                                         | Moltiplicazione                                                                                         | 1                 |       | x          |         |     |
| [nop - ps](nop---ps.md)                                         | Nessuna operazione                                                                                     | 1                 |       | x          |         |     |
| [nrm - ps](nrm---ps.md)                                         | Normalizzare                                                                                        | 3                 |       | x          |         | x   |
| [pow - ps](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [Ps](ps---ps.md)                                                | Versione                                                                                          | 0                 | x     |            |         |     |
| [rcp - ps](rcp---ps.md)                                         | Reciproco                                                                                       | 1                 |       | x          |         | x   |
| [rsq - ps](rsq---ps.md)                                         | Radice quadrata reciproca                                                                           | 1                 |       | x          |         | x   |
| [sincos - ps](sincos---ps.md)                                   | Seno e coseno                                                                                  | 8                 |       | x          |         | x   |
| [sub - ps](sub---ps.md)                                         | Sottrazione                                                                                         | 1                 |       | x          |         |     |
| [texkill - ps](texkill---ps.md)                                 | Kill pixel render (Kill Pixel Render)                                                                                | 1                 |       |            | x       |     |
| [texld - ps \_ 2 \_ 0 e up](texld---ps-2-0.md)                    | Campionare una trama                                                                                 | 1                 |       |            | x       | x   |
| [texldb - ps](texldb---ps.md)                                   | Campionamento delle trame con distorsione del livello di dettaglio da w-component                                      | 1                 |       |            | x       | x   |
| [texldp - ps](texldp---ps.md)                                   | Campionamento di trame con divisione proiettata per componente W                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




