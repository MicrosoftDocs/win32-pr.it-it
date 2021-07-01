---
title: Modificatori per ps_1_X
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Informazioni sui modificatori per ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129940"
---
# <a name="modifiers-for-ps_1_x"></a>Modificatori per ps \_ 1 \_ X

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Ad esempio, usarli per moltiplicare o dividere il risultato per un fattore di due o per stringere il risultato tra zero e uno. I modificatori di istruzione vengono applicati dopo l'esecuzione dell'istruzione, ma prima di scrivere il risultato nel registro di destinazione.

Di seguito è riportato un elenco dei modificatori.



| Modificatore | Descrizione                   | Sintassi           | Versione 1 \_ 1 | Versione 1 \_ 2     |Versione 1 \_ 3    | Versione 1 \_ 4    |
|----------|-------------------------------|------------------|---------|------|------|------|
| \_x2     | Moltiplicare per 2                 | istruzione \_ x2  | X       | X    | X    | X    |
| \_x4     | Moltiplicare per 4                 | istruzione \_ x4  | X       | X    | X    | X    |
| \_x8     | Moltiplicare per 8                 | istruzione \_ x8  |         |      |      | X    |
| \_d2     | Dividere per 2                   | istruzione \_ d2  | X       | X    | X    | X    |
| \_d4     | Dividere per 4                   | istruzione \_ d4  |         |      |      | X    |
| \_d8     | Dividere per 8                   | istruzione \_ d8  |         |      |      | X    |
| \_Sab    | Saturazione (chiusura da 0 e 1) | istruzione \_ sab | X       | X    | X    | X    |



 

-   Il modificatore multiply moltiplica i dati del registro per una potenza di due dopo la lettura. Questo è lo stesso di uno spostamento a sinistra.
-   Il modificatore divide divide i dati del registro per una potenza di due dopo la lettura. Questo è lo stesso di uno spostamento a destra.
-   Il modificatore saturate stringe l'intervallo di valori di registro da zero a uno.

I modificatori di istruzione possono essere usati nelle istruzioni aritmetiche. Non possono essere usati nelle istruzioni relative all'indirizzo della trama.

Modificatore Multiply

Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e moltiplica il risultato per due.


```
add_x2 dest, src0, src1
```



In questo esempio vengono combinati due modificatori di istruzione. In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1). Il risultato viene quindi moltiplicato per due e con un intervallo compreso tra 0,0 e 1,0 per ogni componente. Il risultato viene salvato nel registro di destinazione.


```
add_x2_sat dest, src0, src1
```



Modificatore divide

Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e divide il risultato per due.


```
add_d2 dest, src0, src1
```



Modificatore Saturate

Per le istruzioni aritmetiche, il modificatore di saturazione consente di impostare il risultato di questa istruzione nell'intervallo da 0.0 a 1.0 per ogni componente. Nell'esempio seguente viene illustrato come usare questo modificatore di istruzione.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Questa operazione si verifica dopo qualsiasi modificatore di istruzione di moltiplicazione o divisione. \_sat viene usato più spesso per stringere i risultati del prodotto del punto. Tuttavia, consente anche l'emulazione coerente dei metodi multipass in cui il buffer dei frame è sempre compreso nell'intervallo da 0 a 1 e della sintassi multitesto DirectX 6 e 7.0, in cui la saturazione è definita per verificarsi in ogni fase.

In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e il risultato viene inserito nell'intervallo da 0,0 a 1,0 per ogni componente.


```
add_sat dest, src0, src1
```



In questo esempio vengono combinati due modificatori di istruzione. In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1). Il risultato viene moltiplicato per due e con un intervallo compreso tra 0,0 e 1,0 per ogni componente. Il risultato viene salvato nel registro di destinazione.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




