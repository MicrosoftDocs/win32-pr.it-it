---
title: Proprietà RunningTaskCollection. Item
description: Per gli script, ottiene l'attività specificata dalla raccolta.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto RunningTaskCollection
- Oggetto RunningTaskCollection Utilità di pianificazione, proprietà Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120418"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="578ee-106">Proprietà RunningTaskCollection. Item</span><span class="sxs-lookup"><span data-stu-id="578ee-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="578ee-107">Per gli script, ottiene l'attività specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="578ee-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="578ee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="578ee-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="578ee-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="578ee-109">Property value</span></span>

<span data-ttu-id="578ee-110">Oggetto [**RunningTask**](runningtask.md) che contiene il contesto richiesto.</span><span class="sxs-lookup"><span data-stu-id="578ee-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="578ee-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="578ee-111">Remarks</span></span>

<span data-ttu-id="578ee-112">Le raccolte sono in base 1.</span><span class="sxs-lookup"><span data-stu-id="578ee-112">Collections are 1-based.</span></span> <span data-ttu-id="578ee-113">In altre parole, l'indice per il primo elemento nella raccolta è 1.</span><span class="sxs-lookup"><span data-stu-id="578ee-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="578ee-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="578ee-114">Requirements</span></span>



| <span data-ttu-id="578ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="578ee-115">Requirement</span></span> | <span data-ttu-id="578ee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="578ee-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="578ee-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="578ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="578ee-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="578ee-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="578ee-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="578ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="578ee-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="578ee-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="578ee-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="578ee-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="578ee-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="578ee-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="578ee-123">DLL</span><span class="sxs-lookup"><span data-stu-id="578ee-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="578ee-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="578ee-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="578ee-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="578ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578ee-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="578ee-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





