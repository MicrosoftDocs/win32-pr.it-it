---
title: Esempio di trigger settimanale (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note su base settimanale.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104398435"
---
# <a name="weekly-trigger-example-xml"></a>Esempio di trigger settimanale (XML)

Il codice XML in questo esempio definisce un'attività che avvia il blocco note su base settimanale.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe. Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Per definire un'attività per avviare il blocco note ogni altra settimana il lunedì alle 8:00 AM

Nell'esempio XML seguente viene illustrato come definire un'attività con una singola azione di esecuzione (avvio del blocco note), un singolo trigger di calendario (avvia l'attività ogni un'altra settimana il lunedì alle 8:00 AM) e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita da Utilità di pianificazione.


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

    Contiene le informazioni di registrazione relative all'attività.

-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)

    Definisce il trigger che avvia l'attività.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definisce il trigger di calendario settimanale. In questo caso vengono utilizzati solo quattro elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato, la pianificazione settimanale e i giorni della settimana in cui verrà eseguita l'attività. L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Calendar.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Definisce la pianificazione settimanale. In questo caso, l'intervallo viene impostato in modo da eseguire l'attività ogni altre settimane di lunedì.

-   [**Principale**](taskschedulerschema-principal-principaltype-element.md)

    Definisce il contesto di sicurezza in cui viene eseguita un'attività.

-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md)

    Definisce le impostazioni dell'attività utilizzate da Utilità di pianificazione per eseguire l'attività.

-   [**Azioni**](taskschedulerschema-actions-tasktype-element.md)

    Definisce le azioni eseguite dall'attività, in questo caso l'esecuzione del blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




