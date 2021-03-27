---
title: Istruzioni-vs_1_1
description: Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione 1 \_ 1.
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b4def55dfaca19608599d9c79e20d3e0690832c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975930"
---
# <a name="instructions---vs_1_1"></a>Istruzioni-vs \_ 1 \_ 1

Questa sezione contiene informazioni di riferimento per le istruzioni vertex shader versione 1 \_ 1.

Sono disponibili diversi tipi di istruzioni vertex shader, come illustrato nella tabella. Le colonne a destra indicano quanto segue:

-   Slot di istruzioni: numero di slot di istruzioni usati da ogni istruzione.
-   Installazione: istruzioni non aritmetiche. Ogni shader deve avere un'istruzione version e deve essere la prima istruzione.
-   Aritmetico: queste istruzioni forniscono le operazioni matematiche in uno shader.
-   Novità: queste istruzioni sono nuove per questa versione.

## <a name="instruction-set"></a>Set di istruzioni



| Nome                                                                           | Descrizione                                                                                                     | Slot di istruzioni | Configurazione | Aritmetico | Nuova |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [Aggiungi-vs](add---vs.md)                                                       | Aggiungere due vettori                                                                                                 | 1                 |       | x          | x   |
| [\_input utilizzo DCL (SM1, SM2, SM3-vs ASM)](dcl-usage-input-register---vs.md) | Dichiarare i registri vertici di input (vedere [registri-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) | 0                 | x     |            | x   |
| [def-vs](def---vs.md)                                                       | Definisci costanti                                                                                                | 0                 | x     |            | x   |
| [DP3-vs](dp3---vs.md)                                                       | Prodotto dot a tre componenti                                                                                     | 1                 |       | x          | x   |
| [DP4-vs](dp4---vs.md)                                                       | Prodotto a quattro componenti                                                                                      | 1                 |       | x          | x   |
| [DST-vs](dst---vs.md)                                                       | Calcolare il vettore distanza                                                                                   | 1                 |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Precisione completa 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | Precisione parziale 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [FRC-vs](frc---vs.md)                                                       | Componente frazionario                                                                                            | 3                 |       | x          | x   |
| [Lit-vs](lit---vs.md)                                                       | Calcolo dell'illuminazione parziale                                                                                    | 1                 |       | x          | x   |
| [log-vs](log---vs.md)                                                       | ₂ di log con precisione completa (x)                                                                                          | 10                |       | x          | x   |
| [LogP-vs](logp---vs.md)                                                     | ₂ di log con precisione parziale (x)                                                                                       | 1                 |       | x          | x   |
| [M3X2-vs](m3x2---vs.md)                                                     | 3x2 Multiply                                                                                                    | 2                 |       | x          | x   |
| [M3X3-vs](m3x3---vs.md)                                                     | moltiplicazione 3x3                                                                                                    | 3                 |       | x          | x   |
| [M3x4-vs](m3x4---vs.md)                                                     | 3x4 Multiply                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 Multiply                                                                                                    | 3                 |       | x          | x   |
| [M4x4-vs](m4x4---vs.md)                                                     | moltiplicazione 4x4                                                                                                    | 4                 |       | x          | x   |
| [MAD-vs](mad---vs.md)                                                       | Moltiplica e Aggiungi                                                                                                | 1                 |       | x          | x   |
| [Max-vs](max---vs.md)                                                       | Massimo                                                                                                         | 1                 |       | x          | x   |
| [min-vs](min---vs.md)                                                       | Minima                                                                                                         | 1                 |       | x          | x   |
| [MOV-vs](mov---vs.md)                                                       | Spostamento                                                                                                            | 1                 |       | x          | x   |
| [Mul-vs](mul---vs.md)                                                       | Moltiplicazione                                                                                                        | 1                 |       | x          | x   |
| [NOP-vs](nop---vs.md)                                                       | Nessuna operazione                                                                                                    | 1                 |       | x          | x   |
| [RCP-vs](rcp---vs.md)                                                       | Reciproco                                                                                                      | 1                 |       | x          | x   |
| [RSQ-vs](rsq---vs.md)                                                       | Radice quadrata reciproca                                                                                          | 1                 |       | x          | x   |
| [SGE-vs](sge---vs.md)                                                       | Confronto maggiore o uguale a                                                                                   | 1                 |       | x          | x   |
| [SLT-vs](slt---vs.md)                                                       | Minore di compare                                                                                               | 1                 |       | x          | x   |
| [Sub-vs](sub---vs.md)                                                       | Sottrazione                                                                                                        | 1                 |       | x          | x   |
| [vs](vs---vs.md)                                                              | Versione                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




