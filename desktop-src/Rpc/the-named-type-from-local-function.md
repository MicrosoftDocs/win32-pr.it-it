---
title: Funzione named_type_from_local
description: Gli stub chiamano il \_ tipo denominato \_ dalla \_ funzione locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329124"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="d9794-104">Il \_ tipo denominato \_ della \_ funzione locale</span><span class="sxs-lookup"><span data-stu-id="d9794-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="d9794-105">Gli stub chiamano il \_ tipo denominato \_ dalla \_ funzione locale.</span><span class="sxs-lookup"><span data-stu-id="d9794-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="d9794-106">Converte il tipo utilizzato dall'applicazione nel tipo in cui vengono trasmessi gli stub attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="d9794-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="d9794-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="d9794-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="d9794-108">Il primo parametro è un puntatore ai dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9794-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="d9794-109">Il secondo parametro è un puntatore a un puntatore.</span><span class="sxs-lookup"><span data-stu-id="d9794-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="d9794-110">La funzione la punta ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="d9794-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="d9794-111">La funzione deve allocare memoria per il tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="d9794-111">The function must allocate memory for the transmitted type.</span></span>

 

 




