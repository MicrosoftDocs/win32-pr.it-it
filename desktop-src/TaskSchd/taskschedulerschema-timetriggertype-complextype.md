---
title: Tipo complesso timeTriggerType
description: Definisce il tipo di base per l'elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Tipo complesso timeTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734136"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="24f57-104">Tipo complesso timeTriggerType</span><span class="sxs-lookup"><span data-stu-id="24f57-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="24f57-105">Definisce il tipo di base per [**l'elemento TimeTrigger.**](taskschedulerschema-timetrigger-triggergroup-element.md)</span><span class="sxs-lookup"><span data-stu-id="24f57-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="24f57-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="24f57-106">Child elements</span></span>



| <span data-ttu-id="24f57-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="24f57-107">Element</span></span>                                                                        | <span data-ttu-id="24f57-108">Type</span><span class="sxs-lookup"><span data-stu-id="24f57-108">Type</span></span>     | <span data-ttu-id="24f57-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24f57-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24f57-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="24f57-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="24f57-111">duration</span><span class="sxs-lookup"><span data-stu-id="24f57-111">duration</span></span> | <span data-ttu-id="24f57-112">Specifica il tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="24f57-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="24f57-113">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).</span><span class="sxs-lookup"><span data-stu-id="24f57-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="24f57-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="24f57-114">Remarks</span></span>

<span data-ttu-id="24f57-115">Si noti che questo elemento non aggiunge elementi figlio a quelli definiti dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="24f57-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f57-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24f57-116">Requirements</span></span>



| <span data-ttu-id="24f57-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f57-117">Requirement</span></span> | <span data-ttu-id="24f57-118">Valore</span><span class="sxs-lookup"><span data-stu-id="24f57-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24f57-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f57-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24f57-120">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24f57-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24f57-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f57-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24f57-122">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="24f57-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24f57-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24f57-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f57-124">Utilità di pianificazione complessi dello schema</span><span class="sxs-lookup"><span data-stu-id="24f57-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="24f57-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="24f57-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





