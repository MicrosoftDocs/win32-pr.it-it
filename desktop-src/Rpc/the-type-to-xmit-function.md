---
title: Funzione type_to_xmit
description: Gli stub chiamano il tipo alla funzione xmit per convertire il tipo presentato dall'applicazione \_ \_ nel tipo trasmesso.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970d4a0de9675ac7a5f1b1c1449521177ecb661a1a80fd9ef609a6dc630605a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016501"
---
# <a name="the-type_to_xmit-function"></a>Tipo per \_ \_ la funzione xmit

Gli stub chiamano il **tipo \_ alla funzione \_ xmit** per convertire il tipo presentato dall'applicazione nel tipo trasmesso. La funzione è definita come:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati dell'applicazione. Il secondo parametro viene impostato dalla funzione in modo che punti ai dati trasmessi. La funzione deve allocare memoria per il tipo trasmesso.

Nell'esempio seguente il client chiama la procedura remota con un **\[ parametro in, out \]** di tipo DOUBLE LINK \_ \_ TYPE. Lo stub client chiama il tipo alla funzione **\_ \_ xmit,** qui denominata DOUBLE LINK TYPE in xmit, per convertire i dati dell'elenco collegato doppio \_ in una matrice di \_ \_ \_ dimensioni.

La funzione determina il numero di elementi nell'elenco, alloca una matrice sufficientemente grande da contenere tali elementi, quindi copia gli elementi dell'elenco nella matrice. Prima che la funzione venga restituita, il secondo parametro, *ppArray*, viene impostato in modo che punti alla struttura di dati appena allocata.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




