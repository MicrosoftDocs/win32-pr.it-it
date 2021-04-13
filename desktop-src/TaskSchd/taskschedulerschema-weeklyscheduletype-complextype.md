---
title: Tipo complesso weeklyScheduleType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- Utilità di pianificazione di tipo complesso weeklyScheduleType
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400469"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="0ace8-104">Tipo complesso weeklyScheduleType</span><span class="sxs-lookup"><span data-stu-id="0ace8-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="0ace8-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0ace8-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0ace8-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0ace8-106">Child elements</span></span>



| <span data-ttu-id="0ace8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ace8-107">Element</span></span>                                                                               | <span data-ttu-id="0ace8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ace8-108">Type</span></span>                                                                     | <span data-ttu-id="0ace8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ace8-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0ace8-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="0ace8-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="0ace8-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0ace8-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0ace8-112">Specifica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0ace8-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="0ace8-113">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="0ace8-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="0ace8-114">Specifica l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0ace8-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0ace8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ace8-115">Requirements</span></span>



| <span data-ttu-id="0ace8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ace8-116">Requirement</span></span> | <span data-ttu-id="0ace8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0ace8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ace8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ace8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ace8-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ace8-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ace8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ace8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ace8-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ace8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ace8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ace8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ace8-123">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0ace8-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





