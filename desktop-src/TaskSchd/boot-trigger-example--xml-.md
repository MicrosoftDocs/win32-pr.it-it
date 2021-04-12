---
title: Esempio di trigger di avvio (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando il sistema viene avviato.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336037"
---
# <a name="boot-trigger-example-xml"></a>Esempio di trigger di avvio (XML)

Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando il sistema viene avviato.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe. Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Per definire un'attività per avviare il blocco note all'avvio del sistema

Nell'esempio XML seguente viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger di avvio che avvia l'attività quando viene avviato il sistema e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte del Utilità di pianificazione.


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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.
-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): definisce il trigger di avvio. In questo caso vengono utilizzati solo due elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.
-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.
-   [**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività. In questo caso, viene eseguito il blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




