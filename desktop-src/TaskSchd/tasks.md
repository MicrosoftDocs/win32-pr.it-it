---
title: Attività
description: Un'attività è il lavoro pianificato eseguito dal Utilità di pianificazione servizio.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f6122bcf32e0c3e242b6dce119432a9014718d4b65d19c613ce27794355491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517107"
---
# <a name="tasks"></a>Attività

Un'attività è il lavoro pianificato eseguito dal Utilità di pianificazione servizio. Un'attività è costituita da componenti diversi, ma un'attività deve contenere un trigger che il Utilità di pianificazione usa per avviare l'attività e un'azione che descrive il lavoro che l'Utilità di pianificazione eseguirà.

Quando viene creata, un'attività viene archiviata in una cartella di attività. È possibile accedere alle cartelle attività tramite l'interfaccia [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) per lo scripting) e le attività sono accessibili tramite l'interfaccia [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) [**(RegisteredTask**](registeredtask.md) per lo scripting) quando vengono create. È possibile modificare gli elenchi di controllo di accesso (ACL) per le attività e le cartelle delle attività per concedere o negare a determinati utenti e gruppi l'accesso a una cartella di attività o attività. Questa operazione può essere eseguita usando il metodo [**IRegisteredTask::SetSecurityDescriptor,**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) il metodo [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) o specificando un descrittore di sicurezza quando un'attività viene registrata tramite il [**metodo RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**RegisterTask.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un file di attività o a una cartella di attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

## <a name="components-of-a-task"></a>Componenti di un'attività

La figura seguente mostra i componenti dell'attività.

![componenti delle attività](images/taskcomponents.png)

L'elenco seguente contiene una breve descrizione di ogni componente dell'attività:

-   Trigger: Utilità di pianificazione trigger basati su eventi o tempo per sapere quando avviare un'attività. Ogni attività può specificare uno o più trigger per avviare l'attività.

    Per altre informazioni sui trigger, vedere [Trigger di attività](task-triggers.md).

-   Azioni: queste sono le azioni, il lavoro effettivo, che viene eseguito dall'attività. Ogni attività può specificare una o più azioni per completare il proprio lavoro.

    Per altre informazioni sulle azioni, vedere [Azioni attività](task-actions.md).

-   Entità: le entità definiscono il contesto di sicurezza in cui viene eseguita l'attività. Ad esempio, un'entità può definire un utente o un gruppo di utenti specifico che può eseguire l'attività.

    Per altre informazioni sulle entità, vedere [Contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).

-   Impostazioni: queste sono le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività rispetto alle condizioni esterne all'attività stessa. Ad esempio, queste impostazioni possono specificare la priorità dell'attività rispetto ad altre attività, se è possibile eseguire più istanze dell'attività, come viene gestita l'attività quando il computer si trova in una condizione di inattività e altre condizioni.

    Per altre informazioni sulle impostazioni delle attività, vedere [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).

    > [!Note]  
    > Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione. È possibile modificare questa impostazione modificando [**l'impostazione ExecutionTimeLimit.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit)

     

-   Informazioni di registrazione: informazioni amministrative raccolte al momento della registrazione dell'attività. Ad esempio, queste informazioni descrivono l'autore dell'attività, la data di registrazione dell'attività, una descrizione XML dell'attività e altre informazioni.

    Per altre informazioni sulle informazioni di registrazione delle attività, vedere [Informazioni di registrazione attività](task-registration-information.md).

-   Dati: documentazione aggiuntiva sull'attività fornita dall'autore dell'attività. Ad esempio, questi dati possono contenere la Guida XML che può essere usata dagli utenti quando eseguono l'attività.

## <a name="task-apis"></a>API di attività

Utilità di pianificazione 2.0 offre due set di API: un set di oggetti di scripting e interfacce per Utilità di pianificazione 2.0. Per altre informazioni, vedere Utilità di pianificazione [Reference](task-scheduler-reference.md).

La compatibilità delle attività, impostata tramite la proprietà [**Compatibility,**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) deve essere impostata su TASK COMPATIBILITY V1 solo se è necessario accedere o modificare un'attività da un \_ computer Windows \_ XP, Windows Server 2003 o Windows 2000. In caso contrario, è consigliabile usare Utilità di pianificazione 2.0 perché include più funzionalità.

A partire da Utilità di pianificazione 2.0, [**l'interfaccia ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) per lo scripting) viene usata come punto di partenza per creare attività in cartelle specificate. [**L'interfaccia ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) per lo scripting) viene usata per contenere tutti i componenti di un'attività, ad esempio le impostazioni, le azioni e i trigger. Le [**API ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) forniscono proprietà che vengono quindi usate per definire gli altri componenti dell'attività. Utilità di pianificazione 1.0 fornisce [**l'interfaccia ITask,**](/windows/desktop/api/Mstask/nn-mstask-itask) supportata solo per la compatibilità con le versioni precedenti.

Per lo scripting, le Utilità di pianificazione di esecuzione vengono mappate a oggetti di scripting con nomi, proprietà e metodi simili. Ad esempio, [**l'oggetto**](taskservice.md) di scripting TaskService ha le stesse proprietà e gli stessi metodi dell'interfaccia [**ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

Per altre informazioni ed esempi su come usare le interfacce Utilità di pianificazione, gli oggetti di scripting e XML, vedere [Using the Utilità di pianificazione](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Utilità di pianificazione 1.0 Tasks

Un'Utilità di pianificazione 1.0 è qualsiasi applicazione o tipo di file che Utilità di pianificazione possibile eseguire. Possono essere inclusi gli elementi seguenti (supportati dal sistema operativo in cui verrà eseguita l'attività): applicazioni Win32, applicazioni Win16, applicazioni del sistema operativo/2, applicazioni MS-DOS, file batch (.bat), file di comando (cmd) o qualsiasi tipo di file registrato \* \* correttamente.

I dati che descrivono un'attività vengono mantenuti in un file di attività archiviato nella cartella Attività pianificate. Per altre informazioni, vedere [*Cartella Attività pianificate*](s.md). Il nome di questi file di attività include il nome dell'attività, seguito da un'estensione di file con estensione job.

Per altre informazioni sull'aggiunta di Utilità di pianificazione 1.0, vedere [Aggiunta di elementi di lavoro](adding-work-items.md).

Per altre informazioni sull'enumerazione tramite Utilità di pianificazione 1.0, vedere [Enumerazione delle attività](enumerating-tasks.md).

Per creare, monitorare o controllare attività in un computer Windows Server 2003, Windows XP o Windows 2000 per creare, monitorare o controllare le attività in un computer Windows Vista, le operazioni seguenti devono essere completate nel computer Windows Vista e l'utente che chiama il metodo [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve essere membro del gruppo Administrators nel computer remoto Windows Vista.

**Per abilitare l'eccezione "Condividi file e stampanti" in Windows Firewall**

1.  Fare clic sul pulsante **Start** e quindi scegliere **Pannello di controllo**.
2.  In **Pannello di controllo** fare clic **su Visualizzazione classica** e quindi fare doppio clic sull'icona Windows **Firewall.**
3.  Nella finestra **Windows firewall** fare clic sulla scheda **Eccezioni** e selezionare la casella di controllo **Eccezione** condivisione file e stampanti .

**Per abilitare il servizio "Registro di sistema remoto"**

-   Aprire una finestra del prompt dei comandi e immettere il comando seguente: **net start "Registro di sistema remoto".**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Trigger di attività](task-triggers.md)
</dt> <dt>

[Azioni attività](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




