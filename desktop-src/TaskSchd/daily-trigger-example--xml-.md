---
title: Esempio di trigger giornaliero (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note alle 8 00 AM ogni giorno.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "103719986"
---
# <a name="daily-trigger-example-xml"></a>Esempio di trigger giornaliero (XML)

Il codice XML in questo esempio definisce un'attività che avvia il blocco note alle 8:00 AM ogni giorno. Nell'esempio viene inoltre illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività.

Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe. Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>Per definire un'attività per avviare il blocco note ogni giorno alle 8:00

Nell'esempio XML seguente viene illustrato come definire un'attività con una singola azione di esecuzione (avvio del blocco note), un singolo trigger di calendario (avvia l'attività ogni giorno alle 8:00) e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte di Utilità di pianificazione.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
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

    Definisce il trigger di calendario giornaliero. In questo caso, vengono utilizzati quattro elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato, la pianificazione giornaliera e il modello di ripetizione per l'attività. L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Calendar.

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Definisce la pianificazione giornaliera. In questo caso, l'intervallo viene impostato in modo da eseguire ogni giorno l'attività.

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.
-   [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md)

    Definisce le impostazioni dell'attività utilizzate da Utilità di pianificazione per eseguire l'attività.

-   [**Azioni**](taskschedulerschema-actions-tasktype-element.md)

    Definisce le azioni eseguite dall'attività, in questo caso l'esecuzione del blocco note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




