---
title: Utilità di pianificazione per gli sviluppatori
description: Il Utilità di pianificazione consente di eseguire automaticamente le attività di routine in un computer scelto. Utilità di pianificazione esegue questa operazione monitorando qualsiasi criterio scelto (denominato trigger) e quindi eseguendo le attività quando questi criteri vengono soddisfatti.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Utilità di pianificazione per gli sviluppatori
- Utilità di pianificazione per lo sviluppo
- Sviluppo con Utilità di pianificazione
- Utilità di pianificazione, pagina del portale
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2019
ms.locfileid: "104116941"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="30582-108">Utilità di pianificazione per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="30582-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30582-109">Questo argomento e gli altri argomenti di questa sezione sono destinati a un pubblico di sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="30582-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="30582-110">Se si desidera utilizzare il componente Utilità di pianificazione nella propria capacità di amministratore o di un professionista IT, vedere [utilità di pianificazione](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="30582-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="30582-111">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="30582-111">About the Task Scheduler</span></span>

<span data-ttu-id="30582-112">Il Utilità di pianificazione consente di eseguire automaticamente le attività di routine in un computer scelto.</span><span class="sxs-lookup"><span data-stu-id="30582-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="30582-113">Utilità di pianificazione esegue questa operazione monitorando qualsiasi criterio scelto (denominato trigger) e quindi eseguendo le attività quando questi criteri vengono soddisfatti.</span><span class="sxs-lookup"><span data-stu-id="30582-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="30582-114">È possibile utilizzare il Utilità di pianificazione per eseguire attività quali l'avvio di un'applicazione, l'invio di un messaggio di posta elettronica o la visualizzazione di una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="30582-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="30582-115">È possibile pianificare l'esecuzione delle attività in risposta a questi eventi o trigger.</span><span class="sxs-lookup"><span data-stu-id="30582-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="30582-116">Quando si verifica un evento di sistema specifico.</span><span class="sxs-lookup"><span data-stu-id="30582-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="30582-117">In un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="30582-117">At a specific time.</span></span>
- <span data-ttu-id="30582-118">A un'ora specifica in base a una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="30582-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="30582-119">A un orario specifico in base a una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="30582-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="30582-120">A un orario specifico in base a una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="30582-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="30582-121">In un momento specifico, in base a una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="30582-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="30582-122">Quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="30582-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="30582-123">Quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="30582-123">When the task is registered.</span></span>
- <span data-ttu-id="30582-124">Quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="30582-124">When the system is booted.</span></span>
- <span data-ttu-id="30582-125">Quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="30582-125">When a user logs on.</span></span>
- <span data-ttu-id="30582-126">Quando una sessione di Terminal Server cambia stato.</span><span class="sxs-lookup"><span data-stu-id="30582-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="30582-127">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="30582-127">Developers</span></span>

<span data-ttu-id="30582-128">Il Utilità di pianificazione fornisce le API in questi formati.</span><span class="sxs-lookup"><span data-stu-id="30582-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="30582-129">Utilità di pianificazione 2,0: le interfacce e gli oggetti vengono forniti rispettivamente per C++ e per lo sviluppo di script.</span><span class="sxs-lookup"><span data-stu-id="30582-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="30582-130">Utilità di pianificazione 1,0: le interfacce sono fornite per lo sviluppo in C++.</span><span class="sxs-lookup"><span data-stu-id="30582-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="30582-131">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="30582-131">Run-time requirements</span></span>

<span data-ttu-id="30582-132">Il Utilità di pianificazione richiede i sistemi operativi seguenti.</span><span class="sxs-lookup"><span data-stu-id="30582-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="30582-133">Utilità di pianificazione 2,0: il client richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="30582-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="30582-134">Il server richiede Windows Server 2008 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="30582-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="30582-135">Utilità di pianificazione 1,0: il client richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="30582-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="30582-136">Il server richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="30582-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="30582-137">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="30582-137">In this section</span></span>

| <span data-ttu-id="30582-138">Argomento</span><span class="sxs-lookup"><span data-stu-id="30582-138">Topic</span></span> | <span data-ttu-id="30582-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30582-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="30582-140">Novità di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="30582-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="30582-141">Riepilogo delle nuove funzionalità introdotte dal Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30582-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="30582-142">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="30582-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="30582-143">Informazioni concettuali generali sull'API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30582-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="30582-144">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="30582-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="30582-145">Esempi di codice che illustrano come usare le API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30582-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="30582-146">Riferimento Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="30582-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="30582-147">Informazioni di riferimento dettagliate per le API Utilità di pianificazione e lo schema di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="30582-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |