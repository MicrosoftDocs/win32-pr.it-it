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
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="92aff-104">Tipo \_ per la \_ funzione Xmit</span><span class="sxs-lookup"><span data-stu-id="92aff-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="92aff-105">Gli stub chiamano il **tipo \_ per \_** la funzione Xmit per convertire il tipo presentato dall'applicazione nel tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="92aff-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="92aff-106">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="92aff-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="92aff-107">Il primo parametro è un puntatore ai dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92aff-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="92aff-108">Il secondo parametro viene impostato dalla funzione in modo da puntare ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="92aff-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="92aff-109">La funzione deve allocare memoria per il tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="92aff-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="92aff-110">Nell'esempio seguente, il client chiama la procedura remota che dispone di un parametro **\[ in, \] out** di tipo \_ tipo collegamento doppio \_ .</span><span class="sxs-lookup"><span data-stu-id="92aff-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="92aff-111">Lo stub client chiama il **tipo \_ per \_** la funzione Xmit, in questo caso denominato doppio \_ collegamento \_ \_ a \_ Xmit, per convertire i dati dell'elenco a collegamento doppio in una matrice di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="92aff-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="92aff-112">La funzione determina il numero di elementi nell'elenco, alloca una matrice sufficientemente grande da conservare tali elementi, quindi copia gli elementi dell'elenco nella matrice.</span><span class="sxs-lookup"><span data-stu-id="92aff-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="92aff-113">Prima della restituzione della funzione, il secondo parametro, *ppArray*, viene impostato in modo da puntare alla struttura dei dati appena allocata.</span><span class="sxs-lookup"><span data-stu-id="92aff-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


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



 

 




