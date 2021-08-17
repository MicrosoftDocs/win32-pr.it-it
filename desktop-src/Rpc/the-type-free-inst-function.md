---
title: Funzione type_free_inst
description: Gli stub chiamano la funzione inst gratuita del tipo \_ per liberare la memoria \_ associata al tipo presentato.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc71c8d3557c62eec39fe9a90855ef3ed057d29c21ec60a82ddc7fe04207f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923710"
---
# <a name="the-type_free_inst-function"></a>Funzione \_ \_ inst type free

Gli stub chiamano la **funzione \_ \_ inst** gratuita del tipo per liberare la memoria associata al tipo presentato. La funzione è definita come:

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

Il parametro punta all'istanza del tipo presentato. Questo oggetto non deve essere liberato. Per una discussione su quando chiamare la funzione, vedere [ \_ Trasmissione come attributo](the-transmit-as-attribute.md).

Nell'esempio seguente l'elenco a doppio collegamento viene liberato tramite la visualizzazione dell'elenco fino alla fine, quindi il backup e la libera di ogni elemento dell'elenco.


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



 

 




