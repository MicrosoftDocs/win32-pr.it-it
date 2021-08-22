---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 istruzioni
description: Questa sezione contiene informazioni di riferimento per pixel shader istruzioni della versione 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 217e207d2f60d39979c7117cb48e0cb033fd98c6fbfb419642ff43e59759d510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119735"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Istruzioni

Questa sezione contiene informazioni di riferimento per le istruzioni pixel shader versione 1 \_ X.

Esistono diversi tipi di istruzioni pixel shader, come illustrato nella tabella seguente.

## <a name="instruction-set"></a>Set di istruzioni



| Versione                                    | Descrizione                                                                   | Slot di istruzioni | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [Ps](ps---ps.md)                          | Numero di versione                                                                | 0                 | x    | x    | x    | x    |
| Istruzioni costanti                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def - ps](def---ps.md)                   | Definire costanti                                                              | 0                 | x    | x    | x    | x    |
| Istruzioni per le fasi                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [phase - ps](phase---ps.md)               | Transizione tra la fase 1 e la fase 2                                        | 0                 |      |      |      | x    |
| Istruzioni aritmetiche                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [add - ps](add---ps.md)                   | Aggiungere due vettori                                                               | 1                 | x    | x    | x    | x    |
| [bem - ps](bem---ps.md)                   | Applicare una trasformazione mappa ambiente di urto fittizia                                   | 2                 |      |      |      | x    |
| [cmp - ps](cmp---ps.md)                   | Confrontare l'origine con 0                                                           | 1 più                |      | x    | x    | x    |
| [cnd - ps](cnd---ps.md)                   | Confrontare l'origine con la versione 0.5                                                         | 1                 | x    | x    | x    | x    |
| [dp3 - ps](dp3---ps.md)                   | Prodotto punto a tre componenti                                                   | 1                 | x    | x    | x    | x    |
| [dp4 - ps](dp4---ps.md)                   | Prodotto punto a quattro componenti                                                    | 1 più                |      | x    | x    | x    |
| [lrp - ps](lrp---ps.md)                   | Interpolazione lineare                                                            | 1                 | x    | x    | x    | x    |
| [mad - ps](mad---ps.md)                   | Moltiplicare e aggiungere                                                              | 1                 | x    | x    | x    | x    |
| [mov - ps](mov---ps.md)                   | Spostamento                                                                          | 1                 | x    | x    | x    | x    |
| [mul - ps](mul---ps.md)                   | Moltiplicazione                                                                      | 1                 | x    | x    | x    | x    |
| [nop - ps](nop---ps.md)                   | Nessuna operazione                                                                  | 0                 | x    | x    | x    | x    |
| [sub - ps](sub---ps.md)                   | Sottrazione                                                                      | 1                 | x    | x    | x    | x    |
| Istruzioni per la trama                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex - ps](tex---ps.md)                   | Campionare una trama                                                              | 1                 | x    | x    | x    |      |
| [texbem - ps](texbem---ps.md)             | Applicare una trasformazione mappa ambiente di urto fittizia                                   | 1                 | x    | x    | x    |      |
| [texbeml - ps](texbeml---ps.md)           | Applicare una trasformazione mappa dell'ambiente di urto fittizia con correzione della luminance         | 1+1 PIÙ              | x    | x    | x    |      |
| [texcoord - ps](texcoord---ps.md)         | Interpretare i dati delle coordinate della trama come dati di colore                               | 1                 | x    | x    | x    |      |
| [texcrd - ps](texcrd---ps.md)             | Copiare i dati delle coordinate della trama come dati di colore                                    | 1                 |      |      |      | x    |
| [texdepth - ps](texdepth---ps.md)         | Calcolare i valori di profondità                                                        | 1                 |      |      |      | x    |
| [texdp3 - ps](texdp3---ps.md)             | Prodotto punto a tre componenti tra i dati della trama e le coordinate della trama  | 1                 |      | x    | x    |      |
| [texdp3tex - ps](texdp3tex---ps.md)       | Prodotto a tre componenti e ricerca di trame 1D                             | 1                 |      | x    | x    |      |
| [texkill - ps](texkill---ps.md)           | Annulla il rendering dei pixel in base a un confronto                             | 1                 | x    | x    | x    | x    |
| [texld - ps \_ 1 \_ 4](texld---ps-1-4.md)     | Campionare una trama                                                              | 1                 |      |      |      | x    |
| [texm3x2depth - ps](texm3x2depth---ps.md) | Calcolare i valori di profondità per pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad - ps](texm3x2pad---ps.md)     | Moltiplicazione della prima matrice di righe di una matrice a due righe                        | 1                 | x    | x    | x    |      |
| [texm3x2tex - ps](texm3x2tex---ps.md)     | Moltiplicazione della matrice di righe finale di una matrice di due righe                        | 1                 | x    | x    | x    |      |
| [texm3x3 - ps](texm3x3---ps.md)           | Moltiplicazione di matrice 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad - ps](texm3x3pad---ps.md)     | Moltiplicazione della prima o della seconda riga di una matrice di tre righe                   | 1                 | x    | x    | x    |      |
| [texm3x3spec - ps](texm3x3spec---ps.md)   | Moltiplicazione di riga finale di una moltiplicazione di matrice a tre righe                             | 1                 | x    | x    | x    |      |
| [texm3x3tex - ps](texm3x3tex---ps.md)     | Ricerca di trame usando una moltiplicazione di matrice 3x3                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec - ps](texm3x3vspec---ps.md) | Ricerca della trama usando una moltiplicazione di matrice 3x3, con vettore di raggi oculare non costante | 1                 | x    | x    | x    |      |
| [texreg2ar - ps](texreg2ar---ps.md)       | Campionare una trama usando i componenti alfa e rosso                           | 1                 | x    | x    | x    |      |
| [texreg2gb - ps](texreg2gb---ps.md)       | Campionare una trama usando i componenti verde e blu                          | 1                 | x    | x    | x    |      |
| [texreg2rgb - ps](texreg2rgb---ps.md)     | Campionare una trama usando i componenti rosso, verde e blu                     | 1                 |      | x    | x    |      |



 

1.  1 slot in ps \_ 1 \_ 4; 2 slot in ps \_ 1 \_ 2 e ps \_ 1 \_ 3
2.  1 + 1 = 1 istruzione aritmetica + 1 istruzione di trama

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




