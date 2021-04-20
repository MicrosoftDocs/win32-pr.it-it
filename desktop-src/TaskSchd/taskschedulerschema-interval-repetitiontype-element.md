---
title: Elemento Interval (repetitionType)
description: Specifica l'intervallo di tempo tra ogni riavvio dell'attività.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Elemento Interval Utilità di pianificazione
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734196"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="0111b-104">Elemento Interval (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="0111b-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="0111b-105">Specifica l'intervallo di tempo tra ogni riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0111b-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="0111b-106">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti).</span><span class="sxs-lookup"><span data-stu-id="0111b-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="0111b-107">Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="0111b-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0111b-108">L'elemento è definito dal tipo [**complesso repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="0111b-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0111b-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="0111b-109">Parent element</span></span>



| <span data-ttu-id="0111b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="0111b-110">Element</span></span>                                                                      | <span data-ttu-id="0111b-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="0111b-111">Derived from</span></span>                                                             | <span data-ttu-id="0111b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0111b-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0111b-113">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="0111b-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="0111b-114">**tipo ripetizione**</span><span class="sxs-lookup"><span data-stu-id="0111b-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="0111b-115">Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0111b-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0111b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0111b-116">Remarks</span></span>

<span data-ttu-id="0111b-117">Per lo sviluppo di script, l'intervallo del modello di ripetizione viene specificato usando la [**proprietà RepetitionPattern.Interval.**](repetitionpattern-interval.md)</span><span class="sxs-lookup"><span data-stu-id="0111b-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="0111b-118">Per lo sviluppo in C++, l'intervallo del modello di ripetizione viene specificato usando la [**proprietà IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)</span><span class="sxs-lookup"><span data-stu-id="0111b-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0111b-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="0111b-119">Examples</span></span>

<span data-ttu-id="0111b-120">Per un esempio completo del codice XML per un'attività che usa un intervallo di ripetizione, vedere [Esempio di trigger giornaliero (XML).](daily-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="0111b-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0111b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0111b-121">Requirements</span></span>



| <span data-ttu-id="0111b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0111b-122">Requirement</span></span> | <span data-ttu-id="0111b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0111b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0111b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0111b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0111b-125">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0111b-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0111b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0111b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0111b-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0111b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0111b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0111b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0111b-129">Utilità di pianificazione schema</span><span class="sxs-lookup"><span data-stu-id="0111b-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0111b-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0111b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





