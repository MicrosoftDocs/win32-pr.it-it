---
title: Metodo RegisteredTask. GetInstances
description: Per gli script, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Metodo GetInstances Utilità di pianificazione
- Metodo GetInstances Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, Metodo GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120814"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="0545e-106">Metodo RegisteredTask. GetInstances</span><span class="sxs-lookup"><span data-stu-id="0545e-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="0545e-107">Per gli script, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="0545e-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="0545e-108">**RegisteredTask. GetInstances** restituirà solo le istanze dell'attività registrata attualmente in esecuzione che sono in esecuzione nel contesto di sicurezza di un utente o al di sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="0545e-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="0545e-109">Per i membri del gruppo **Administrators, ad** esempio **, vengono** restituite tutte le istanze dell'attività registrata attualmente in esecuzione, ma per i membri del gruppo Users verranno restituite solo le istanze dell'attività registrata attualmente in esecuzione nel contesto di sicurezza del gruppo Users.</span><span class="sxs-lookup"><span data-stu-id="0545e-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0545e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0545e-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="0545e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0545e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0545e-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="0545e-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="0545e-113">Questo parametro è riservato per utilizzi futuri e deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="0545e-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0545e-114">*runningTasks* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0545e-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0545e-115">Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene tutte le istanze attualmente in esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0545e-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0545e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0545e-116">Return value</span></span>

<span data-ttu-id="0545e-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0545e-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0545e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0545e-118">Requirements</span></span>



| <span data-ttu-id="0545e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0545e-119">Requirement</span></span> | <span data-ttu-id="0545e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0545e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0545e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0545e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0545e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0545e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0545e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0545e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0545e-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0545e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0545e-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0545e-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="0545e-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0545e-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0545e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0545e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0545e-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0545e-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0545e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0545e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0545e-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0545e-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0545e-131">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="0545e-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





