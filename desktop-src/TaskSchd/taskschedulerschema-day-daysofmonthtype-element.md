---
title: Elemento Day (daysOfMonthType)
description: Specifica un giorno del mese durante il quale viene eseguita l'attività.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Utilità di pianificazione elemento Day
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048092"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="a171f-104">Elemento Day (daysOfMonthType)</span><span class="sxs-lookup"><span data-stu-id="a171f-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="a171f-105">Specifica un giorno del mese durante il quale viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="a171f-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="a171f-106">L'elemento **Day** è definito dal tipo complesso [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a171f-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a171f-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="a171f-107">Parent element</span></span>



| <span data-ttu-id="a171f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a171f-108">Element</span></span>                                                                            | <span data-ttu-id="a171f-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="a171f-109">Derived from</span></span>                                                               | <span data-ttu-id="a171f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a171f-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a171f-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="a171f-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="a171f-112">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="a171f-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="a171f-113">Specifica i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="a171f-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="a171f-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="a171f-114">Examples</span></span>

<span data-ttu-id="a171f-115">Il codice XML seguente definisce la parte relativa ai giorni di un calendario mensile che esegue l'attività il primo e il quindicesimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="a171f-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="a171f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a171f-116">Requirements</span></span>



| <span data-ttu-id="a171f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a171f-117">Requirement</span></span> | <span data-ttu-id="a171f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a171f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a171f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a171f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a171f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a171f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a171f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a171f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a171f-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a171f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a171f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a171f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a171f-124">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a171f-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





