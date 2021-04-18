---
description: Al termine del commit delle operazioni da parte della coda, è necessario chiuderla utilizzando la funzione SetupCloseFileQueue con l'handle creato da SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Chiusura della coda di file e del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319335"
---
# <a name="closing-the-file-queue-and-inf-file"></a><span data-ttu-id="fd512-103">Chiusura della coda di file e del file INF</span><span class="sxs-lookup"><span data-stu-id="fd512-103">Closing the File Queue and INF File</span></span>

<span data-ttu-id="fd512-104">Al termine del commit delle operazioni da parte della coda, è necessario chiuderla utilizzando la funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="fd512-104">After the queue has finished committing its operations, it should be closed using the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span> <span data-ttu-id="fd512-105">Il callback predefinito della coda deve essere eliminato e ricreato prima che sia possibile eseguire il commit di un'altra coda.</span><span class="sxs-lookup"><span data-stu-id="fd512-105">The default queue callback must be destroyed and recreated before another queue can be committed.</span></span>

<span data-ttu-id="fd512-106">Se è stato avviato un contesto predefinito per l'utilizzo da parte della routine di callback predefinita, è necessario terminare anche chiamando la funzione [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="fd512-106">If a default context was initiated for use by the default callback routine, it should also be terminated by calling the [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) function.</span></span> <span data-ttu-id="fd512-107">Il *contesto* è un puntatore alla struttura restituita dalla funzione [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .</span><span class="sxs-lookup"><span data-stu-id="fd512-107">The *Context* is a pointer to the structure returned by the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) function.</span></span>

<span data-ttu-id="fd512-108">Quando l'accesso alle informazioni INF non è più necessario, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con l'handle creato da [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) per liberare risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd512-108">When access to the INF information is no longer needed, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function with the handle that was created by [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) to free system resources.</span></span>

 

 



