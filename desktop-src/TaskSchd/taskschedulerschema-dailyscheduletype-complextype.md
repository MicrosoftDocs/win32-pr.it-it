---
title: Tipo complesso dailyScheduleType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- Utilità di pianificazione di tipo complesso dailyScheduleType
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302169"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="cd822-104">Tipo complesso dailyScheduleType</span><span class="sxs-lookup"><span data-stu-id="cd822-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="cd822-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cd822-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cd822-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cd822-106">Child elements</span></span>



| <span data-ttu-id="cd822-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cd822-107">Element</span></span>                                                                            | <span data-ttu-id="cd822-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd822-108">Type</span></span> | <span data-ttu-id="cd822-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd822-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="cd822-110">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="cd822-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="cd822-111">Specifica l'intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd822-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cd822-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd822-112">Requirements</span></span>



| <span data-ttu-id="cd822-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd822-113">Requirement</span></span> | <span data-ttu-id="cd822-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cd822-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd822-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd822-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cd822-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd822-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd822-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd822-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cd822-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd822-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd822-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd822-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd822-120">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="cd822-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cd822-121">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="cd822-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





