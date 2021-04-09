---
description: In genere, la sincronizzazione non è necessaria quando si ha un Apartment a thread singolo (STA) perché l'Apartment fornisce la sincronizzazione.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Concetti relativi alla sincronizzazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748879"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="4cb88-103">Concetti relativi alla sincronizzazione COM+</span><span class="sxs-lookup"><span data-stu-id="4cb88-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="4cb88-104">In genere, la sincronizzazione non è necessaria quando si ha un Apartment a thread singolo (STA) perché l'Apartment fornisce la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4cb88-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="4cb88-105">La sincronizzazione diventa importante quando si dispone di un Apartment a thread multipli (MTA) e di un oggetto a thread libero.</span><span class="sxs-lookup"><span data-stu-id="4cb88-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="4cb88-106">In passato, gli oggetti a thread libero hanno dovuto gestire il blocco.</span><span class="sxs-lookup"><span data-stu-id="4cb88-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="4cb88-107">È possibile eliminare la necessità di utilizzare il blocco impostando l'attributo di sincronizzazione per un componente.</span><span class="sxs-lookup"><span data-stu-id="4cb88-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="4cb88-108">La sincronizzazione presenta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cb88-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="4cb88-109">Consente a un chiamante di immettere il componente alla volta.</span><span class="sxs-lookup"><span data-stu-id="4cb88-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="4cb88-110">Impedisce il flusso attraverso il processo o tra computer.</span><span class="sxs-lookup"><span data-stu-id="4cb88-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="4cb88-111">Flussi da componente a componente all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="4cb88-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="4cb88-112">Consente la rientranza dallo stesso chiamante.</span><span class="sxs-lookup"><span data-stu-id="4cb88-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="4cb88-113">Diversamente dagli Apartment, le attività estendono i contesti di più processi e host.</span><span class="sxs-lookup"><span data-stu-id="4cb88-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="4cb88-114">La sincronizzazione determina quale attività conterrà un oggetto.</span><span class="sxs-lookup"><span data-stu-id="4cb88-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="4cb88-115">Gli oggetti possono risiedere in una delle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cb88-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="4cb88-116">Attività del creatore</span><span class="sxs-lookup"><span data-stu-id="4cb88-116">Creator's activity</span></span>
-   <span data-ttu-id="4cb88-117">Nuova attività</span><span class="sxs-lookup"><span data-stu-id="4cb88-117">New activity</span></span>
-   <span data-ttu-id="4cb88-118">Nessuna attività</span><span class="sxs-lookup"><span data-stu-id="4cb88-118">No activity</span></span>

<span data-ttu-id="4cb88-119">COM+ garantisce la concorrenza in base a una serie di blocchi per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="4cb88-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="4cb88-120">Se un chiamante tenta di immettere un componente COM+ Synchronized già utilizzato da un altro chiamante, la chiamata viene bloccata fino a quando il blocco non viene rilasciato.</span><span class="sxs-lookup"><span data-stu-id="4cb88-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="4cb88-121">Questo comportamento di blocco non si timeout e non può essere configurato per il timeout. Se il blocco non è in uso, il blocco viene acquisito e la chiamata viene elaborata.</span><span class="sxs-lookup"><span data-stu-id="4cb88-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="4cb88-122">Al termine, il blocco viene rilasciato per il chiamante successivo.</span><span class="sxs-lookup"><span data-stu-id="4cb88-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="4cb88-123">Per evitare deadlock, COM+ gestisce l'accesso a tutti gli oggetti tra le attività da parte di una serie annidata di chiamate concatenate in tutta la rete.</span><span class="sxs-lookup"><span data-stu-id="4cb88-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="4cb88-124">COM+ fornisce le seguenti impostazioni di sincronizzazione:</span><span class="sxs-lookup"><span data-stu-id="4cb88-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="4cb88-125">Disabled</span><span class="sxs-lookup"><span data-stu-id="4cb88-125">Disabled</span></span>
-   <span data-ttu-id="4cb88-126">Non supportato</span><span class="sxs-lookup"><span data-stu-id="4cb88-126">Not Supported</span></span>
-   <span data-ttu-id="4cb88-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="4cb88-127">Supported</span></span>
-   <span data-ttu-id="4cb88-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="4cb88-128">Required</span></span>
-   <span data-ttu-id="4cb88-129">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="4cb88-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="4cb88-130">Alcune impostazioni di sincronizzazione funzionano insieme ad altre impostazioni del componente COM+.</span><span class="sxs-lookup"><span data-stu-id="4cb88-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="4cb88-131">La sincronizzazione è ad esempio necessaria se il servizio [di attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md) è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4cb88-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="4cb88-132">JIT è obbligatorio se si abilitano le transazioni. Pertanto, l' [elaborazione delle transazioni](com--transactions.md) com+ richiede anche la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4cb88-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="4cb88-133">Pertanto, le classi con l'impostazione JIT = true devono avere anche l'impostazione Synchronization = Required o Synchronization = RequiresNew.</span><span class="sxs-lookup"><span data-stu-id="4cb88-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="4cb88-134">Per istruzioni sull'impostazione delle opzioni di sincronizzazione tramite lo strumento di amministrazione Servizi componenti, vedere [impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="4cb88-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="4cb88-135">Per ulteriori informazioni sull'utilizzo della libreria di amministrazione COM+ per impostare le opzioni di sincronizzazione, vedere [automazione di com+ Administration](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="4cb88-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cb88-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4cb88-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cb88-137">Attività di sincronizzazione COM+</span><span class="sxs-lookup"><span data-stu-id="4cb88-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



