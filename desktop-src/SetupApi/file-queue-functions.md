---
description: Le funzioni seguenti vengono utilizzate con le code di file.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funzioni della coda di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314655"
---
# <a name="file-queue-functions"></a><span data-ttu-id="04b88-103">Funzioni della coda di file</span><span class="sxs-lookup"><span data-stu-id="04b88-103">File Queue Functions</span></span>

<span data-ttu-id="04b88-104">Le funzioni seguenti vengono utilizzate con le code di file.</span><span class="sxs-lookup"><span data-stu-id="04b88-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="04b88-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="04b88-105">Function</span></span>                                                             | <span data-ttu-id="04b88-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04b88-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04b88-107">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="04b88-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="04b88-108">Termina la coda.</span><span class="sxs-lookup"><span data-stu-id="04b88-108">Terminates the queue.</span></span> <span data-ttu-id="04b88-109">Non viene eseguito il commit di tutte le transazioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="04b88-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="04b88-110">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="04b88-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="04b88-111">Esegui il commit di tutte le transazioni in coda.</span><span class="sxs-lookup"><span data-stu-id="04b88-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="04b88-112">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="04b88-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="04b88-113">Inizializza e restituisce un handle per la coda di file.</span><span class="sxs-lookup"><span data-stu-id="04b88-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="04b88-114">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="04b88-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="04b88-115">Richiede all'utente di riavviare il computer, se necessario.</span><span class="sxs-lookup"><span data-stu-id="04b88-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="04b88-116">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="04b88-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="04b88-117">Accoda una copia del file.</span><span class="sxs-lookup"><span data-stu-id="04b88-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="04b88-118">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="04b88-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="04b88-119">Accoda i file in una sezione dei file di copia INF.</span><span class="sxs-lookup"><span data-stu-id="04b88-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="04b88-120">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="04b88-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="04b88-121">Accoda i file in una sezione dei file di copia INF usando le informazioni predefinite specificate in un file INF.</span><span class="sxs-lookup"><span data-stu-id="04b88-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="04b88-122">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="04b88-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="04b88-123">Accoda un'eliminazione di file.</span><span class="sxs-lookup"><span data-stu-id="04b88-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="04b88-124">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="04b88-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="04b88-125">Accoda i file in una sezione dei file di eliminazione INF.</span><span class="sxs-lookup"><span data-stu-id="04b88-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="04b88-126">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="04b88-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="04b88-127">Accoda una ridenominazione del file.</span><span class="sxs-lookup"><span data-stu-id="04b88-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="04b88-128">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="04b88-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="04b88-129">Accoda i file in una sezione dei file di ridenominazione INF.</span><span class="sxs-lookup"><span data-stu-id="04b88-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="04b88-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="04b88-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="04b88-131">Esegue l'analisi della coda di file.</span><span class="sxs-lookup"><span data-stu-id="04b88-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="04b88-132">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="04b88-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="04b88-133">Imposta l'override del percorso della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="04b88-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



