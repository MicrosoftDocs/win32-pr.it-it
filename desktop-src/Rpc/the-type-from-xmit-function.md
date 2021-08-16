---
title: Funzione type_from_xmit
description: Gli stub chiamano il tipo dalla funzione xmit per convertire i dati dal tipo trasmesso al tipo \_ \_ presentato all'applicazione.
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a38e372467208c76111728080037c65f5dca2856304a49f06e7e33426277eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923700"
---
# <a name="the-type_from_xmit-function"></a>Tipo \_ della \_ funzione xmit

Gli stub chiamano il **tipo \_ dalla funzione \_ xmit** per convertire i dati dal tipo trasmesso al tipo presentato all'applicazione. La funzione è definita come:

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati trasmessi. La funzione imposta il secondo parametro in modo che punti ai dati presentati.

Il **tipo della funzione \_ \_ xmit** deve gestire la memoria per il tipo presentato. La funzione deve allocare memoria per l'intera struttura di dati che inizia in corrispondenza dell'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e lo passa alla funzione). Il valore del secondo parametro non può cambiare durante la chiamata. La funzione può modificare il contenuto in corrispondenza di tale indirizzo.

In questo esempio la funzione DOUBLE \_ LINK \_ TYPE di \_ xmit converte la matrice \_ dimensionata in un elenco collegato doppio. La funzione mantiene il puntatore valido all'inizio dell'elenco, libera la memoria associata al resto dell'elenco, quindi crea un nuovo elenco che inizia in corrispondenza dello stesso puntatore. La funzione usa una funzione di utilità, **InsertNewNode**, per aggiungere un nodo elenco alla fine dell'elenco e assegnare i puntatori *pNext* e *pPrevious* ai valori appropriati.


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



 

 




