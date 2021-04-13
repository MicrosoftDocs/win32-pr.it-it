---
title: attributo midl_user_free
description: La funzione della versione \_ gratuita dell'utente MIDL \_ viene fornita dalle applicazioni client e server per deallocare la memoria allocata in modo dinamico.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- attributo midl_user_free MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337166"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="02b39-104">\_attributo gratuito dell'utente MIDL \_</span><span class="sxs-lookup"><span data-stu-id="02b39-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="02b39-105">La funzione della versione **\_ \_ gratuita dell'utente MIDL** viene fornita dalle applicazioni client e server per deallocare la memoria allocata in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="02b39-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="02b39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02b39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b39-107">*p*</span><span class="sxs-lookup"><span data-stu-id="02b39-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="02b39-108">Puntatore al blocco di memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="02b39-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02b39-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="02b39-109">Remarks</span></span>

<span data-ttu-id="02b39-110">Sia l'applicazione client che l'applicazione server devono implementare la funzione **MIDL \_ User \_ Free** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="02b39-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="02b39-111">La **funzione \_ User \_ Free MIDL** deve essere in grado di liberare tutte le archiviazioni allocate dall' [**\_ utente MIDL \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="02b39-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="02b39-112">Le applicazioni e gli stub chiamano l' **\_ utente MIDL \_ gratuitamente** quando si gestiscono oggetti a cui fanno riferimento i puntatori:</span><span class="sxs-lookup"><span data-stu-id="02b39-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="02b39-113">L'applicazione server deve chiamare **l' \_ utente MIDL \_ gratuitamente** per liberare la memoria allocata da ApplicationA ", ad esempio quando si elimina un nodo specificato.</span><span class="sxs-lookup"><span data-stu-id="02b39-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="02b39-114">Lo stub del server chiama l' **\_ utente MIDL \_ gratuitamente** a rilasciare la memoria nel server dopo aver eseguito il marshalling di tutti gli **\[** argomenti [**out**](out-idl.md) **\]** , **\[** [**in**](in.md), **\] out** arguments e il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="02b39-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="02b39-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="02b39-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="02b39-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02b39-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b39-117">**matrici**</span><span class="sxs-lookup"><span data-stu-id="02b39-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="02b39-118">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="02b39-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="02b39-119">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="02b39-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="02b39-120">**in**</span><span class="sxs-lookup"><span data-stu-id="02b39-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="02b39-121">**\_alloca utente \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="02b39-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="02b39-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="02b39-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="02b39-123">**out**</span><span class="sxs-lookup"><span data-stu-id="02b39-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="02b39-124">**unico**</span><span class="sxs-lookup"><span data-stu-id="02b39-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 