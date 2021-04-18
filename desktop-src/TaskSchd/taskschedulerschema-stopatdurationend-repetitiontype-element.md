---
title: Elemento StopAtDurationEnd (repetitionType)
description: Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Utilità di pianificazione elemento StopAtDurationEnd
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302680"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="13ea0-104">Elemento StopAtDurationEnd (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="13ea0-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="13ea0-105">Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="13ea0-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="13ea0-106">Questa operazione è applicabile solo se le ripetizioni sono impostate.</span><span class="sxs-lookup"><span data-stu-id="13ea0-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="13ea0-107">L'elemento **StopAtDurationEnd** è definito dal tipo complesso [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="13ea0-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="13ea0-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="13ea0-108">Parent element</span></span>

| <span data-ttu-id="13ea0-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="13ea0-109">Element</span></span> | <span data-ttu-id="13ea0-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="13ea0-110">Derived from</span></span> | <span data-ttu-id="13ea0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13ea0-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="13ea0-112">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="13ea0-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="13ea0-113">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="13ea0-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="13ea0-114">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="13ea0-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="13ea0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="13ea0-115">Remarks</span></span>

<span data-ttu-id="13ea0-116">Per lo sviluppo di script, questa impostazione viene specificata tramite la proprietà [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .</span><span class="sxs-lookup"><span data-stu-id="13ea0-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="13ea0-117">Per lo sviluppo in C++, questa impostazione viene specificata tramite la proprietà [**IRepetitionPattern:: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .</span><span class="sxs-lookup"><span data-stu-id="13ea0-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ea0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13ea0-118">Requirements</span></span>

| <span data-ttu-id="13ea0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ea0-119">Requirement</span></span> | <span data-ttu-id="13ea0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="13ea0-120">Value</span></span> |
|-|-|
| <span data-ttu-id="13ea0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13ea0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13ea0-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13ea0-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13ea0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13ea0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13ea0-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13ea0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="13ea0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13ea0-125">See also</span></span>

[<span data-ttu-id="13ea0-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="13ea0-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="13ea0-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="13ea0-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
