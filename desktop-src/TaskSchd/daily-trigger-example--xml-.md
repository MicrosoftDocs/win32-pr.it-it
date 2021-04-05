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
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="b2b90-103">Esempio di trigger giornaliero (XML)</span><span class="sxs-lookup"><span data-stu-id="b2b90-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="b2b90-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note alle 8:00 AM ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="b2b90-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="b2b90-105">Nell'esempio viene inoltre illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="b2b90-106">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="b2b90-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="b2b90-107">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="b2b90-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="b2b90-108">Per definire un'attività per avviare il blocco note ogni giorno alle 8:00</span><span class="sxs-lookup"><span data-stu-id="b2b90-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="b2b90-109">Nell'esempio XML seguente viene illustrato come definire un'attività con una singola azione di esecuzione (avvio del blocco note), un singolo trigger di calendario (avvia l'attività ogni giorno alle 8:00) e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b2b90-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="b2b90-110">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="b2b90-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="b2b90-111">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si usa questo esempio.</span><span class="sxs-lookup"><span data-stu-id="b2b90-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="b2b90-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b2b90-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="b2b90-113">Contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="b2b90-114">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="b2b90-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="b2b90-115">Definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="b2b90-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2b90-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="b2b90-117">Definisce il trigger di calendario giornaliero.</span><span class="sxs-lookup"><span data-stu-id="b2b90-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="b2b90-118">In questo caso, vengono utilizzati quattro elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato, la pianificazione giornaliera e il modello di ripetizione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="b2b90-119">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Calendar.</span><span class="sxs-lookup"><span data-stu-id="b2b90-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="b2b90-120">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="b2b90-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="b2b90-121">Definisce la pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="b2b90-121">Defines the daily schedule.</span></span> <span data-ttu-id="b2b90-122">In questo caso, l'intervallo viene impostato in modo da eseguire ogni giorno l'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="b2b90-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="b2b90-124">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="b2b90-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="b2b90-125">Definisce le impostazioni dell'attività utilizzate da Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b90-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="b2b90-126">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="b2b90-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="b2b90-127">Definisce le azioni eseguite dall'attività, in questo caso l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="b2b90-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b90-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2b90-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b90-129">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b2b90-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




