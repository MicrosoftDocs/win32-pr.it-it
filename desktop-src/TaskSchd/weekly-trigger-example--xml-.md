---
title: Esempio di trigger settimanale (XML)
description: Il codice XML in questo esempio definisce un'attività che inizia Blocco note su base bi-settimanale.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c038c21db137ce9180d76cecf4c2885274f7cdd72720b12b919f9a39e98e575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001811"
---
# <a name="weekly-trigger-example-xml"></a>Esempio di trigger settimanale (XML)

Il codice XML in questo esempio definisce un'attività che inizia Blocco note su base bi-settimanale.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) per lo scripting) o lo strumento Schtasks.exe da riga di comando. Se si usa lo strumento Schtasks.exe (disponibile nella directory C: Windows System32), è possibile usare il comando seguente per registrare l'attività: \\ \\ **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Per definire un'attività da Blocco note ogni altra settimana il lunedì alle 8:00

L'esempio XML seguente illustra come definire un'attività con una singola azione di esecuzione (a partire da Blocco note), un singolo trigger di calendario (avvia l'attività ogni due settimane il lunedì alle 8:00 AM) e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte di Utilità di pianificazione.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
        </CalendarTrigger>
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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contiene informazioni di registrazione sull'attività.

-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)

    Definisce il trigger che avvia l'attività.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definisce il trigger del calendario settimanale. In questo caso, vengono usati solo quattro elementi figlio: i limiti di inizio e fine che specificano quando il trigger viene attivato e disattivato, la pianificazione settimanale e i giorni della settimana in cui verrà eseguita l'attività. [**L'elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger di calendario.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Definisce la pianificazione settimanale. In questo caso, l'intervallo è impostato per eseguire l'attività ogni due settimane di lunedì.

-   [**Principale**](taskschedulerschema-principal-principaltype-element.md)

    Definisce il contesto di sicurezza in cui viene eseguita un'attività.

-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md)

    Definisce le impostazioni dell'attività Utilità di pianificazione per eseguire l'attività.

-   [**Azioni**](taskschedulerschema-actions-tasktype-element.md)

    Definisce le azioni eseguite dall'attività (in questo caso, l'esecuzione Blocco note).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




