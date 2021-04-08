---
description: La definizione di Winternl. h seguente è l'indirizzo di memoria statica dell'ID di sessione della console Servizi terminal attiva. Questo ID di sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Recupero dell'ID di sessione della console attiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877641"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="5008e-104">Recupero dell'ID di sessione della console attiva</span><span class="sxs-lookup"><span data-stu-id="5008e-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="5008e-105">La definizione di Winternl. h seguente è l'indirizzo di memoria statica dell'ID di sessione della console Servizi terminal attiva.</span><span class="sxs-lookup"><span data-stu-id="5008e-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="5008e-106">Questo ID di sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5008e-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="5008e-107">Questa definizione può cambiare nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="5008e-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="5008e-108">Per assicurarsi che l'applicazione continuerà a funzionare correttamente in futuro, l'applicazione deve chiamare [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span><span class="sxs-lookup"><span data-stu-id="5008e-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
