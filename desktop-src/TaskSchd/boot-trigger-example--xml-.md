---
title: Esempio di trigger di avvio (XML)
description: Il codice XML in questo esempio definisce un'attività che Blocco note all'avvio del sistema.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75b4c9628da5ef56ec006faf9d7301661dfd0f76894ebb4f5f37cc1035d40f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860320"
---
# <a name="boot-trigger-example-xml"></a>Esempio di trigger di avvio (XML)

Il codice XML in questo esempio definisce un'attività che Blocco note all'avvio del sistema.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) per lo scripting) o lo strumento Schtasks.exe da riga di comando. Se si usa lo strumento Schtasks.exe (disponibile nella directory C: Windows System32), è possibile usare il comando seguente per registrare l'attività: \\ \\ **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Per definire un'attività da avviare Blocco note all'avvio del sistema

L'esempio XML seguente illustra come definire un'attività con una singola azione di esecuzione (a partire da Blocco note), un trigger di avvio singolo che avvia l'attività all'avvio del sistema e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte del Utilità di pianificazione.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Elementi dello schema TaskScheduler

Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si usa questo esempio.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene informazioni di registrazione sull'attività.
-   [**Trigger:**](taskschedulerschema-triggers-tasktype-element.md)definisce il trigger che avvia l'attività.
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): definisce il trigger di avvio. In questo caso vengono usati solo due elementi figlio: i limiti iniziale e finale che specificano quando il trigger viene attivato e disattivato.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.
-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività che l'Utilità di pianificazione usa per eseguire l'attività.
-   [**Azioni**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività. In questo caso, eseguire Blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




