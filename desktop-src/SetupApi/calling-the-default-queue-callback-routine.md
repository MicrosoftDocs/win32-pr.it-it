---
description: Se la routine di callback della coda predefinita viene inizializzata e specificata quando viene chiamato SetupCommitFileQueue, la coda chiama la routine di callback della coda predefinita internamente ed è necessario eseguire altre operazioni.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Chiamata della routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318625"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="c685c-103">Chiamata della routine di callback della coda predefinita</span><span class="sxs-lookup"><span data-stu-id="c685c-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="c685c-104">Se la routine di callback della coda predefinita viene inizializzata e specificata quando viene chiamato [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , la coda chiama la routine di callback della coda predefinita internamente ed è necessario eseguire altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="c685c-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="c685c-105">Se si crea una routine di callback del filtro basata sulla routine di callback della coda predefinita per gestire un subset delle notifiche della coda, la routine di callback del filtro deve chiamare [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="c685c-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c685c-106">Quando si chiama [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) in modo esplicito, è necessario passare il puntatore void restituito da [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="c685c-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="c685c-107">Un modo per eseguire questa operazione consiste nel creare una struttura di contesto per la routine di callback personalizzata che includa come uno dei suoi membri il puntatore void restituito da [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="c685c-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



