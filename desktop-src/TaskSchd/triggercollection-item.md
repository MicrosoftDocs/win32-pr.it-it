---
title: Proprietà TriggerCollection. Item
description: Per gli script, ottiene il trigger specificato dalla raccolta.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto TriggerCollection
- TriggerCollection, oggetto Utilità di pianificazione, proprietà Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740775"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="76b46-106">Proprietà TriggerCollection. Item</span><span class="sxs-lookup"><span data-stu-id="76b46-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="76b46-107">Per gli script, ottiene il trigger specificato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="76b46-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76b46-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="76b46-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="76b46-109">Property value</span></span>

<span data-ttu-id="76b46-110">Oggetto [**trigger**](trigger.md) che rappresenta il trigger richiesto.</span><span class="sxs-lookup"><span data-stu-id="76b46-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="76b46-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="76b46-111">Remarks</span></span>

<span data-ttu-id="76b46-112">Le raccolte sono in base 1.</span><span class="sxs-lookup"><span data-stu-id="76b46-112">Collections are 1-based.</span></span> <span data-ttu-id="76b46-113">In altre parole, l'indice per il primo elemento nella raccolta è 1.</span><span class="sxs-lookup"><span data-stu-id="76b46-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b46-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76b46-114">Requirements</span></span>



| <span data-ttu-id="76b46-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76b46-115">Requirement</span></span> | <span data-ttu-id="76b46-116">Valore</span><span class="sxs-lookup"><span data-stu-id="76b46-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76b46-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b46-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76b46-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76b46-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76b46-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76b46-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76b46-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76b46-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76b46-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="76b46-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="76b46-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76b46-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76b46-123">DLL</span><span class="sxs-lookup"><span data-stu-id="76b46-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b46-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76b46-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76b46-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76b46-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b46-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="76b46-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





