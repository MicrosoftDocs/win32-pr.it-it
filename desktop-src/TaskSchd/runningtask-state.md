---
title: Proprietà RunningTask. state
description: Per gli script, ottiene un identificatore per lo stato dell'attività in esecuzione.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Utilità di pianificazione proprietà stato
- Utilità di pianificazione proprietà state, oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione, proprietà state
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740855"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="c4798-106">Proprietà RunningTask. state</span><span class="sxs-lookup"><span data-stu-id="c4798-106">RunningTask.State property</span></span>

<span data-ttu-id="c4798-107">Per gli script, ottiene un identificatore per lo stato dell'attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c4798-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="c4798-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c4798-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4798-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4798-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="c4798-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c4798-110">Property value</span></span>

<span data-ttu-id="c4798-111">Identificatore per lo stato dell'attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c4798-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="c4798-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c4798-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="c4798-113">Significato</span><span class="sxs-lookup"><span data-stu-id="c4798-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="c4798-114"><dt>**Attività \_ STATO \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="c4798-115">Lo stato dell'attività è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c4798-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="c4798-116"><dt>**Attività \_ STATO \_ disabilitato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c4798-117">L'attività è registrata ma è disabilitata e nessuna istanza dell'attività viene accodata o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c4798-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="c4798-118">L'attività non può essere eseguita fino a quando non viene abilitata.</span><span class="sxs-lookup"><span data-stu-id="c4798-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="c4798-119"><dt>**Attività \_ STATO in \_ coda**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="c4798-120">Le istanze dell'attività vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="c4798-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="c4798-121"><dt>**Attività \_ STATO \_ pronto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="c4798-122">L'attività è pronta per essere eseguita, ma nessuna istanza è in coda o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c4798-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="c4798-123"><dt>**Attività \_ STATO \_ che esegue**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="c4798-124">Una o più istanze dell'attività sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c4798-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="c4798-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4798-125">Remarks</span></span>

<span data-ttu-id="c4798-126">Il metodo [**RunningTask. Refresh**](runningtask-refresh.md) viene chiamato prima che venga restituito il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4798-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4798-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4798-127">Requirements</span></span>



| <span data-ttu-id="c4798-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4798-128">Requirement</span></span> | <span data-ttu-id="c4798-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c4798-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4798-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4798-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4798-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4798-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c4798-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4798-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4798-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4798-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4798-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4798-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4798-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4798-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c4798-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4798-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4798-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





