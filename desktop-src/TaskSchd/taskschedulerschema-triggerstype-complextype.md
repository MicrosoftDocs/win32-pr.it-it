---
title: Tipo complesso triggersType
description: Definisce il gruppo (triggerGroup) per tutti gli elementi trigger.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- Utilità di pianificazione di tipo complesso triggersType
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302676"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="312cb-104">Tipo complesso triggersType</span><span class="sxs-lookup"><span data-stu-id="312cb-104">triggersType Complex Type</span></span>

<span data-ttu-id="312cb-105">Definisce il gruppo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) per tutti gli elementi trigger.</span><span class="sxs-lookup"><span data-stu-id="312cb-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="312cb-106">Il gruppo [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene l'elenco dei trigger che possono essere usati in un'attività.</span><span class="sxs-lookup"><span data-stu-id="312cb-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="312cb-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="312cb-107">Requirements</span></span>



| <span data-ttu-id="312cb-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="312cb-108">Requirement</span></span> | <span data-ttu-id="312cb-109">Valore</span><span class="sxs-lookup"><span data-stu-id="312cb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="312cb-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="312cb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="312cb-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="312cb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="312cb-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="312cb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="312cb-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="312cb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="312cb-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="312cb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312cb-115">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="312cb-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





