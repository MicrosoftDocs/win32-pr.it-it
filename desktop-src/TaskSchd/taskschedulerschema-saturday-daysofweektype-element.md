---
title: Elemento Saturday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il sabato.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Utilità di pianificazione elemento sabato
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742895"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="8055d-104">Elemento Saturday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="8055d-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="8055d-105">Specifica che l'attività viene eseguita il sabato.</span><span class="sxs-lookup"><span data-stu-id="8055d-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="8055d-106">L'elemento **sabati** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8055d-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8055d-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="8055d-107">Parent element</span></span>



| <span data-ttu-id="8055d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8055d-108">Element</span></span>                                                                                                                  | <span data-ttu-id="8055d-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="8055d-109">Derived from</span></span>                                                             | <span data-ttu-id="8055d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8055d-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8055d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="8055d-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="8055d-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="8055d-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="8055d-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="8055d-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="8055d-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="8055d-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="8055d-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="8055d-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="8055d-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="8055d-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="8055d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="8055d-117">Examples</span></span>

<span data-ttu-id="8055d-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività sabato.</span><span class="sxs-lookup"><span data-stu-id="8055d-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="8055d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8055d-119">Requirements</span></span>



| <span data-ttu-id="8055d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8055d-120">Requirement</span></span> | <span data-ttu-id="8055d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8055d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8055d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8055d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8055d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8055d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8055d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8055d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8055d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8055d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8055d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8055d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8055d-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8055d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8055d-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8055d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





