---
title: EventTrigger. Subscription (proprietà)
description: Per gli script, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Utilità di pianificazione proprietà sottoscrizione
- Utilità di pianificazione proprietà di sottoscrizione, oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, Proprietà Subscription
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302230"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="5f6fa-106">EventTrigger. Subscription (proprietà)</span><span class="sxs-lookup"><span data-stu-id="5f6fa-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="5f6fa-107">Per gli script, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="5f6fa-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f6fa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f6fa-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="5f6fa-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5f6fa-109">Property value</span></span>

<span data-ttu-id="5f6fa-110">Stringa di query che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="5f6fa-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f6fa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f6fa-111">Remarks</span></span>

<span data-ttu-id="5f6fa-112">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, la sottoscrizione dell'evento viene specificata utilizzando l'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5f6fa-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="5f6fa-113">Per ulteriori informazioni sulla scrittura di una stringa di query per determinati eventi, vedere [selezione](/previous-versions//aa385231(v=vs.85)) di eventi e [sottoscrizione degli eventi](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="5f6fa-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5f6fa-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="5f6fa-114">Examples</span></span>

<span data-ttu-id="5f6fa-115">La stringa di query seguente definisce una sottoscrizione a tutti gli eventi di livello 2 nel canale di sistema:</span><span class="sxs-lookup"><span data-stu-id="5f6fa-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="5f6fa-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f6fa-116">Requirements</span></span>



| <span data-ttu-id="5f6fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f6fa-117">Requirement</span></span> | <span data-ttu-id="5f6fa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6fa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6fa-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f6fa-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f6fa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f6fa-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f6fa-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f6fa-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f6fa-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5f6fa-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f6fa-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f6fa-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f6fa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f6fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f6fa-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f6fa-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f6fa-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f6fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6fa-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5f6fa-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5f6fa-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="5f6fa-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

