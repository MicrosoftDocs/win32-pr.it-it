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
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="0494a-104">Tipo \_ dalla \_ funzione Xmit</span><span class="sxs-lookup"><span data-stu-id="0494a-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="0494a-105">Gli stub chiamano il **tipo \_ dalla funzione \_ Xmit** per convertire i dati dal tipo trasmesso al tipo presentato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0494a-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="0494a-106">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="0494a-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="0494a-107">Il primo parametro è un puntatore ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="0494a-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="0494a-108">La funzione imposta il secondo parametro in modo che punti ai dati presentati.</span><span class="sxs-lookup"><span data-stu-id="0494a-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="0494a-109">Il **tipo della funzione \_ \_ Xmit** deve gestire la memoria per il tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="0494a-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="0494a-110">La funzione deve allocare memoria per l'intera struttura di dati che inizia dall'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e la passa alla funzione).</span><span class="sxs-lookup"><span data-stu-id="0494a-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="0494a-111">Il valore del secondo parametro non può essere modificato durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="0494a-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="0494a-112">La funzione può modificare il contenuto in corrispondenza di tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="0494a-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="0494a-113">In questo esempio, il tipo di collegamento doppio della funzione \_ \_ \_ da \_ Xmit converte la matrice di dimensioni in un elenco a collegamento doppio.</span><span class="sxs-lookup"><span data-stu-id="0494a-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="0494a-114">La funzione mantiene il puntatore valido all'inizio dell'elenco, libera la memoria associata al resto dell'elenco, quindi crea un nuovo elenco che inizia con lo stesso puntatore.</span><span class="sxs-lookup"><span data-stu-id="0494a-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="0494a-115">La funzione usa una funzione di utilità, **InsertNewNode**, per aggiungere un nodo elenco alla fine dell'elenco e per assegnare i puntatori *pNext* e *pPrevious* ai valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="0494a-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


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



 

 




