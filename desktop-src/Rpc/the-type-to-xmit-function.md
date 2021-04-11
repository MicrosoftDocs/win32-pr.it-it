---
title: Funzione type_to_xmit
description: Gli stub chiamano il tipo \_ per la \_ funzione Xmit per convertire il tipo presentato dall'applicazione nel tipo trasmesso.
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955688"
---
# <a name="the-type_to_xmit-function"></a>Tipo \_ per la \_ funzione Xmit

Gli stub chiamano il **tipo \_ per \_** la funzione Xmit per convertire il tipo presentato dall'applicazione nel tipo trasmesso. La funzione è definita come segue:

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati dell'applicazione. Il secondo parametro viene impostato dalla funzione in modo da puntare ai dati trasmessi. La funzione deve allocare memoria per il tipo trasmesso.

Nell'esempio seguente, il client chiama la procedura remota che dispone di un parametro **\[ in, \] out** di tipo \_ tipo collegamento doppio \_ . Lo stub client chiama il **tipo \_ per \_** la funzione Xmit, in questo caso denominato doppio \_ collegamento \_ \_ a \_ Xmit, per convertire i dati dell'elenco a collegamento doppio in una matrice di dimensioni.

La funzione determina il numero di elementi nell'elenco, alloca una matrice sufficientemente grande da conservare tali elementi, quindi copia gli elementi dell'elenco nella matrice. Prima della restituzione della funzione, il secondo parametro, *ppArray*, viene impostato in modo da puntare alla struttura dei dati appena allocata.


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



 

 




