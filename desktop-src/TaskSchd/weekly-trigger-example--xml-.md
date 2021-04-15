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
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="8cf0a-103">Esempio di trigger settimanale (XML)</span><span class="sxs-lookup"><span data-stu-id="8cf0a-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="8cf0a-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note su base settimanale.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="8cf0a-105">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8cf0a-106">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8cf0a-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="8cf0a-107">Per definire un'attività per avviare il blocco note ogni altra settimana il lunedì alle 8:00 AM</span><span class="sxs-lookup"><span data-stu-id="8cf0a-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="8cf0a-108">Nell'esempio XML seguente viene illustrato come definire un'attività con una singola azione di esecuzione (avvio del blocco note), un singolo trigger di calendario (avvia l'attività ogni un'altra settimana il lunedì alle 8:00 AM) e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita da Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8cf0a-109">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="8cf0a-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8cf0a-110">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si usa questo esempio.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="8cf0a-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="8cf0a-112">Contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="8cf0a-113">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="8cf0a-114">Definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="8cf0a-115">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="8cf0a-116">Definisce il trigger di calendario settimanale.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="8cf0a-117">In questo caso vengono utilizzati solo quattro elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato, la pianificazione settimanale e i giorni della settimana in cui verrà eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="8cf0a-118">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Calendar.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="8cf0a-119">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="8cf0a-120">Definisce la pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-120">Defines the weekly schedule.</span></span> <span data-ttu-id="8cf0a-121">In questo caso, l'intervallo viene impostato in modo da eseguire l'attività ogni altre settimane di lunedì.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="8cf0a-122">**Principale**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="8cf0a-123">Definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="8cf0a-124">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="8cf0a-125">Definisce le impostazioni dell'attività utilizzate da Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="8cf0a-126">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="8cf0a-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="8cf0a-127">Definisce le azioni eseguite dall'attività, in questo caso l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="8cf0a-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cf0a-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cf0a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf0a-129">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8cf0a-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




