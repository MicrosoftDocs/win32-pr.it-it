---
title: Esempio di trigger di registrazione (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando l'attività è registrata.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "106299333"
---
# <a name="registration-trigger-example-xml"></a>Esempio di trigger di registrazione (XML)

Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando l'attività è registrata.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe. Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

> [!Note]  
> Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>Per definire un'attività per avviare il blocco note alla registrazione

Nell'esempio di codice XML riportato di seguito viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger di registrazione che avvia l'attività quando viene registrata e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita dal Utilità di pianificazione.

> [!Note]  
> Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.

 


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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.
-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.
-   [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): definisce il trigger di registrazione. In questo caso vengono utilizzati solo due elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.
-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.
-   [**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività. In questo caso, viene eseguito il blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




