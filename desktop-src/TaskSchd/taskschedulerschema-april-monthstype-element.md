---
title: Elemento April (monthsType)
description: Specifica che l'attività viene eseguita nell'aprile.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Utilità di pianificazione elemento di aprile
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121242"
---
# <a name="april-monthstype-element"></a><span data-ttu-id="33456-104">Elemento April (monthsType)</span><span class="sxs-lookup"><span data-stu-id="33456-104">April (monthsType) Element</span></span>

<span data-ttu-id="33456-105">Specifica che l'attività viene eseguita nell'aprile.</span><span class="sxs-lookup"><span data-stu-id="33456-105">Specifies that the task runs in April.</span></span>

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="33456-106">L'elemento **April** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="33456-106">The **April** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="33456-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="33456-107">Parent element</span></span>



| <span data-ttu-id="33456-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="33456-108">Element</span></span>                                                                                                          | <span data-ttu-id="33456-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="33456-109">Derived from</span></span>                                                     | <span data-ttu-id="33456-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33456-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33456-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="33456-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="33456-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="33456-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="33456-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="33456-113">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |
| [<span data-ttu-id="33456-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="33456-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="33456-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="33456-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="33456-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="33456-116">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="33456-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="33456-117">Examples</span></span>

<span data-ttu-id="33456-118">Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività ad aprile.</span><span class="sxs-lookup"><span data-stu-id="33456-118">The following XML defines a months calendar that runs the task in April.</span></span>


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="33456-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33456-119">Requirements</span></span>



| <span data-ttu-id="33456-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33456-120">Requirement</span></span> | <span data-ttu-id="33456-121">Valore</span><span class="sxs-lookup"><span data-stu-id="33456-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33456-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33456-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33456-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33456-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33456-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33456-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33456-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33456-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33456-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33456-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33456-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="33456-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="33456-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="33456-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





