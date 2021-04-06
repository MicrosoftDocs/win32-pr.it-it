---
title: Elemento Subscription (eventTriggerType)
description: Specifica la query XPath che identifica l'evento che attiva il trigger.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Utilità di pianificazione dell'elemento subscription
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743767"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="28c82-104">Elemento Subscription (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="28c82-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="28c82-105">Specifica la query XPath che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="28c82-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="28c82-106">L'elemento **Subscription** è definito dal tipo complesso [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="28c82-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="28c82-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="28c82-107">Parent element</span></span>



| <span data-ttu-id="28c82-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="28c82-108">Element</span></span>                                                                       | <span data-ttu-id="28c82-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="28c82-109">Derived from</span></span>                                                                 | <span data-ttu-id="28c82-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28c82-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="28c82-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="28c82-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="28c82-112">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="28c82-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="28c82-113">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="28c82-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="28c82-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="28c82-114">Remarks</span></span>

<span data-ttu-id="28c82-115">Per lo sviluppo di script, la sottoscrizione dell'evento viene specificata dalla proprietà [**EventTrigger. Subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="28c82-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="28c82-116">Per lo sviluppo in C++, la sottoscrizione dell'evento viene specificata dalla proprietà [**IEventTrigger:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .</span><span class="sxs-lookup"><span data-stu-id="28c82-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c82-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28c82-117">Requirements</span></span>



| <span data-ttu-id="28c82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c82-118">Requirement</span></span> | <span data-ttu-id="28c82-119">Valore</span><span class="sxs-lookup"><span data-stu-id="28c82-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28c82-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28c82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28c82-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28c82-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28c82-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28c82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28c82-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28c82-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28c82-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28c82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c82-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="28c82-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="28c82-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="28c82-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





