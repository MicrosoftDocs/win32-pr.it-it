---
title: Elemento November (monthsType)
description: Specifica che l'attività viene eseguita nel novembre.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Utilità di pianificazione dell'elemento November
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301904"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="94abf-104">Elemento November (monthsType)</span><span class="sxs-lookup"><span data-stu-id="94abf-104">November (monthsType) Element</span></span>

<span data-ttu-id="94abf-105">Specifica che l'attività viene eseguita nel novembre.</span><span class="sxs-lookup"><span data-stu-id="94abf-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="94abf-106">L'elemento **November** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="94abf-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="94abf-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="94abf-107">Parent element</span></span>



| <span data-ttu-id="94abf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="94abf-108">Element</span></span>                                                                                                          | <span data-ttu-id="94abf-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="94abf-109">Derived from</span></span>                                                     | <span data-ttu-id="94abf-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94abf-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94abf-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="94abf-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="94abf-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="94abf-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="94abf-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="94abf-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="94abf-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="94abf-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="94abf-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="94abf-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="94abf-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="94abf-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="94abf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="94abf-117">Examples</span></span>

<span data-ttu-id="94abf-118">Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di novembre.</span><span class="sxs-lookup"><span data-stu-id="94abf-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="94abf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94abf-119">Requirements</span></span>



| <span data-ttu-id="94abf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="94abf-120">Requirement</span></span> | <span data-ttu-id="94abf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="94abf-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94abf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94abf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94abf-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94abf-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94abf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94abf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94abf-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94abf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94abf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94abf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94abf-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="94abf-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="94abf-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="94abf-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





