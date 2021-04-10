---
title: Dichiarazione di funzioni asincrone
description: Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- RPC (Remote Procedure Call), attività, dichiarazione di funzioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963531"
---
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="cc145-104">Dichiarazione di funzioni asincrone</span><span class="sxs-lookup"><span data-stu-id="cc145-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="cc145-105">Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="cc145-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="cc145-106">L'utilizzo di funzioni RPC asincrone non richiede alcuna modifica speciale al file IDL.</span><span class="sxs-lookup"><span data-stu-id="cc145-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="cc145-107">Nell'esempio seguente viene illustrato un file IDL per un'applicazione che utilizza una funzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="cc145-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

<span data-ttu-id="cc145-108">Per tutte le funzioni RPC asincrone utilizzate dall'applicazione, sarà necessario modificare la dichiarazione delle funzioni asincrone all'interno del file ACF dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc145-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="cc145-109">Applicare l'attributo [**\[ Async \]**](../midl/async.md) a ogni nome di funzione asincrona, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="cc145-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="cc145-110">Quando si applica l'attributo **\[ Async \]** nel file ACF, il compilatore MIDL genera automaticamente un parametro di handle asincrono aggiuntivo nel codice stub.</span><span class="sxs-lookup"><span data-stu-id="cc145-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 