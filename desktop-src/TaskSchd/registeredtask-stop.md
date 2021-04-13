---
title: Metodo RegisteredTask. Stop
description: Per lo scripting, arresta immediatamente l'attività registrata.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Metodo Stop Utilità di pianificazione
- Metodo Stop Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400888"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="e2f35-106">Metodo RegisteredTask. Stop</span><span class="sxs-lookup"><span data-stu-id="e2f35-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="e2f35-107">Per lo scripting, arresta immediatamente l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="e2f35-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f35-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2f35-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="e2f35-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2f35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f35-110">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f35-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f35-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="e2f35-111">Reserved.</span></span> <span data-ttu-id="e2f35-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e2f35-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f35-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2f35-113">Return value</span></span>

<span data-ttu-id="e2f35-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e2f35-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f35-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2f35-115">Remarks</span></span>

<span data-ttu-id="e2f35-116">La funzione **RegisteredTask. Stop** arresta tutte le istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e2f35-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="e2f35-117">Gli utenti dell'account di sistema possono arrestare un'attività, gli utenti con privilegi di gruppo amministratori possono arrestare un'attività e se un utente dispone dei diritti per eseguire e leggere un'attività, l'utente può arrestare l'attività.</span><span class="sxs-lookup"><span data-stu-id="e2f35-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="e2f35-118">Un utente può arrestare le istanze dell'attività in esecuzione con le stesse credenziali dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e2f35-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="e2f35-119">In tutti gli altri casi, all'utente viene negato l'accesso per arrestare l'attività.</span><span class="sxs-lookup"><span data-stu-id="e2f35-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2f35-120">Requirements</span></span>



| <span data-ttu-id="e2f35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f35-121">Requirement</span></span> | <span data-ttu-id="e2f35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e2f35-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f35-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2f35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f35-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2f35-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2f35-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2f35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f35-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2f35-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2f35-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e2f35-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2f35-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2f35-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2f35-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f35-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f35-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f35-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f35-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2f35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f35-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="e2f35-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





