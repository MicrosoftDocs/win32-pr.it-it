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
# <a name="the-type_free_inst-function"></a><span data-ttu-id="15cb8-104">\_Funzione Inst gratuita del tipo \_</span><span class="sxs-lookup"><span data-stu-id="15cb8-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="15cb8-105">Gli stub chiamano la **funzione \_ \_ inst gratuita del tipo** per liberare la memoria associata al tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="15cb8-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="15cb8-106">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="15cb8-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="15cb8-107">Il parametro punta all'istanza del tipo presentata.</span><span class="sxs-lookup"><span data-stu-id="15cb8-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="15cb8-108">Questo oggetto non deve essere liberato.</span><span class="sxs-lookup"><span data-stu-id="15cb8-108">This object should not be freed.</span></span> <span data-ttu-id="15cb8-109">Per una discussione su quando chiamare la funzione, vedere [l'attributo trasmissione \_ As](the-transmit-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="15cb8-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="15cb8-110">Nell'esempio seguente, l'elenco collegato doppio viene liberato scorrendo l'elenco fino alla fine, quindi eseguendo il backup e liberando ogni elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="15cb8-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


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



 

 




