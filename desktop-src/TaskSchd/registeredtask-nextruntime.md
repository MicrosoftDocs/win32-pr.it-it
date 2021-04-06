---
title: Proprietà RegisteredTask. NextRunTime
description: Per lo scripting, ottiene l'ora in cui l'attività registrata viene pianificata per l'esecuzione successiva.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Utilità di pianificazione Proprietà NextRunTime
- Utilità di pianificazione Proprietà NextRunTime, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, Proprietà NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742778"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="d59dc-106">Proprietà RegisteredTask. NextRunTime</span><span class="sxs-lookup"><span data-stu-id="d59dc-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="d59dc-107">Per lo scripting, ottiene l'ora in cui l'attività registrata viene pianificata per l'esecuzione successiva.</span><span class="sxs-lookup"><span data-stu-id="d59dc-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="d59dc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d59dc-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="d59dc-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d59dc-109">Property value</span></span>

<span data-ttu-id="d59dc-110">Ora pianificata per l'esecuzione successiva dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="d59dc-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="d59dc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d59dc-111">Remarks</span></span>

<span data-ttu-id="d59dc-112">Se l'attività registrata contiene trigger disabilitati singolarmente, questi trigger avranno comunque effetto sul successivo runtime pianificato che viene restituito anche se sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="d59dc-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d59dc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d59dc-113">Requirements</span></span>



| <span data-ttu-id="d59dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d59dc-114">Requirement</span></span> | <span data-ttu-id="d59dc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d59dc-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d59dc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d59dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d59dc-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d59dc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d59dc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d59dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d59dc-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d59dc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d59dc-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d59dc-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d59dc-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d59dc-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d59dc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d59dc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d59dc-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d59dc-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d59dc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d59dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d59dc-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d59dc-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d59dc-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="d59dc-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





