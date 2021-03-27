---
title: Modificatori per ps_1_X
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856958"
---
# <a name="modifiers-for-ps_1_x"></a>Modificatori per PS \_ 1 \_ X

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione. Usare, ad esempio, per moltiplicare o dividere il risultato per un fattore di due o per bloccare il risultato tra zero e uno. I modificatori di istruzione vengono applicati dopo l'esecuzione dell'istruzione, ma prima di scrivere il risultato nel registro di destinazione.

Di seguito è riportato un elenco dei modificatori.



| Modificatore | Descrizione                   | Sintassi           | Versione |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_X2     | Moltiplica per 2                 | istruzione \_ X2  | X       | X    | X    | X    |
| \_X4     | Moltiplica per 4                 | istruzioni \_ X4  | X       | X    | X    | X    |
| \_X8     | Moltiplica per 8                 | istruzione \_ x8  |         |      |      | X    |
| \_D2     | Divisione per 2                   | istruzioni \_ D2  | X       | X    | X    | X    |
| \_D4     | Divisione per 4                   | istruzione \_ D4  |         |      |      | X    |
| \_D8     | Divisione per 8                   | istruzione \_ D8  |         |      |      | X    |
| \_Sat    | Satura (morsetto da 0 a 1) | istruzioni \_ Sat | X       | X    | X    | X    |



 

-   Il modificatore Multiply Moltiplica i dati del registro per una potenza di due dopo che è stata letta. Si tratta dello stesso valore di Shift Left.
-   Il modificatore divide divide i dati del registro per una potenza di due dopo che è stato letto. Si tratta della stessa operazione di spostamento a destra.
-   Il modificatore di saturazione blocca l'intervallo di valori di registro da zero a uno.

I modificatori di istruzione possono essere utilizzati nelle istruzioni aritmetiche. Non possono essere usate nelle istruzioni relative all'indirizzo della trama.

Modificatore Multiply

In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e viene moltiplicato per due il risultato.


```
add_x2 dest, src0, src1
```



In questo esempio vengono combinati due modificatori di istruzione. In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1). Il risultato viene quindi moltiplicato per due e fissato tra 0,0 e 1,0 per ogni componente. Il risultato viene salvato nel registro di destinazione.


```
add_x2_sat dest, src0, src1
```



Modificatore di divisione

In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e il risultato viene diviso per due.


```
add_d2 dest, src0, src1
```



Modificatore saturazione

Per istruzioni aritmetiche, il modificatore di saturazione blocca il risultato di questa istruzione nell'intervallo compreso tra 0,0 e 1,0 per ogni componente. Nell'esempio seguente viene illustrato come utilizzare questo modificatore di istruzioni.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Questa operazione si verifica dopo qualsiasi modificatore di istruzione Multiply o divide. \_Sat viene usato più spesso per bloccare i risultati dei prodotti in un punto. Tuttavia, consente anche un'emulazione coerente di metodi MultiPASS, in cui il buffer dei frame è sempre compreso tra 0 e 1 e la sintassi multitrama di DirectX 6 e 7,0, in cui la saturazione viene definita in ogni fase.

Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e blocca il risultato nell'intervallo compreso tra 0,0 e 1,0 per ogni componente.


```
add_sat dest, src0, src1
```



In questo esempio vengono combinati due modificatori di istruzione. In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1). Il risultato viene moltiplicato per due e fissato tra 0,0 e 1,0 per ogni componente. Il risultato viene salvato nel registro di destinazione.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




