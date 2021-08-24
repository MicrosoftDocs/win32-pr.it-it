---
title: Istruzioni - vs_2_0
description: Questa sezione contiene informazioni di riferimento per le istruzioni relative al vertex shader versione \_ 2 0.
ms.assetid: f5ca3e44-3c71-4221-9381-cea521d984e0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0baaa0fb9523e59e3dafdb0a7dd1dd7856325c518f06995da4d768929982b6f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744471"
---
# <a name="instructions---vs_2_0"></a>Istruzioni - vs \_ 2 \_ 0

Questa sezione contiene informazioni di riferimento per le istruzioni relative al vertex shader versione \_ 2 0.

Esistono diversi tipi di istruzioni per vertex shader, come illustrato nella tabella. Le colonne a destra sono le seguenti:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Configurazione: istruzioni non aritmetiche. Ogni shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetica: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Flow controllo: queste istruzioni aggiungono funzionalità di controllo del flusso, ad esempio [ciclo](loop---vs.md)... [endloop](endloop---vs.md), [se](if-bool---vs.md)... [else](else---vs.md)... [endif - rispetto alle](endif---vs.md)chiamate di subroutine e .
-   Nuovo: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                                           | Descrizione                                                                                                     | Slot di istruzioni | Eseguire la configurazione | Aritmetico | Controllo di flusso | Nuovo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs - vs](abs---vs.md)                                                       | Valore assoluto                                                                                                  | 1                 |       | x          |              | x   |
| [add - vs](add---vs.md)                                                       | Aggiungere due vettori                                                                                                 | 1                 |       | x          |              |     |
| [call - vs](call---vs.md)                                                     | Chiamare una subroutine                                                                                               | 2                 |       |            | x            | x   |
| [callnz bool - vs](callnz-bool---vs.md)                                       | Chiamare una subroutine se un registro booleano è diverso da zero                                                             | 3                 |       |            | x            | x   |
| [crs - vs](crs---vs.md)                                                       | Prodotto incrociato                                                                                                   | 2                 |       | x          |              | x   |
| [dcl \_ usage input (sm1, sm2, sm3 - vs asm)](dcl-usage-input-register---vs.md) | Dichiarare i registri dei vertici di input (vedere [Registri - vs \_ 2 \_ 0)](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) | 0                 | x     |            |              |     |
| [def - vs](def---vs.md)                                                       | Definire costanti                                                                                                | 0                 | x     |            |              |     |
| [defb - vs](defb---vs.md)                                                     | Definire una costante booleana                                                                                       | 0                 | x     |            |              | x   |
| [defi - vs](defi---vs.md)                                                     | Definire una costante integer                                                                                      | 0                 | x     |            |              | x   |
| [dp3 - vs](dp3---vs.md)                                                       | Prodotto punto a tre componenti                                                                                     | 1                 |       | x          |              |     |
| [dp4 - vs](dp4---vs.md)                                                       | Prodotto punto a quattro componenti                                                                                      | 1                 |       | x          |              |     |
| [dst - vs](dst---vs.md)                                                       | Calcolare il vettore di distanza                                                                                   | 1                 |       | x          |              |     |
| [else - vs](else---vs.md)                                                     | Begin an [else - vs](else---vs.md) block                                                                       | 1                 |       |            | x            | x   |
| [endif - vs](endif---vs.md)                                                   | Terminare [un if bool - vs](if-bool---vs.md)... [else - vs](else---vs.md) block                                      | 1                 |       |            | x            | x   |
| [endloop - vs](endloop---vs.md)                                               | Fine di un [ciclo - vs](loop---vs.md) blocco                                                                       | 2                 |       |            | x            | x   |
| [endrep - vs](endrep---vs.md)                                                 | Fine di un blocco di ripetizione                                                                                           | 2                 |       |            | x            | x   |
| [exp - vs](exp---vs.md)                                                       | Precisione completa 2<sup>x</sup>                                                                                    | 1                 |       | x          |              |     |
| [exp - vs](exp---vs.md)                                                       | Precisione parziale 2<sup>x</sup>                                                                                 | 1                 |       | x          |              |     |
| [frc - vs](frc---vs.md)                                                       | Componente frazionario                                                                                            | 1                 |       | x          |              |     |
| [if bool - vs](if-bool---vs.md)                                               | Iniziare un [blocco if bool - vs](if-bool---vs.md) (usando una condizione booleana)                                     | 3                 |       |            | x            | x   |
| [label - vs](label---vs.md)                                                   | Etichetta                                                                                                           | 0                 |       |            | x            | x   |
| [lit - vs](lit---vs.md)                                                       | Calcolo dell'illuminazione parziale                                                                                    | 3                 |       | x          |              |     |
| [log - e](log---vs.md)                                                       | Logodato di precisione completa(x)                                                                                          | 1                 |       | x          |              |     |
| [logp - vs](logp---vs.md)                                                     | Partial precision log più(x)                                                                                       | 1                 |       | x          |              |     |
| [loop - vs](loop---vs.md)                                                     | Ciclo                                                                                                            | 3                 |       |            | x            | x   |
| [lrp - vs](lrp---vs.md)                                                       | Interpolazione lineare                                                                                            | 2                 |       | x          |              | x   |
| [m3x2 - vs](m3x2---vs.md)                                                     | Moltiplicazione 3x2                                                                                                    | 2                 |       | x          |              |     |
| [m3x3 - vs](m3x3---vs.md)                                                     | Moltiplicazione 3x3                                                                                                    | 3                 |       | x          |              |     |
| [m3x4 - vs](m3x4---vs.md)                                                     | Moltiplicazione 3x4                                                                                                    | 4                 |       | x          |              |     |
| [m4x3 - vs](m4x3---vs.md)                                                     | Moltiplicazione 4x3                                                                                                    | 3                 |       | x          |              |     |
| [m4x4 - vs](m4x4---vs.md)                                                     | Moltiplicazione 4x4                                                                                                    | 4                 |       | x          |              |     |
| [mad - vs](mad---vs.md)                                                       | Moltiplicare e aggiungere                                                                                                | 1                 |       | x          |              |     |
| [max - vs](max---vs.md)                                                       | Massimo                                                                                                         | 1                 |       | x          |              |     |
| [min - vs](min---vs.md)                                                       | Minimo                                                                                                         | 1                 |       | x          |              |     |
| [mov - vs](mov---vs.md)                                                       | Spostamento                                                                                                            | 1                 |       | x          |              |     |
| [mova - vs](mova---vs.md)                                                     | Spostare i dati da un registro a virgola mobile al registro degli indirizzi (a0)                                           | 1                 |       | x          |              | x   |
| [mul - vs](mul---vs.md)                                                       | Moltiplicazione                                                                                                        | 1                 |       | x          |              |     |
| [nop - vs](nop---vs.md)                                                       | Nessuna operazione                                                                                                    | 1                 |       | x          |              |     |
| [nrm - vs](nrm---vs.md)                                                       | Normalizzare un vettore 4D                                                                                           | 3                 |       | x          |              | x   |
| [pow - vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                   | 3                 |       | x          |              | x   |
| [rcp - vs](rcp---vs.md)                                                       | Reciproco                                                                                                      | 1                 |       | x          |              |     |
| [rep - vs](rep---vs.md)                                                       | Repeat                                                                                                          | 3                 |       |            | x            | x   |
| [ret - vs](ret---vs.md)                                                       | Fine di una subroutine o main                                                                              | 1                 |       |            | x            | x   |
| [rsq - vs](rsq---vs.md)                                                       | Radice quadrata reciproca                                                                                          | 1                 |       | x          |              |     |
| [sge - vs](sge---vs.md)                                                       | Confronto maggiore o uguale a                                                                                   | 1                 |       | x          |              |     |
| [sgn - vs](sgn---vs.md)                                                       | Sign                                                                                                            | 3                 |       | x          |              | x   |
| [sincos - vs](sincos---vs.md)                                                 | Seno e coseno                                                                                                 | 8                 |       | x          |              | x   |
| [slt - vs](slt---vs.md)                                                       | Confronto minore di                                                                                               | 1                 |       | x          |              |     |
| [sub - vs](sub---vs.md)                                                       | Sottrazione                                                                                                        | 1                 |       | x          |              |     |
| [Vs](vs---vs.md)                                                              | Versione                                                                                                         | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




