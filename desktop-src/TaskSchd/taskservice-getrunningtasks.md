---
title: TaskService. GetRunningTasks, metodo
description: Per gli script, ottiene una raccolta di attività in esecuzione.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Utilità di pianificazione del metodo GetRunningTasks
- Metodo GetRunningTasks Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743738"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="98660-106">TaskService. GetRunningTasks, metodo</span><span class="sxs-lookup"><span data-stu-id="98660-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="98660-107">Per gli script, ottiene una raccolta di attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="98660-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="98660-108">**TaskService. GetRunningTasks** restituirà solo una raccolta di attività in esecuzione che sono in esecuzione in o al di sotto del contesto di sicurezza di un utente.</span><span class="sxs-lookup"><span data-stu-id="98660-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="98660-109">Per i membri del gruppo Administrators, ad esempio, **GetRunningTasks** restituirà una raccolta di tutte le attività in esecuzione, ma per i membri del gruppo Users, **GetRunningTasks** restituirà solo una raccolta di attività in esecuzione nel contesto di sicurezza del gruppo Users.</span><span class="sxs-lookup"><span data-stu-id="98660-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="98660-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98660-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="98660-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="98660-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98660-112">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98660-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98660-113">Passare 1 per restituire tutte le attività in esecuzione, incluse le attività nascoste.</span><span class="sxs-lookup"><span data-stu-id="98660-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="98660-114">Passare 0 per restituire una raccolta di attività in esecuzione che non sono attività nascoste.</span><span class="sxs-lookup"><span data-stu-id="98660-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98660-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98660-115">Return value</span></span>

<span data-ttu-id="98660-116">Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene le attività attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="98660-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="98660-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98660-117">Requirements</span></span>



| <span data-ttu-id="98660-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="98660-118">Requirement</span></span> | <span data-ttu-id="98660-119">Valore</span><span class="sxs-lookup"><span data-stu-id="98660-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98660-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98660-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98660-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98660-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="98660-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98660-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98660-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98660-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98660-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="98660-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="98660-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98660-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98660-126">DLL</span><span class="sxs-lookup"><span data-stu-id="98660-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98660-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98660-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98660-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98660-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98660-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="98660-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





