---
description: Dopo che tutte le operazioni di file desiderate sono state accodate, è necessario eseguire il commit della coda. In questo modo verranno elaborate le operazioni dei file accodati.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Commit di una coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759791"
---
# <a name="committing-a-queue"></a><span data-ttu-id="7d2b7-104">Commit di una coda</span><span class="sxs-lookup"><span data-stu-id="7d2b7-104">Committing a Queue</span></span>

<span data-ttu-id="7d2b7-105">Dopo che tutte le operazioni di file desiderate sono state accodate, è necessario eseguire il commit della coda.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="7d2b7-106">In questo modo verranno elaborate le operazioni dei file accodati.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="7d2b7-107">Non è possibile riutilizzare una coda di file dopo che è stato eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="7d2b7-108">La procedura consigliata consiste nel raccogliere tutte le operazioni di file necessarie per la coda di file ed eseguire il commit della coda una sola volta.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="7d2b7-109">Se è necessaria un'elaborazione aggiuntiva della coda dopo che è stato eseguito il commit, è necessario chiudere l'handle per la coda e creare una nuova coda di file.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="7d2b7-110">Per eseguire il commit della coda di file, chiamare la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , specificando una routine di callback.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="7d2b7-111">La routine di callback riceverà le notifiche da **SetupCommitFileQueue** durante l'elaborazione delle operazioni sui file.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="7d2b7-112">Se si desidera utilizzare la routine di callback della coda predefinita, è innanzitutto necessario inizializzare il contesto necessario chiamando [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="7d2b7-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="7d2b7-113">Per ulteriori informazioni sulla routine di callback della coda predefinita, vedere [routine di callback](default-queue-callback-routine.md)della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="7d2b7-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) deve essere chiamato prima che la coda venga chiusa.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="7d2b7-115">Tutte le operazioni di cui non è stato eseguito il commit quando viene chiamato [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) non verranno eseguite.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



