---
title: Funzione type_free_xmit
description: Gli stub chiamano il tipo \_ Free \_ Xmit Function per liberare la memoria associata ai dati trasmessi.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221508"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="cc477-104">\_Funzione Xmit gratuita del tipo \_</span><span class="sxs-lookup"><span data-stu-id="cc477-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="cc477-105">Gli stub chiamano il **tipo \_ Free \_ Xmit** Function per liberare la memoria associata ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="cc477-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="cc477-106">Quando il [tipo della funzione \_ \_ Xmit](the-type-from-xmit-function.md) converte i dati trasmessi nel tipo presentato, la memoria non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="cc477-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="cc477-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="cc477-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="cc477-108">Il parametro è un puntatore alla memoria che contiene il tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="cc477-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="cc477-109">In questo esempio la memoria contiene una matrice che si trova in una singola struttura.</span><span class="sxs-lookup"><span data-stu-id="cc477-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="cc477-110">Il \_ tipo di collegamento doppia della funzione \_ \_ \_ Xmit Free USA la funzione fornita dall'utente MIDL \_ User \_ Free per liberare la memoria:</span><span class="sxs-lookup"><span data-stu-id="cc477-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




