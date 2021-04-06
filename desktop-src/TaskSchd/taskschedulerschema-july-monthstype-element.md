---
title: Elemento July (monthsType)
description: Specifica che l'attività viene eseguita nel luglio.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Utilità di pianificazione elemento di luglio
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742903"
---
# <a name="july-monthstype-element"></a><span data-ttu-id="54bfe-104">Elemento July (monthsType)</span><span class="sxs-lookup"><span data-stu-id="54bfe-104">July (monthsType) Element</span></span>

<span data-ttu-id="54bfe-105">Specifica che l'attività viene eseguita nel luglio.</span><span class="sxs-lookup"><span data-stu-id="54bfe-105">Specifies that the task runs in July.</span></span>

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="54bfe-106">L'elemento **July** viene definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54bfe-106">The **July** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="54bfe-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="54bfe-107">Parent element</span></span>



| <span data-ttu-id="54bfe-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="54bfe-108">Element</span></span>                                                                                                          | <span data-ttu-id="54bfe-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="54bfe-109">Derived from</span></span>                                                     | <span data-ttu-id="54bfe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54bfe-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54bfe-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="54bfe-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="54bfe-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="54bfe-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="54bfe-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="54bfe-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="54bfe-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="54bfe-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="54bfe-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="54bfe-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="54bfe-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="54bfe-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="54bfe-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="54bfe-117">Examples</span></span>

<span data-ttu-id="54bfe-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività nel mese di luglio.</span><span class="sxs-lookup"><span data-stu-id="54bfe-118">The following XML defines a months calendar that runs the task in July.</span></span>


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="54bfe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54bfe-119">Requirements</span></span>



| <span data-ttu-id="54bfe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54bfe-120">Requirement</span></span> | <span data-ttu-id="54bfe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="54bfe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54bfe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54bfe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54bfe-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54bfe-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54bfe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54bfe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54bfe-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54bfe-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54bfe-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54bfe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bfe-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="54bfe-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="54bfe-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="54bfe-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





