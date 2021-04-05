---
title: Funzione type_free_inst
description: Gli stub chiamano la \_ funzione Inst gratuita del tipo \_ per liberare la memoria associata al tipo presentato.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856165"
---
# <a name="the-type_free_inst-function"></a>\_Funzione Inst gratuita del tipo \_

Gli stub chiamano la **funzione \_ \_ inst gratuita del tipo** per liberare la memoria associata al tipo presentato. La funzione è definita come segue:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Il parametro punta all'istanza del tipo presentata. Questo oggetto non deve essere liberato. Per una discussione su quando chiamare la funzione, vedere [l'attributo trasmissione \_ As](the-transmit-as-attribute.md).

Nell'esempio seguente, l'elenco collegato doppio viene liberato scorrendo l'elenco fino alla fine, quindi eseguendo il backup e liberando ogni elemento dell'elenco.


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




