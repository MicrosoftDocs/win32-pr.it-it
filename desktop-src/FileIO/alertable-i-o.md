---
description: L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: I/O Alertable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308913"
---
# <a name="alertable-io"></a><span data-ttu-id="374ec-103">I/O Alertable</span><span class="sxs-lookup"><span data-stu-id="374ec-103">Alertable I/O</span></span>

<span data-ttu-id="374ec-104">L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="374ec-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="374ec-105">Per comprendere quando un thread è in uno stato di avviso, si consideri lo scenario seguente:</span><span class="sxs-lookup"><span data-stu-id="374ec-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="374ec-106">Un thread avvia una richiesta di lettura asincrona chiamando [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) con un puntatore a una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="374ec-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="374ec-107">Il thread avvia una richiesta di scrittura asincrona chiamando [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) con un puntatore a una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="374ec-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="374ec-108">Il thread chiama una funzione che recupera una riga di dati da un server di database remoto.</span><span class="sxs-lookup"><span data-stu-id="374ec-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="374ec-109">In questo scenario, le chiamate a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) torneranno probabilmente prima della chiamata di funzione nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="374ec-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="374ec-110">In tal caso, il kernel inserisce i puntatori alle funzioni di callback nella coda di chiamata di procedura asincrona (APC) del thread.</span><span class="sxs-lookup"><span data-stu-id="374ec-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="374ec-111">Il kernel mantiene questa coda in modo specifico per contenere i dati della richiesta I/O restituiti fino a quando non può essere elaborata dal thread corrispondente.</span><span class="sxs-lookup"><span data-stu-id="374ec-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="374ec-112">Quando il recupero delle righe viene completato e il thread viene restituito dalla funzione, la priorità più elevata consiste nell'elaborare le richieste di I/O restituite nella coda chiamando le funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="374ec-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="374ec-113">A tale scopo, deve immettere uno stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="374ec-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="374ec-114">Un thread può eseguire questa operazione solo chiamando una delle funzioni seguenti con i flag appropriati:</span><span class="sxs-lookup"><span data-stu-id="374ec-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="374ec-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="374ec-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="374ec-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="374ec-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="374ec-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="374ec-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="374ec-118">**SignalObjectAndWait**</span><span class="sxs-lookup"><span data-stu-id="374ec-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="374ec-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="374ec-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="374ec-120">Quando il thread entra in uno stato di avviso, si verificano gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="374ec-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="374ec-121">Il kernel controlla la coda APC del thread.</span><span class="sxs-lookup"><span data-stu-id="374ec-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="374ec-122">Se la coda contiene puntatori a funzioni di callback, il kernel rimuove il puntatore dalla coda e lo invia al thread.</span><span class="sxs-lookup"><span data-stu-id="374ec-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="374ec-123">Il thread esegue la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="374ec-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="374ec-124">I passaggi 1 e 2 vengono ripetuti per ogni puntatore rimanente nella coda.</span><span class="sxs-lookup"><span data-stu-id="374ec-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="374ec-125">Quando la coda è vuota, il thread viene restituito dalla funzione che lo ha inserito in uno stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="374ec-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="374ec-126">In questo scenario, quando il thread entra in uno stato di avviso, chiamerà le funzioni di callback inviate a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), quindi restituirà dalla funzione che lo ha inserito in uno stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="374ec-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="374ec-127">Se un thread entra in uno stato di avviso mentre la coda APC è vuota, l'esecuzione del thread verrà sospesa dal kernel fino a quando non si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="374ec-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="374ec-128">L'oggetto kernel in attesa di diventa segnalato.</span><span class="sxs-lookup"><span data-stu-id="374ec-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="374ec-129">Un puntatore alla funzione di callback viene inserito nella coda APC.</span><span class="sxs-lookup"><span data-stu-id="374ec-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="374ec-130">Un thread che usa l'I/O con avvisi elabora le richieste di I/o asincrone in modo più efficiente rispetto a quando attendono semplicemente il flag di evento nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e il meccanismo di i/o di avviso è meno complesso delle [porte di completamento i/o](i-o-completion-ports.md) da usare.</span><span class="sxs-lookup"><span data-stu-id="374ec-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="374ec-131">Tuttavia, l'I/O con avvisi restituisce il risultato della richiesta di I/O solo al thread che lo ha avviato.</span><span class="sxs-lookup"><span data-stu-id="374ec-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="374ec-132">Le porte di completamento I/O non presentano questa limitazione.</span><span class="sxs-lookup"><span data-stu-id="374ec-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="374ec-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="374ec-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="374ec-134">Chiamate di procedure asincrone</span><span class="sxs-lookup"><span data-stu-id="374ec-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
