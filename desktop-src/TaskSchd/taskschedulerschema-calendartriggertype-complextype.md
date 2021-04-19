---
title: Tipo complesso calendarTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi del calendario.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Utilità di pianificazione di tipo complesso calendarTriggerType
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302005"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="8d1c5-104">Tipo complesso calendarTriggerType</span><span class="sxs-lookup"><span data-stu-id="8d1c5-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="8d1c5-105">Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi del calendario.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8d1c5-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8d1c5-106">Child elements</span></span>



| <span data-ttu-id="8d1c5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d1c5-107">Element</span></span>                                                                                                      | <span data-ttu-id="8d1c5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d1c5-108">Type</span></span>                                                                                                 | <span data-ttu-id="8d1c5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d1c5-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d1c5-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="8d1c5-111">duration</span><span class="sxs-lookup"><span data-stu-id="8d1c5-111">duration</span></span>                                                                                             | <span data-ttu-id="8d1c5-112">Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="8d1c5-113">Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).</span><span class="sxs-lookup"><span data-stu-id="8d1c5-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="8d1c5-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="8d1c5-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="8d1c5-116">Specifica una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-116">Specifies a daily schedule.</span></span> <span data-ttu-id="8d1c5-117">Ad esempio, l'attività viene avviata ogni giorno, ogni giorno, ogni tre giorni e così via.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="8d1c5-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="8d1c5-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="8d1c5-120">Specifica una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="8d1c5-121">Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese per mesi specifici.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="8d1c5-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="8d1c5-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="8d1c5-124">Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="8d1c5-125">Ad esempio, l'attività viene avviata in giorni specifici della settimana, settimane del mese e mesi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="8d1c5-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="8d1c5-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8d1c5-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="8d1c5-128">Specifica una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="8d1c5-129">Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana.</span><span class="sxs-lookup"><span data-stu-id="8d1c5-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="8d1c5-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d1c5-130">Remarks</span></span>

<span data-ttu-id="8d1c5-131">Oltre all'elemento figlio definito qui, l'elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1c5-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1c5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d1c5-132">Requirements</span></span>



| <span data-ttu-id="8d1c5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d1c5-133">Requirement</span></span> | <span data-ttu-id="8d1c5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8d1c5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8d1c5-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d1c5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8d1c5-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d1c5-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8d1c5-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d1c5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8d1c5-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d1c5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d1c5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d1c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1c5-140">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8d1c5-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8d1c5-141">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8d1c5-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





