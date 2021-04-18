---
title: Novità di Utilità di pianificazione
description: Elenco di nuove funzionalità introdotte da diverse versioni di Utilità di pianificazione.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Utilità di pianificazione Utilità di pianificazione, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305343"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="d9fe6-104">Novità di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d9fe6-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="d9fe6-105">Le modifiche seguenti riepilogano le novità di versioni diverse di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="d9fe6-106">Windows 10 (e Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="d9fe6-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="d9fe6-107">Le modifiche Utilità di pianificazione seguenti sono state introdotte in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="d9fe6-108">Quando lo screen saver batteria è acceso, le attività di Windows Utilità di pianificazione vengono attivate solo se l'attività è:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="d9fe6-109">Non impostato per **avviare l'attività solo se il computer è inattivo... (l'** attività non usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="d9fe6-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="d9fe6-110">Non impostato per l'esecuzione durante la manutenzione automatica (l'attività non usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="d9fe6-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="d9fe6-111">È impostato per l' **esecuzione solo quando l'utente è connesso** (l'attività [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) è un **\_ \_ \_ token interattivo di accesso attività** o un **\_ \_ gruppo di accesso attività**)</span><span class="sxs-lookup"><span data-stu-id="d9fe6-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="d9fe6-112">Tutti gli altri trigger vengono posticipati fino a quando il risparmio di batteria non è disattivato.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="d9fe6-113">Per ulteriori informazioni sull'accesso allo stato di batteria saver nell'applicazione, vedere [**\_ \_ stato di alimentazione del sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span><span class="sxs-lookup"><span data-stu-id="d9fe6-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="d9fe6-114">Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="d9fe6-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="d9fe6-115">Per motivi di sicurezza, un utente non amministratore non può visualizzare né gestire un'attività Utilità di pianificazione di Windows creata da un altro utente.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="d9fe6-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d9fe6-116">Windows 8</span></span>

<span data-ttu-id="d9fe6-117">In Windows 8 sono state introdotte le seguenti Utilità di pianificazione 2,0 modifiche:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="d9fe6-118">Supporto di PowerShell: gli utenti possono gestire (creare, eliminare, modificare, avviare, arrestare e così via in modo esplicito) Windows Utilità di pianificazione le attività usando il modulo ScheduledTasks di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="d9fe6-119">Password gestite: gli amministratori possono usare gli account Active Directory password gestite come entità attività.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="d9fe6-120">Queste attività non richiedono più un criterio di reimpostazione della password applicato.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="d9fe6-121">API changes (modifiche API): introduce due nuove impostazioni attività con l'interfaccia [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .</span><span class="sxs-lookup"><span data-stu-id="d9fe6-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="d9fe6-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): le attività che usano queste impostazioni vengono considerate come un nuovo tipo di attività pianificate che vengono richiamate durante il periodo di manutenzione automatico del sistema operativo, in base alla periodicità e alla scadenza specificate.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="d9fe6-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): le attività impostate per essere volatili sono sempre disabilitate in un avvio del sistema operativo e devono essere riabilitate in modo esplicito quando necessario.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="d9fe6-124">Le attività volatili sono utilizzate dai cluster di failover per garantire che sia pianificata una sola istanza di attività in un cluster alla volta.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="d9fe6-125">Il motore di pianificazione unificato supporta ora le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="d9fe6-126">Tipo di accesso S4U, tramite l'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d9fe6-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="d9fe6-127">Valori di query XPath per i trigger di evento, tramite l'elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d9fe6-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="d9fe6-128">Non consentire la terminazione dell'attività, tramite l'elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d9fe6-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="d9fe6-129">Funzionalità deprecate in questa versione</span><span class="sxs-lookup"><span data-stu-id="d9fe6-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="d9fe6-130">Azione: [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (è possibile usare [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) con il cmdlet [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) di [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)come soluzione alternativa).</span><span class="sxs-lookup"><span data-stu-id="d9fe6-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="d9fe6-131">Azione: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="d9fe6-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="d9fe6-132">AT.exe utilità cmdline</span><span class="sxs-lookup"><span data-stu-id="d9fe6-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="d9fe6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9fe6-133">Windows 7</span></span>

<span data-ttu-id="d9fe6-134">In Windows 7 sono state introdotte le modifiche seguenti Utilità di pianificazione 2,0:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="d9fe6-135">Utilizzando il motore di pianificazione unificato fornito dal sistema operativo sottostante.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="d9fe6-136">Possibilità di rifiutare l'avvio delle attività nelle sessioni remote (RAIL) delle applicazioni remote.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="d9fe6-137">Protezione avanzata delle attività (solo per le attività in esecuzione come "servizio di rete" o "servizio locale"):</span><span class="sxs-lookup"><span data-stu-id="d9fe6-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="d9fe6-138">Possibilità di assegnare un tipo di ID di sicurezza (SID) del token di processo (ad esempio, Unrestricted o None) a un'attività.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="d9fe6-139">Consentire agli sviluppatori di attività di richiedere il set esatto di privilegi richiesti dall'attività.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="d9fe6-140">Modifiche API:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-140">API changes:</span></span>

    -   <span data-ttu-id="d9fe6-141">Supporto per la protezione avanzata delle attività: la nuova funzionalità di protezione avanzata delle attività è stata introdotta con la nuova interfaccia IPrincipal2.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="d9fe6-142">In sono state introdotte due nuove impostazioni attività con la nuova interfaccia ITaskSettings2.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="d9fe6-143">DisallowStartOnRemoteAppSession: la nuova impostazione DisallowStartOnRemoteAppSession può rifiutare l'avvio di un'attività se attivata nelle sessioni [remote (Rail) integrate delle applicazioni](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .</span><span class="sxs-lookup"><span data-stu-id="d9fe6-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="d9fe6-144">UseUnifiedSchedulingEngine: l'uso dell'impostazione UseUnifiedSchedulingEngine fornisce un comportamento coeso per le attività e i servizi di Windows perché viene gestito in modo uniforme da un motore di pianificazione comune a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="d9fe6-145">Sebbene sia consigliabile utilizzare un motore unificato, non supporta alcune delle funzionalità Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="d9fe6-146">Se la combinazione di proprietà non consentirà l'esecuzione dell'attività in un motore unificato, la registrazione di tale oggetto verrà rifiutata.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="d9fe6-147">Le funzionalità delle attività che non sono supportate dal motore di pianificazione unificato includono:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="d9fe6-148">Tipi di accesso:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-148">Logon types:</span></span>

                -   [<span data-ttu-id="d9fe6-149">\_ \_ \_ \_ password o token interattivo di accesso all'attività \_</span><span class="sxs-lookup"><span data-stu-id="d9fe6-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="d9fe6-150">Criteri per più istanze:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="d9fe6-151">**\_ \_ arresto esistente delle istanze dell'attività \_**</span><span class="sxs-lookup"><span data-stu-id="d9fe6-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="d9fe6-152">Azioni:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-152">Actions:</span></span>

                -   [<span data-ttu-id="d9fe6-153">Inviare e-mail</span><span class="sxs-lookup"><span data-stu-id="d9fe6-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="d9fe6-154">Visualizzare il messaggio</span><span class="sxs-lookup"><span data-stu-id="d9fe6-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="d9fe6-155">Impostazioni:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-155">Settings:</span></span>

                -   [<span data-ttu-id="d9fe6-156">Impostazioni di rete delle attività</span><span class="sxs-lookup"><span data-stu-id="d9fe6-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="d9fe6-157">Non consentire la terminazione dell'attività</span><span class="sxs-lookup"><span data-stu-id="d9fe6-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="d9fe6-158">Trigger:</span><span class="sxs-lookup"><span data-stu-id="d9fe6-158">Triggers:</span></span>

                -   [<span data-ttu-id="d9fe6-159">Limite tempo di esecuzione del trigger</span><span class="sxs-lookup"><span data-stu-id="d9fe6-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="d9fe6-160">Modelli di ripetizione per i trigger di calendario</span><span class="sxs-lookup"><span data-stu-id="d9fe6-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="d9fe6-161">Valori di query XPath per i trigger di evento</span><span class="sxs-lookup"><span data-stu-id="d9fe6-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="d9fe6-162">Tipi [di trigger giornalieri](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) e mensili [mensili](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md)</span><span class="sxs-lookup"><span data-stu-id="d9fe6-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="d9fe6-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9fe6-163">Windows Vista</span></span>

<span data-ttu-id="d9fe6-164">Per lo sviluppo di applicazioni che utilizzano il servizio Utilità di pianificazione in Windows Vista, è necessario utilizzare l'API Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="d9fe6-165">Per ulteriori informazioni, vedere [utilità di pianificazione riferimento](task-scheduler-reference.md) e [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="d9fe6-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="d9fe6-166">Windows 2000, Windows XP e Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9fe6-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="d9fe6-167">L'API Utilità di pianificazione 2,0 non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="d9fe6-168">Usare Utilità di pianificazione 1,0.</span><span class="sxs-lookup"><span data-stu-id="d9fe6-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9fe6-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9fe6-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9fe6-170">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d9fe6-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d9fe6-171">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d9fe6-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
