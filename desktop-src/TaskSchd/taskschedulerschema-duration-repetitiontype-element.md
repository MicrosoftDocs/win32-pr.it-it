---
title: Duration (repetitionType)-elemento
description: Specifica il tempo di ripetizione del pattern.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Utilità di pianificazione elemento Duration
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341323"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="afe82-104">Duration (repetitionType)-elemento</span><span class="sxs-lookup"><span data-stu-id="afe82-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="afe82-105">Specifica il tempo di ripetizione del pattern.</span><span class="sxs-lookup"><span data-stu-id="afe82-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="afe82-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="afe82-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="afe82-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="afe82-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="afe82-108">Se non viene specificato alcun valore per la durata, il modello viene ripetuto per un tempo illimitato.</span><span class="sxs-lookup"><span data-stu-id="afe82-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="afe82-109">Il valore minimo è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="afe82-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="afe82-110">L'elemento è definito dal tipo complesso [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="afe82-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="afe82-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="afe82-111">Parent element</span></span>



| <span data-ttu-id="afe82-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="afe82-112">Element</span></span>                                                                      | <span data-ttu-id="afe82-113">Derivato da</span><span class="sxs-lookup"><span data-stu-id="afe82-113">Derived from</span></span>                                                             | <span data-ttu-id="afe82-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afe82-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afe82-115">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="afe82-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="afe82-116">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="afe82-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="afe82-117">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="afe82-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="afe82-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="afe82-118">Remarks</span></span>

<span data-ttu-id="afe82-119">Per le applicazioni di scripting, la durata del modello viene specificata utilizzando la proprietà [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .</span><span class="sxs-lookup"><span data-stu-id="afe82-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="afe82-120">Per le applicazioni C++, la durata del modello viene specificata tramite la proprietà [**IRepetitionPattern::D uration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="afe82-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="afe82-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="afe82-121">Examples</span></span>

<span data-ttu-id="afe82-122">Nel codice XML seguente viene definito un modello di ripetizione per un trigger.</span><span class="sxs-lookup"><span data-stu-id="afe82-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="afe82-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afe82-123">Requirements</span></span>



| <span data-ttu-id="afe82-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe82-124">Requirement</span></span> | <span data-ttu-id="afe82-125">Valore</span><span class="sxs-lookup"><span data-stu-id="afe82-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="afe82-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afe82-126">Minimum supported client</span></span><br/> | <span data-ttu-id="afe82-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afe82-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="afe82-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afe82-128">Minimum supported server</span></span><br/> | <span data-ttu-id="afe82-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afe82-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afe82-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afe82-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe82-131">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="afe82-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="afe82-132">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="afe82-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





