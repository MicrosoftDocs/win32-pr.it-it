---
title: Elemento February (monthsType)
description: Specifica che l'attività viene eseguita nel febbraio.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Utilità di pianificazione elemento di febbraio
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302490"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="c0a3c-104">Elemento February (monthsType)</span><span class="sxs-lookup"><span data-stu-id="c0a3c-104">February (monthsType) Element</span></span>

<span data-ttu-id="c0a3c-105">Specifica che l'attività viene eseguita nel febbraio.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c0a3c-106">L'elemento **February** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a3c-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c0a3c-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c0a3c-107">Parent element</span></span>



| <span data-ttu-id="c0a3c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0a3c-108">Element</span></span>                                                                                                          | <span data-ttu-id="c0a3c-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="c0a3c-109">Derived from</span></span>                                                     | <span data-ttu-id="c0a3c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0a3c-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a3c-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c0a3c-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c0a3c-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c0a3c-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c0a3c-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c0a3c-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c0a3c-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="c0a3c-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c0a3c-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c0a3c-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="c0a3c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0a3c-117">Examples</span></span>

<span data-ttu-id="c0a3c-118">Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività in febbraio.</span><span class="sxs-lookup"><span data-stu-id="c0a3c-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="c0a3c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0a3c-119">Requirements</span></span>



| <span data-ttu-id="c0a3c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a3c-120">Requirement</span></span> | <span data-ttu-id="c0a3c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c0a3c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0a3c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0a3c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a3c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0a3c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0a3c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0a3c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a3c-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0a3c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0a3c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0a3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a3c-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c0a3c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c0a3c-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c0a3c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





