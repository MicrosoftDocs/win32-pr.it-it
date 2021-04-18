---
description: Implementare il multitasking, pianificare le priorità e usare processi, thread, pool di thread, oggetti processo e Fiber. Utilizzare la pianificazione in modalità utente per pianificare i thread.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311966"
---
# <a name="processes-and-threads"></a><span data-ttu-id="ed181-104">Processi e thread</span><span class="sxs-lookup"><span data-stu-id="ed181-104">Processes and Threads</span></span>

<span data-ttu-id="ed181-105">Un'applicazione è costituita da uno o più processi.</span><span class="sxs-lookup"><span data-stu-id="ed181-105">An application consists of one or more processes.</span></span> <span data-ttu-id="ed181-106">Un *processo*, in termini più semplici, è un programma in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed181-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="ed181-107">Uno o più thread vengono eseguiti nel contesto del processo.</span><span class="sxs-lookup"><span data-stu-id="ed181-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="ed181-108">Un *thread* è l'unità di base in cui il sistema operativo alloca il tempo del processore.</span><span class="sxs-lookup"><span data-stu-id="ed181-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="ed181-109">Un thread può eseguire qualsiasi parte del codice del processo, incluse le parti attualmente eseguite da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="ed181-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="ed181-110">Un *oggetto processo* consente la gestione di gruppi di processi come unità.</span><span class="sxs-lookup"><span data-stu-id="ed181-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="ed181-111">Gli oggetti processo sono oggetti namable, a protezione diretta e condivisibili che controllano gli attributi dei processi ad essi associati.</span><span class="sxs-lookup"><span data-stu-id="ed181-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="ed181-112">Le operazioni eseguite sull'oggetto processo hanno effetto su tutti i processi associati all'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="ed181-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="ed181-113">Un *pool di thread* è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed181-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="ed181-114">Il pool di thread viene utilizzato principalmente per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ed181-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="ed181-115">Un *Fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed181-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="ed181-116">I fiber vengono eseguiti nel contesto dei thread che li pianificano.</span><span class="sxs-lookup"><span data-stu-id="ed181-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="ed181-117">La *pianificazione in modalità utente* è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread.</span><span class="sxs-lookup"><span data-stu-id="ed181-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="ed181-118">I thread UMS differiscono dalle [fibre](fibers.md) in quanto ogni thread UMS dispone di un proprio contesto di thread invece di condividere il contesto del thread di un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="ed181-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="ed181-119">Novità di processi e thread</span><span class="sxs-lookup"><span data-stu-id="ed181-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="ed181-120">Informazioni su processi e thread</span><span class="sxs-lookup"><span data-stu-id="ed181-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="ed181-121">Uso di processi e thread</span><span class="sxs-lookup"><span data-stu-id="ed181-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="ed181-122">Riferimento a processi e thread</span><span class="sxs-lookup"><span data-stu-id="ed181-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



