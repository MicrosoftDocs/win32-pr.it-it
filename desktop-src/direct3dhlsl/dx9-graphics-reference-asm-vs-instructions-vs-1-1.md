---
title: Istruzioni - vs_1_1
description: Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione \_ 1 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f980640009158c6c4dc684158836d1514ca47755fea700ac7cc619f6e7574409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789091"
---
# <a name="instructions---vs_1_1"></a>Istruzioni - vs \_ 1 \_ 1

Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione \_ 1 1.

Esistono diversi tipi di istruzioni vertex shader, come illustrato nella tabella. Le colonne a destra sono le seguenti:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Configurazione: istruzioni non aritmetiche. Ogni shader deve avere un'istruzione di versione e deve essere la prima istruzione.
-   Aritmetica: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Nuovo: queste istruzioni non sono nuove di questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                                           | Descrizione                                                                                                     | Slot di istruzioni | Eseguire la configurazione | Aritmetico | Nuovo |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [add - vs](add---vs.md)                                                       | Aggiungere due vettori                                                                                                 | 1                 |       | x          | x   |
| [Input di utilizzo dcl \_ (sm1, sm2, sm3 - vs asm)](dcl-usage-input-register---vs.md) | Dichiarare i registri dei vertici di input (vedere [Registri - vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def - vs](def---vs.md)                                                       | Definire costanti                                                                                                | 0                 | x     |            | x   |
| [dp3 - vs](dp3---vs.md)                                                       | Prodotto dot a tre componenti                                                                                     | 1                 |       | x          | x   |
| [dp4 - vs](dp4---vs.md)                                                       | Prodotto dot a quattro componenti                                                                                      | 1                 |       | x          | x   |
| [dst - vs](dst---vs.md)                                                       | Calcolare il vettore di distanza                                                                                   | 1                 |       | x          | x   |
| [exp - vs](exp---vs.md)                                                       | Precisione completa 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp - vs](exp---vs.md)                                                       | Precisione parziale 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [frc - vs](frc---vs.md)                                                       | Componente frazionario                                                                                            | 3                 |       | x          | x   |
| [lit - vs](lit---vs.md)                                                       | Calcolo parziale dell'illuminazione                                                                                    | 1                 |       | x          | x   |
| [log - vs](log---vs.md)                                                       | Log con precisione completa(x)                                                                                          | 10                |       | x          | x   |
| [logp - vs](logp---vs.md)                                                     | Log con precisione parziale(x)                                                                                       | 1                 |       | x          | x   |
| [m3x2 - vs](m3x2---vs.md)                                                     | Moltiplicazione 3x2                                                                                                    | 2                 |       | x          | x   |
| [m3x3 - vs](m3x3---vs.md)                                                     | Moltiplicazione 3x3                                                                                                    | 3                 |       | x          | x   |
| [m3x4 - vs](m3x4---vs.md)                                                     | Moltiplicazione 3x4                                                                                                    | 4                 |       | x          | x   |
| [m4x3 - vs](m4x3---vs.md)                                                     | Moltiplicazione 4x3                                                                                                    | 3                 |       | x          | x   |
| [m4x4 - vs](m4x4---vs.md)                                                     | Moltiplicazione 4x4                                                                                                    | 4                 |       | x          | x   |
| [mad - vs](mad---vs.md)                                                       | Moltiplicare e aggiungere                                                                                                | 1                 |       | x          | x   |
| [max - vs](max---vs.md)                                                       | Massimo                                                                                                         | 1                 |       | x          | x   |
| [min - vs](min---vs.md)                                                       | Minimo                                                                                                         | 1                 |       | x          | x   |
| [mov - vs](mov---vs.md)                                                       | Spostamento                                                                                                            | 1                 |       | x          | x   |
| [mul - vs](mul---vs.md)                                                       | Moltiplicazione                                                                                                        | 1                 |       | x          | x   |
| [nop - vs](nop---vs.md)                                                       | Nessuna operazione                                                                                                    | 1                 |       | x          | x   |
| [rcp - vs](rcp---vs.md)                                                       | Reciproco                                                                                                      | 1                 |       | x          | x   |
| [rsq - vs](rsq---vs.md)                                                       | Radice quadrata reciproca                                                                                          | 1                 |       | x          | x   |
| [sge - vs](sge---vs.md)                                                       | Confronto maggiore o uguale a                                                                                   | 1                 |       | x          | x   |
| [slt - vs](slt---vs.md)                                                       | Confronto minore di                                                                                               | 1                 |       | x          | x   |
| [sub - vs](sub---vs.md)                                                       | Sottrazione                                                                                                        | 1                 |       | x          | x   |
| [Vs](vs---vs.md)                                                              | Versione                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




