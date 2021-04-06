---
title: Funzione type_from_xmit
description: Gli stub chiamano il tipo \_ dalla \_ funzione Xmit per convertire i dati dal tipo trasmesso al tipo presentato all'applicazione.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045157"
---
# <a name="the-type_from_xmit-function"></a>Tipo \_ dalla \_ funzione Xmit

Gli stub chiamano il **tipo \_ dalla funzione \_ Xmit** per convertire i dati dal tipo trasmesso al tipo presentato all'applicazione. La funzione è definita come segue:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati trasmessi. La funzione imposta il secondo parametro in modo che punti ai dati presentati.

Il **tipo della funzione \_ \_ Xmit** deve gestire la memoria per il tipo presentato. La funzione deve allocare memoria per l'intera struttura di dati che inizia dall'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e la passa alla funzione). Il valore del secondo parametro non può essere modificato durante la chiamata. La funzione può modificare il contenuto in corrispondenza di tale indirizzo.

In questo esempio, il tipo di collegamento doppio della funzione \_ \_ \_ da \_ Xmit converte la matrice di dimensioni in un elenco a collegamento doppio. La funzione mantiene il puntatore valido all'inizio dell'elenco, libera la memoria associata al resto dell'elenco, quindi crea un nuovo elenco che inizia con lo stesso puntatore. La funzione usa una funzione di utilità, **InsertNewNode**, per aggiungere un nodo elenco alla fine dell'elenco e per assegnare i puntatori *pNext* e *pPrevious* ai valori appropriati.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




