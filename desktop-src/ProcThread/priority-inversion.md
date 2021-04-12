---
description: L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da pianificare.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversione priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345456"
---
# <a name="priority-inversion"></a><span data-ttu-id="ff93f-103">Inversione priorità</span><span class="sxs-lookup"><span data-stu-id="ff93f-103">Priority Inversion</span></span>

<span data-ttu-id="ff93f-104">L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da pianificare.</span><span class="sxs-lookup"><span data-stu-id="ff93f-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="ff93f-105">Si consideri un caso semplice con tre thread: thread 1, thread 2 e thread 3.</span><span class="sxs-lookup"><span data-stu-id="ff93f-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="ff93f-106">Il thread 1 è con priorità alta e diventa pronto per essere pianificato.</span><span class="sxs-lookup"><span data-stu-id="ff93f-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="ff93f-107">Il thread 2, un thread con priorità bassa, sta eseguendo il codice in una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="ff93f-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="ff93f-108">Thread 1, il thread con priorità alta, inizia ad attendere una risorsa condivisa dal thread 2.</span><span class="sxs-lookup"><span data-stu-id="ff93f-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="ff93f-109">Il thread 3 ha priorità media.</span><span class="sxs-lookup"><span data-stu-id="ff93f-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="ff93f-110">Il thread 3 riceve tutto il tempo del processore, perché il thread con priorità alta (thread 1) è in attesa di risorse condivise dal thread con priorità bassa (thread 2).</span><span class="sxs-lookup"><span data-stu-id="ff93f-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="ff93f-111">Il thread 2 non lascerà la sezione critica, perché non ha la priorità più alta e non verrà pianificata.</span><span class="sxs-lookup"><span data-stu-id="ff93f-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="ff93f-112">L'utilità di pianificazione risolve questo problema, incrementando in modo casuale la priorità dei thread pronti, in questo caso i blocchi con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="ff93f-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="ff93f-113">I thread con priorità bassa vengono eseguiti abbastanza a lungo per uscire dalla sezione critica e il thread con priorità alta può accedere alla sezione critica.</span><span class="sxs-lookup"><span data-stu-id="ff93f-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="ff93f-114">Se il thread con priorità bassa non ha tempo sufficiente per uscire dalla sezione critica per la prima volta, si otterrà un'altra opportunità durante il ciclo di pianificazione successivo.</span><span class="sxs-lookup"><span data-stu-id="ff93f-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



