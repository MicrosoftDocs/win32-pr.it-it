---
title: Attività
description: Un'attività è il lavoro pianificato eseguito dal servizio Utilità di pianificazione.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Utilità di pianificazione attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298747"
---
# <a name="tasks"></a>Attività

Un'attività è il lavoro pianificato eseguito dal servizio Utilità di pianificazione. Un'attività è costituita da componenti diversi, ma un'attività deve contenere un trigger utilizzato dal Utilità di pianificazione per avviare l'attività e un'azione che descrive il lavoro che verrà eseguito dall'Utilità di pianificazione.

Quando si crea un'attività, questa viene archiviata in una cartella attività. È possibile accedere alle cartelle delle attività tramite l'interfaccia [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) per lo scripting) e accedere alle attività tramite l'interfaccia [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) per lo scripting) al momento della creazione. È possibile modificare gli elenchi di controllo di accesso (ACL) per le attività e le cartelle attività per concedere o negare a determinati utenti e gruppi l'accesso a una cartella attività o attività. Questa operazione può essere eseguita usando il metodo [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , il metodo [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) oppure specificando un descrittore di sicurezza quando un'attività viene registrata usando il metodo [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un file attività o a una cartella attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

## <a name="components-of-a-task"></a>Componenti di un'attività

Nella figura seguente sono illustrati i componenti dell'attività.

![componenti attività](images/taskcomponents.png)

L'elenco seguente contiene una breve descrizione di ogni componente attività:

-   Trigger: Utilità di pianificazione usa trigger basati su eventi o temporali per capire quando avviare un'attività. Ogni attività può specificare uno o più trigger per avviare l'attività.

    Per ulteriori informazioni sui trigger, vedere [trigger di attività](task-triggers.md).

-   Azioni: queste sono le azioni, il lavoro effettivo che viene eseguito dall'attività. Ogni attività può specificare una o più azioni per completare il lavoro.

    Per altre informazioni sulle azioni, vedere [azioni attività](task-actions.md).

-   Entità: le entità definiscono il contesto di sicurezza in cui viene eseguita l'attività. Ad esempio, un'entità potrebbe definire un utente o un gruppo di utenti specifico che può eseguire l'attività.

    Per ulteriori informazioni sulle entità, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).

-   Impostazioni: si tratta delle impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività in relazione alle condizioni esterne all'attività stessa. Queste impostazioni possono ad esempio specificare la priorità dell'attività in relazione ad altre attività, se è possibile eseguire più istanze dell'attività, il modo in cui l'attività viene gestita quando il computer si trova in una condizione di inattività e altre condizioni.

    Per ulteriori informazioni sulle impostazioni delle attività, vedere [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) per lo scripting).

    > [!Note]  
    > Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione. È possibile modificare questa impostazione modificando l'impostazione [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .

     

-   Informazioni di registrazione: informazioni amministrative raccolte quando l'attività viene registrata. Ad esempio, queste informazioni descrivono l'autore dell'attività, la data in cui l'attività è stata registrata, una descrizione XML dell'attività e altre informazioni.

    Per ulteriori informazioni sulle informazioni di registrazione delle attività, vedere [informazioni sulla registrazione delle attività](task-registration-information.md).

-   Data: documentazione aggiuntiva sull'attività fornita dall'autore dell'attività. Ad esempio, questi dati possono contenere la guida XML che può essere utilizzata dagli utenti quando eseguono l'attività.

## <a name="task-apis"></a>API attività

Utilità di pianificazione 2,0 offre due set di API: un set di oggetti di script e interfacce per Utilità di pianificazione 2,0. Per ulteriori informazioni, vedere [utilità di pianificazione Reference](task-scheduler-reference.md).

Per la compatibilità delle attività, impostata tramite la proprietà [**compatibilità**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , è consigliabile impostare solo la \_ compatibilità delle attività \_ V1 se è necessario accedere o modificare un'attività da un computer Windows XP, Windows Server 2003 o Windows 2000. In caso contrario, è consigliabile usare Utilità di pianificazione compatibilità 2,0, perché include più funzionalità.

A partire da Utilità di pianificazione 2,0, l'interfaccia [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) per lo scripting) viene usata come punto di partenza per la creazione di attività in cartelle specifiche. L'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) per lo scripting) viene usata per conservare tutti i componenti di un'attività, ad esempio le impostazioni, le azioni e i trigger. Le API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) forniscono proprietà che vengono quindi utilizzate per definire gli altri componenti dell'attività. Utilità di pianificazione 1,0 fornisce l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , supportata solo per la compatibilità con le versioni precedenti.

Per gli script, le interfacce di Utilità di pianificazione vengono mappate a oggetti di script con nomi, proprietà e metodi simili. Ad esempio, l'oggetto di scripting [**TaskService**](taskservice.md) ha le stesse proprietà e i metodi dell'interfaccia [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Attività Utilità di pianificazione 1,0

Un'attività Utilità di pianificazione 1,0 è qualsiasi tipo di applicazione o di file che può essere eseguito dall'Utilità di pianificazione. Questi possono includere uno dei seguenti (come supportato dal sistema operativo in cui verrà eseguita l'attività): applicazioni Win32, applicazioni Win16, applicazioni OS/2, applicazioni MS-DOS, file batch ( \* . bat), file di comando ( \* cmd) o qualsiasi tipo di file registrato correttamente.

I dati che descrivono un'attività vengono conservati in un file di attività archiviato nella cartella delle attività pianificate. Per ulteriori informazioni, vedere [*cartella attività pianificate*](s.md). Il nome di questi file delle attività include il nome dell'attività, seguito da un'estensione del nome di file. job.

Per ulteriori informazioni sull'aggiunta di Utilità di pianificazione attività 1,0, vedere [aggiunta di elementi di lavoro](adding-work-items.md).

Per ulteriori informazioni sull'enumerazione tramite Utilità di pianificazione attività 1,0, vedere [enumerazione delle attività](enumerating-tasks.md).

Per un computer Windows Server 2003, Windows XP o Windows 2000 per creare, monitorare o controllare le attività in un computer con Windows Vista, è necessario completare le operazioni seguenti nel computer con Windows Vista e l'utente che chiama il metodo [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve essere un membro del gruppo Administrators nel computer Windows Vista remoto.

**Per abilitare l'eccezione "condivisione di file e stampanti" in Windows Firewall**

1.  Fare clic sul pulsante **Start** e quindi scegliere **Pannello di controllo**.
2.  Nel **Pannello di controllo** fare clic su **visualizzazione classica** , quindi fare doppio clic sull'icona **Windows Firewall** .
3.  Nella finestra **Windows Firewall** fare clic sulla scheda **eccezioni** , quindi selezionare la casella di controllo eccezioni **condivisione file e stampanti** .

**Per abilitare il servizio "Registro di sistema remoto"**

-   Aprire una finestra del prompt dei comandi e immettere il comando seguente: **net start "Remote Registry"**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Trigger attività](task-triggers.md)
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

 

 




