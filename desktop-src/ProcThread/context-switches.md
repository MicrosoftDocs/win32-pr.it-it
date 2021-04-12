---
description: L'utilità di pianificazione mantiene una coda di thread eseguibili per ogni livello di priorità.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambi di contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231523"
---
# <a name="context-switches"></a><span data-ttu-id="ed809-103">Cambi di contesto</span><span class="sxs-lookup"><span data-stu-id="ed809-103">Context Switches</span></span>

<span data-ttu-id="ed809-104">L'utilità di pianificazione mantiene una coda di thread eseguibili per ogni livello di priorità.</span><span class="sxs-lookup"><span data-stu-id="ed809-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="ed809-105">Questi sono noti come *thread pronti*.</span><span class="sxs-lookup"><span data-stu-id="ed809-105">These are known as *ready threads*.</span></span> <span data-ttu-id="ed809-106">Quando un processore diventa disponibile, il sistema esegue un *cambio di contesto*.</span><span class="sxs-lookup"><span data-stu-id="ed809-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="ed809-107">I passaggi in un cambio di contesto sono:</span><span class="sxs-lookup"><span data-stu-id="ed809-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="ed809-108">Salva il contesto del thread che ha appena terminato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed809-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="ed809-109">Posizionare il thread che ha appena terminato l'esecuzione alla fine della coda per la relativa priorità.</span><span class="sxs-lookup"><span data-stu-id="ed809-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="ed809-110">Trovare la coda con priorità più alta che contiene thread pronti.</span><span class="sxs-lookup"><span data-stu-id="ed809-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="ed809-111">Rimuovere il thread all'inizio della coda, caricarne il contesto ed eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="ed809-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="ed809-112">Le classi di thread seguenti non sono thread pronti.</span><span class="sxs-lookup"><span data-stu-id="ed809-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="ed809-113">Thread creati con il flag di creazione \_ sospesa</span><span class="sxs-lookup"><span data-stu-id="ed809-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="ed809-114">Thread interrotti durante l'esecuzione con la funzione [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)</span><span class="sxs-lookup"><span data-stu-id="ed809-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="ed809-115">Thread in attesa di un oggetto o di un input di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed809-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="ed809-116">Finché i thread sospesi o bloccati diventano pronti per l'esecuzione, l'utilità di pianificazione non alloca alcun tempo del processore, indipendentemente dalla loro priorità.</span><span class="sxs-lookup"><span data-stu-id="ed809-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="ed809-117">I motivi più comuni per un cambio di contesto sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed809-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="ed809-118">Intervallo di tempo trascorso.</span><span class="sxs-lookup"><span data-stu-id="ed809-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="ed809-119">Un thread con una priorità più alta è diventato pronto per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed809-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="ed809-120">È necessario attendere un thread in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed809-120">A running thread needs to wait.</span></span>

<span data-ttu-id="ed809-121">Quando un thread in esecuzione deve attendere, cede il resto della sezione di tempo.</span><span class="sxs-lookup"><span data-stu-id="ed809-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
