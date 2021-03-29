---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 istruzioni
description: Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c3fa8e76e1075da321a60d05504dff074dbfcfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222121"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 istruzioni

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 1 \_ X.

Sono disponibili diversi tipi di istruzioni di pixel shader, come illustrato nella tabella seguente.

## <a name="instruction-set"></a>Set di istruzioni



| Versione                                    |                                                                               | Slot di istruzioni | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [ps](ps---ps.md)                          | Numero di versione                                                                | 0                 | x    | x    | x    | x    |
| Istruzioni costanti                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def-PS](def---ps.md)                   | Definisci costanti                                                              | 0                 | x    | x    | x    | x    |
| Istruzioni della fase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [fase-PS](phase---ps.md)               | Transizione tra la fase 1 e la fase 2                                        | 0                 |      |      |      | x    |
| Istruzioni aritmetiche                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Add-PS](add---ps.md)                   | Aggiungere due vettori                                                               | 1                 | x    | x    | x    | x    |
| [bem-PS](bem---ps.md)                   | Applicare un ambiente Bump finto-trasformazione Mappa                                   | 2                 |      |      |      | x    |
| [CMP-PS](cmp---ps.md)                   | Confronta origine con 0                                                           | 1 ¹                |      | x    | x    | x    |
| [CND-PS](cnd---ps.md)                   | Confronta origine con 0,5                                                         | 1                 | x    | x    | x    | x    |
| [DP3-PS](dp3---ps.md)                   | Prodotto dot a tre componenti                                                   | 1                 | x    | x    | x    | x    |
| [DP4-PS](dp4---ps.md)                   | Prodotto a quattro componenti                                                    | 1 ¹                |      | x    | x    | x    |
| [LRP-PS](lrp---ps.md)                   | Interpolazione lineare                                                            | 1                 | x    | x    | x    | x    |
| [MAD-PS](mad---ps.md)                   | Moltiplica e Aggiungi                                                              | 1                 | x    | x    | x    | x    |
| [MOV-PS](mov---ps.md)                   | Spostamento                                                                          | 1                 | x    | x    | x    | x    |
| [Mul-PS](mul---ps.md)                   | Moltiplicazione                                                                      | 1                 | x    | x    | x    | x    |
| [NOP-PS](nop---ps.md)                   | Nessuna operazione                                                                  | 0                 | x    | x    | x    | x    |
| [Sub-PS](sub---ps.md)                   | Sottrazione                                                                      | 1                 | x    | x    | x    | x    |
| Istruzioni di trama                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Tex-PS](tex---ps.md)                   | Campionare una trama                                                              | 1                 | x    | x    | x    |      |
| [texbem-PS](texbem---ps.md)             | Applicare un ambiente Bump finto-trasformazione Mappa                                   | 1                 | x    | x    | x    |      |
| [texbeml-PS](texbeml---ps.md)           | Applicare un ambiente Bump finto-trasformazione Mappa con la correzione della luminanza         | 1 +1 ²              | x    | x    | x    |      |
| [TEXCOORD-PS](texcoord---ps.md)         | Interpretare i dati delle coordinate di trama come dati di colore                               | 1                 | x    | x    | x    |      |
| [texcrd-PS](texcrd---ps.md)             | Copia i dati delle coordinate di trama come dati di colore                                    | 1                 |      |      |      | x    |
| [texdepth-PS](texdepth---ps.md)         | Calcolare i valori di profondità                                                        | 1                 |      |      |      | x    |
| [texdp3-PS](texdp3---ps.md)             | Prodotto punto a tre componenti tra i dati della trama e le coordinate di trama  | 1                 |      | x    | x    |      |
| [texdp3tex-PS](texdp3tex---ps.md)       | Prodotto a tre componenti e ricerca di trama 1D                             | 1                 |      | x    | x    |      |
| [texkill-PS](texkill---ps.md)           | Annulla il rendering dei pixel in base a un confronto                             | 1                 | x    | x    | x    | x    |
| [texld-PS \_ 1 \_ 4](texld---ps-1-4.md)     | Campionare una trama                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-PS](texm3x2depth---ps.md) | Calcolare i valori di profondità per pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad-PS](texm3x2pad---ps.md)     | Matrice della prima riga che si moltiplica per una matrice a due righe                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-PS](texm3x2tex---ps.md)     | Matrice di righe finale multipla di una matrice a due righe                        | 1                 | x    | x    | x    |      |
| [texm3x3-PS](texm3x3---ps.md)           | moltiplicazione matrice 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-PS](texm3x3pad---ps.md)     | Moltiplicazione della prima o della seconda riga di una matrice a tre righe                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-PS](texm3x3spec---ps.md)   | Moltiplicazione della riga finale di una matrice a tre righe                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-PS](texm3x3tex---ps.md)     | Trama-Cerca con una matrice 3x3 moltiplicata                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-PS](texm3x3vspec---ps.md) | Texture ricercata con una matrice 3x3 moltiplicata, con vettore di occhi non costanti | 1                 | x    | x    | x    |      |
| [texreg2ar-PS](texreg2ar---ps.md)       | Campionare una trama usando i componenti alfa e rosso                           | 1                 | x    | x    | x    |      |
| [texreg2gb-PS](texreg2gb---ps.md)       | Campionare una trama usando i componenti verde e blu                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-PS](texreg2rgb---ps.md)     | Campionare una trama usando i componenti rosso, verde e blu                     | 1                 |      | x    | x    |      |



 

1.  1 slot in PS \_ 1 \_ 4; 2 slot in PS \_ 1 \_ 2 e PS \_ 1 \_ 3
2.  1 + 1 = 1 istruzione aritmetica + 1 istruzione di trama

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




