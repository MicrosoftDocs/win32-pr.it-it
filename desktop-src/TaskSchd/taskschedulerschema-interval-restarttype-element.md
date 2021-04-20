---
title: Elemento Interval (restartType)
description: Specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734186"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="16af4-104">Elemento Interval (restartType)</span><span class="sxs-lookup"><span data-stu-id="16af4-104">Interval (restartType) Element</span></span>

<span data-ttu-id="16af4-105">Specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="16af4-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="16af4-106">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti).</span><span class="sxs-lookup"><span data-stu-id="16af4-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="16af4-107">Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="16af4-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="16af4-108">L'elemento è definito dal [**tipo complesso restartType.**](taskschedulerschema-restarttype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="16af4-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="16af4-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="16af4-109">Parent element</span></span>



| <span data-ttu-id="16af4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="16af4-110">Element</span></span>                                                                               | <span data-ttu-id="16af4-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="16af4-111">Derived from</span></span>                                                       | <span data-ttu-id="16af4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16af4-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16af4-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="16af4-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="16af4-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="16af4-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="16af4-115">Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività ha esito negativo per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="16af4-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="16af4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="16af4-116">Remarks</span></span>

<span data-ttu-id="16af4-117">Se questo elemento viene specificato, è necessario specificare anche l'elemento [**Count**](taskschedulerschema-count-restarttype-element.md) per indicare al Utilità di pianificazione quante volte deve tentare di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="16af4-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="16af4-118">Per lo sviluppo in C++, vedere [**Proprietà RestartInterval di ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)</span><span class="sxs-lookup"><span data-stu-id="16af4-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="16af4-119">Per lo sviluppo di script, [**vedere TaskSettings.RestartInterval.**](tasksettings-restartinterval.md)</span><span class="sxs-lookup"><span data-stu-id="16af4-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16af4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16af4-120">Requirements</span></span>



| <span data-ttu-id="16af4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="16af4-121">Requirement</span></span> | <span data-ttu-id="16af4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="16af4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16af4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16af4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="16af4-124">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16af4-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16af4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16af4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="16af4-126">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="16af4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16af4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16af4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16af4-128">Utilità di pianificazione schema</span><span class="sxs-lookup"><span data-stu-id="16af4-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





