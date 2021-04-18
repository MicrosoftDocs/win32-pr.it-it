---
title: Tipo complesso monthlyScheduleType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- Utilità di pianificazione di tipo complesso monthlyScheduleType
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301331"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="d18cc-104">Tipo complesso monthlyScheduleType</span><span class="sxs-lookup"><span data-stu-id="d18cc-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="d18cc-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d18cc-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d18cc-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d18cc-106">Child elements</span></span>



| <span data-ttu-id="d18cc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d18cc-107">Element</span></span>                                                                            | <span data-ttu-id="d18cc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d18cc-108">Type</span></span>                                                                       | <span data-ttu-id="d18cc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d18cc-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d18cc-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="d18cc-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="d18cc-111">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="d18cc-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="d18cc-112">Specifica i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="d18cc-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="d18cc-113">**Mesi**</span><span class="sxs-lookup"><span data-stu-id="d18cc-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="d18cc-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="d18cc-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="d18cc-115">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="d18cc-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d18cc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d18cc-116">Requirements</span></span>



| <span data-ttu-id="d18cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18cc-117">Requirement</span></span> | <span data-ttu-id="d18cc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d18cc-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d18cc-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d18cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d18cc-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d18cc-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d18cc-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d18cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d18cc-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d18cc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d18cc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d18cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18cc-124">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d18cc-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d18cc-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d18cc-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





