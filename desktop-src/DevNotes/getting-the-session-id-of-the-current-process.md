---
description: Nell'esempio di codice assembly x86 seguente viene ottenuto l'ID di sessione di Servizi terminal associato al processo corrente.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Recupero dell'ID di sessione del processo corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126618"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="0fbe3-103">Recupero dell'ID di sessione del processo corrente</span><span class="sxs-lookup"><span data-stu-id="0fbe3-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="0fbe3-104">\[Gli indirizzi di memoria specificati da questo codice di esempio possono cambiare nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="0fbe3-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="0fbe3-105">Per assicurarsi che l'applicazione continuerà a funzionare correttamente in futuro, l'applicazione deve chiamare [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) e quindi [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anziché il codice di esempio seguente.\]</span><span class="sxs-lookup"><span data-stu-id="0fbe3-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="0fbe3-106">Nell'esempio di codice assembly x86 seguente viene ottenuto l'ID di sessione di Servizi terminal associato al processo corrente.</span><span class="sxs-lookup"><span data-stu-id="0fbe3-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
