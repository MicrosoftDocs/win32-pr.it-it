---
title: Tipo complesso daysOfMonthType
description: Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- Utilità di pianificazione di tipo complesso daysOfMonthType
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400831"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="3f98a-104">Tipo complesso daysOfMonthType</span><span class="sxs-lookup"><span data-stu-id="3f98a-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="3f98a-105">Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3f98a-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3f98a-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3f98a-106">Child elements</span></span>



| <span data-ttu-id="3f98a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3f98a-107">Element</span></span>                                                        | <span data-ttu-id="3f98a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f98a-108">Type</span></span>                                                                    | <span data-ttu-id="3f98a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f98a-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3f98a-110">**Giorno**</span><span class="sxs-lookup"><span data-stu-id="3f98a-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="3f98a-111">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="3f98a-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="3f98a-112">Specifica un giorno del mese durante il quale viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="3f98a-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3f98a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f98a-113">Requirements</span></span>



| <span data-ttu-id="3f98a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f98a-114">Requirement</span></span> | <span data-ttu-id="3f98a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3f98a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f98a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f98a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f98a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f98a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f98a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f98a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f98a-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f98a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f98a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f98a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f98a-121">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3f98a-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3f98a-122">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3f98a-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





