---
description: "Quando la funzione SetupCommitFileQueue esegue il commit della coda di file, elabora le operazioni sui file nell'ordine seguente: operazioni di eliminazione di file, quindi operazioni di ridenominazione dei file e infine operazioni di copia dei file."
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordine di impegno della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882361"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="a17d0-103">Ordine di impegno della coda</span><span class="sxs-lookup"><span data-stu-id="a17d0-103">Order of Queue Commitment</span></span>

<span data-ttu-id="a17d0-104">Quando la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) esegue il commit della coda di file, elabora le operazioni sui file nell'ordine seguente: operazioni di eliminazione di file, quindi operazioni di ridenominazione dei file e infine operazioni di copia dei file.</span><span class="sxs-lookup"><span data-stu-id="a17d0-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="a17d0-105">Nella struttura seguente viene illustrato il ciclo di vita del processo di impegno di una coda.</span><span class="sxs-lookup"><span data-stu-id="a17d0-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="a17d0-106">avvia la coda secondaria Delete</span><span class="sxs-lookup"><span data-stu-id="a17d0-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="a17d0-107">avvia un'operazione di eliminazione file <--REPEAT per ogni</span><span class="sxs-lookup"><span data-stu-id="a17d0-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="a17d0-108">termina un'operazione di eliminazione file <--eliminazione file in coda</span><span class="sxs-lookup"><span data-stu-id="a17d0-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="a17d0-109">terminare la coda secondaria Delete</span><span class="sxs-lookup"><span data-stu-id="a17d0-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="a17d0-110">avviare la ridenominazione della coda secondaria</span><span class="sxs-lookup"><span data-stu-id="a17d0-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="a17d0-111">avviare un'operazione di ridenominazione dei file <--REPEAT per ogni</span><span class="sxs-lookup"><span data-stu-id="a17d0-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="a17d0-112">termina un'operazione di eliminazione file <--Rinomina file in coda</span><span class="sxs-lookup"><span data-stu-id="a17d0-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="a17d0-113">terminare la ridenominazione della coda secondaria</span><span class="sxs-lookup"><span data-stu-id="a17d0-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="a17d0-114">avviare la copia subque</span><span class="sxs-lookup"><span data-stu-id="a17d0-114">start the copy subque</span></span>
    -   <span data-ttu-id="a17d0-115">avviare un'operazione di copia dei file <--REPEAT per ogni</span><span class="sxs-lookup"><span data-stu-id="a17d0-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="a17d0-116">termina un'operazione di copia file < la copia del file in coda</span><span class="sxs-lookup"><span data-stu-id="a17d0-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="a17d0-117">terminare la coda secondaria di copia</span><span class="sxs-lookup"><span data-stu-id="a17d0-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="a17d0-118">termina la coda</span><span class="sxs-lookup"><span data-stu-id="a17d0-118">finish the queue</span></span>

 

<span data-ttu-id="a17d0-119">A ogni passaggio o, se si verifica un errore, la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) invia una notifica alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="a17d0-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="a17d0-120">La routine di callback può utilizzare le informazioni inviate dalla coda per tenere traccia dello stato di avanzamento dell'installazione e, se necessario, interagire con l'utente.</span><span class="sxs-lookup"><span data-stu-id="a17d0-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="a17d0-121">Se, ad esempio, un'operazione di copia file richiede un file di origine non disponibile nel percorso corrente, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) invierà una \_ notifica SPFILENOTIFY NEEDMEDIA alla routine di callback, insieme alle informazioni sul file e sui supporti necessari.</span><span class="sxs-lookup"><span data-stu-id="a17d0-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="a17d0-122">La routine di callback può utilizzare queste informazioni per generare una finestra di dialogo in cui viene richiesto all'utente di inserire il disco successivo chiamando [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="a17d0-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="a17d0-123">Con l'API di installazione di è inclusa una routine di callback della coda predefinita, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka).</span><span class="sxs-lookup"><span data-stu-id="a17d0-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="a17d0-124">Questa routine gestisce le notifiche della coda e genera finestre di dialogo di errore e indicatori di stato per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a17d0-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="a17d0-125">È possibile utilizzare la routine di callback della coda predefinita, oppure scrivere una routine di callback del filtro per gestire un subset delle notifiche e passare le altre alla routine di callback della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="a17d0-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="a17d0-126">Se nessuna delle funzionalità della routine di callback soddisfa le proprie esigenze, è possibile scrivere una routine di callback personalizzata autonoma che non chiami la routine di callback della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="a17d0-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="a17d0-127">Per altre informazioni sulle routine di callback della coda, vedere [routine di callback della coda predefinita](default-queue-callback-routine.md)e [creazione di una routine di callback della coda personalizzata](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="a17d0-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



