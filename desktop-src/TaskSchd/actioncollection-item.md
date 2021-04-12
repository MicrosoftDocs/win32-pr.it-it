---
title: Proprietà ActionCollection. Item
description: Per lo scripting, ottiene un'azione specificata dalla raccolta.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, proprietà Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400801"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="3f5b0-106">Proprietà ActionCollection. Item</span><span class="sxs-lookup"><span data-stu-id="3f5b0-106">ActionCollection.Item property</span></span>

<span data-ttu-id="3f5b0-107">Per lo scripting, ottiene un'azione specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="3f5b0-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5b0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f5b0-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="3f5b0-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3f5b0-109">Property value</span></span>

<span data-ttu-id="3f5b0-110">Oggetto [**azione**](action.md) che rappresenta l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="3f5b0-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f5b0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f5b0-111">Remarks</span></span>

<span data-ttu-id="3f5b0-112">Le raccolte sono in base 1.</span><span class="sxs-lookup"><span data-stu-id="3f5b0-112">Collections are 1-based.</span></span> <span data-ttu-id="3f5b0-113">In altre parole, l'indice per il primo elemento nella raccolta è 1.</span><span class="sxs-lookup"><span data-stu-id="3f5b0-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5b0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f5b0-114">Requirements</span></span>



| <span data-ttu-id="3f5b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5b0-115">Requirement</span></span> | <span data-ttu-id="3f5b0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3f5b0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5b0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f5b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5b0-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f5b0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f5b0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f5b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5b0-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f5b0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f5b0-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3f5b0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f5b0-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b0-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f5b0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3f5b0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f5b0-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b0-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5b0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f5b0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5b0-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3f5b0-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3f5b0-127">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="3f5b0-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





