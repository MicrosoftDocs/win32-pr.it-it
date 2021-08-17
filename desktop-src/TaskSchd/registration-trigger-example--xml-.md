---
title: Esempio di trigger di registrazione (XML)
description: Il codice XML in questo esempio definisce un'attività che inizia Blocco note quando l'attività viene registrata.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b111f5c8c0801bb404e12cee20faf19208d7372d1a3980f7368c6efd2bcbfd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759582"
---
# <a name="registration-trigger-example-xml"></a>Esempio di trigger di registrazione (XML)

Il codice XML in questo esempio definisce un'attività che inizia Blocco note quando l'attività viene registrata.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) per lo scripting) o lo strumento Schtasks.exe da riga di comando. Se si usa lo strumento Schtasks.exe (disponibile nella directory C: Windows System32), è possibile usare il comando seguente per registrare l'attività: \\ \\ **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

> [!Note]  
> Quando un'attività con un trigger di registrazione viene aggiornata, l'attività verrà eseguita dopo l'aggiornamento.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>Per definire un'attività da avviare Blocco note alla registrazione

L'esempio XML seguente illustra come definire un'attività con una singola azione di esecuzione (a partire da Blocco note), un singolo trigger di registrazione che avvia l'attività quando viene registrata e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita dal Utilità di pianificazione.

> [!Note]  
> Quando un'attività con un trigger di registrazione viene aggiornata, l'attività verrà eseguita dopo l'aggiornamento.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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
-   [**RegistrationTrigger:**](taskschedulerschema-registrationtrigger-triggergroup-element.md)definisce il trigger di registrazione. In questo caso, vengono usati solo due elementi figlio: i limiti iniziale e finale che specificano quando il trigger viene attivato e disattivato.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.
-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività che l'Utilità di pianificazione usa per eseguire l'attività.
-   [**Azioni**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività. In questo caso, eseguire Blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




