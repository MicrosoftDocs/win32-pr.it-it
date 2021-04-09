---
description: Nell'esempio seguente viene illustrato come viene utilizzato un gestore di terminazione per garantire che le risorse vengano rilasciate quando viene terminata l'esecuzione di un corpo sorvegliato di codice.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Uso di un gestore di terminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966125"
---
# <a name="using-a-termination-handler"></a><span data-ttu-id="7b4d0-103">Uso di un gestore di terminazione</span><span class="sxs-lookup"><span data-stu-id="7b4d0-103">Using a Termination Handler</span></span>

<span data-ttu-id="7b4d0-104">Nell'esempio seguente viene illustrato come viene utilizzato un gestore di terminazione per garantire che le risorse vengano rilasciate quando viene terminata l'esecuzione di un corpo sorvegliato di codice.</span><span class="sxs-lookup"><span data-stu-id="7b4d0-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="7b4d0-105">In questo caso, un thread utilizza la funzione [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) per attendere la proprietà di un oggetto della sezione critica.</span><span class="sxs-lookup"><span data-stu-id="7b4d0-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="7b4d0-106">Al termine dell'esecuzione del codice protetto dalla sezione critica, il thread deve chiamare la funzione [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) per rendere disponibile l'oggetto sezione critica ad altri thread.</span><span class="sxs-lookup"><span data-stu-id="7b4d0-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="7b4d0-107">L'utilizzo di un gestore di terminazione garantisce che questa operazione verrà eseguita.</span><span class="sxs-lookup"><span data-stu-id="7b4d0-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="7b4d0-108">Per ulteriori informazioni, vedere [oggetti sezione critica](../sync/critical-section-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b4d0-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
