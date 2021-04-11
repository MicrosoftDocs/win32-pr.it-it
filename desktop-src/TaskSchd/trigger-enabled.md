---
title: Proprietà trigger. Enabled
description: Per gli script, ottiene o imposta un valore booleano che indica se il trigger è abilitato.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Utilità di pianificazione proprietà abilitata
- Utilità di pianificazione proprietà abilitata, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963980"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="d7520-106">Proprietà trigger. Enabled</span><span class="sxs-lookup"><span data-stu-id="d7520-106">Trigger.Enabled property</span></span>

<span data-ttu-id="d7520-107">Per gli script, ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d7520-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7520-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7520-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d7520-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d7520-109">Property value</span></span>

<span data-ttu-id="d7520-110">True se il trigger è abilitato. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="d7520-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="d7520-111">Il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="d7520-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7520-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7520-112">Remarks</span></span>

<span data-ttu-id="d7520-113">Durante la lettura o la scrittura di codice XML per un'attività, la proprietà Enabled viene specificata utilizzando l'elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d7520-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7520-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7520-114">Requirements</span></span>



| <span data-ttu-id="d7520-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7520-115">Requirement</span></span> | <span data-ttu-id="d7520-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d7520-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7520-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7520-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7520-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7520-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7520-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7520-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7520-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7520-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7520-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d7520-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7520-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7520-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7520-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d7520-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7520-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7520-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7520-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7520-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7520-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d7520-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





