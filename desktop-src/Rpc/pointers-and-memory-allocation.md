---
title: Puntatori e allocazione di memoria
description: La possibilità di modificare la memoria tramite puntatori spesso richiede che il server e il client allochino memoria sufficiente per gli elementi nella matrice.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118231"
---
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="a4407-103">Puntatori e allocazione di memoria</span><span class="sxs-lookup"><span data-stu-id="a4407-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="a4407-104">La possibilità di modificare la memoria tramite puntatori spesso richiede che il server e il client allochino memoria sufficiente per gli elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a4407-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="a4407-105">Quando uno stub deve allocare o liberare memoria, chiama funzioni della libreria di run-time che a loro volta chiamano le funzioni [**MIDL \_ User \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e l' [**\_ utente MIDL \_ Free**](/windows/desktop/Midl/midl-user-free-1).</span><span class="sxs-lookup"><span data-stu-id="a4407-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="a4407-106">Queste funzioni non sono incluse come parte della libreria di Runtime.</span><span class="sxs-lookup"><span data-stu-id="a4407-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="a4407-107">È necessario scrivere versioni personalizzate di queste funzioni e collegarle all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4407-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="a4407-108">In questo modo, è possibile decidere come gestire la memoria.</span><span class="sxs-lookup"><span data-stu-id="a4407-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="a4407-109">Quando si compila il file IDL in modalità OSF-Compatibility (**/OSF**), non è necessario implementare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="a4407-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="a4407-110">È necessario scrivere queste funzioni nei prototipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4407-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="a4407-111">Ad esempio, le versioni di queste funzioni per un'applicazione possono semplicemente chiamare funzioni della libreria standard:</span><span class="sxs-lookup"><span data-stu-id="a4407-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 