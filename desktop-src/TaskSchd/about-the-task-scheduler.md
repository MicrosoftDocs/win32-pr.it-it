---
title: Informazioni sul Utilità di pianificazione
description: Il servizio Utilità di pianificazione consente di eseguire attività automatiche in un computer scelto.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Utilità di pianificazione Utilità di pianificazione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298480"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="5a9ab-104">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5a9ab-104">About the Task Scheduler</span></span>

<span data-ttu-id="5a9ab-105">Il servizio Utilità di pianificazione consente di eseguire attività automatiche in un computer scelto.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="5a9ab-106">Con questo servizio, è possibile pianificare l'esecuzione di qualsiasi programma in un momento appropriato o quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="5a9ab-107">Il Utilità di pianificazione monitora il tempo o i criteri di evento scelti, quindi esegue l'attività quando tali criteri vengono soddisfatti.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="5a9ab-108">Dove è installato Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5a9ab-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="5a9ab-109">Il Utilità di pianificazione viene installato automaticamente con diversi sistemi operativi Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="5a9ab-110">Utilità di pianificazione 1,0 viene installato con i sistemi operativi Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="5a9ab-111">Utilità di pianificazione 2,0 viene installato con Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="5a9ab-112">Per lo sviluppo di applicazioni che utilizzano il servizio Utilità di pianificazione in Windows Vista, è necessario utilizzare l'API Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="5a9ab-113">Per ulteriori informazioni, vedere [utilità di pianificazione Reference](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5a9ab-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="5a9ab-114">Utilità di pianificazione viene avviato ogni volta che viene avviato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="5a9ab-115">Può essere eseguito tramite l'interfaccia utente grafica (GUI) Utilità di pianificazione o tramite l'API Utilità di pianificazione descritta in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="5a9ab-116">Informazioni sulle attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-116">Information about Tasks</span></span>

<span data-ttu-id="5a9ab-117">Le attività sono il componente principale del Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5a9ab-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="5a9ab-118">Per informazioni sulle attività e sui relativi componenti, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a9ab-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="5a9ab-119">Attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="5a9ab-120">Azioni attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="5a9ab-121">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="5a9ab-122">Informazioni di registrazione delle attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="5a9ab-123">Condizioni di inattività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="5a9ab-124">Contesti di sicurezza per le attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="5a9ab-125">Ripetizione di un'attività</span><span class="sxs-lookup"><span data-stu-id="5a9ab-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="5a9ab-126">Manutenzione automatica</span><span class="sxs-lookup"><span data-stu-id="5a9ab-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="5a9ab-127">Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="5a9ab-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a9ab-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a9ab-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9ab-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5a9ab-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




