---
title: Metodo RegisteredTask. Run
description: Per lo scripting, esegue immediatamente l'attività registrata.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Metodo Run Utilità di pianificazione
- Metodo Run Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302229"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="bd58a-106">Metodo RegisteredTask. Run</span><span class="sxs-lookup"><span data-stu-id="bd58a-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="bd58a-107">Per lo scripting, esegue immediatamente l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="bd58a-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd58a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd58a-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="bd58a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd58a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd58a-110">*parametri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd58a-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd58a-111">Parametri utilizzati come valori nelle azioni dell'attività.</span><span class="sxs-lookup"><span data-stu-id="bd58a-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="bd58a-112">Per non specificare i valori dei parametri per le azioni dell'attività, impostare questo parametro su **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="bd58a-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="bd58a-113">In caso contrario, è possibile specificare un solo valore stringa o una matrice di valori stringa.</span><span class="sxs-lookup"><span data-stu-id="bd58a-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="bd58a-114">I valori stringa specificati sono associati a nomi e archiviati come coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="bd58a-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="bd58a-115">Se si specifica un solo valore stringa, Arg0 sarà il nome assegnato al valore.</span><span class="sxs-lookup"><span data-stu-id="bd58a-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="bd58a-116">Il valore può essere utilizzato nell'azione dell'attività in cui la variabile $ (Arg0) viene utilizzata nelle proprietà dell'azione.</span><span class="sxs-lookup"><span data-stu-id="bd58a-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="bd58a-117">Se si passano valori quali "0", "100" e "250" come matrice di valori stringa, "0" sostituirà le variabili $ (Arg0), "100" sostituiranno le variabili $ (arg1) e "250" sostituiranno le variabili $ (arg2) utilizzate nelle proprietà dell'azione.</span><span class="sxs-lookup"><span data-stu-id="bd58a-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="bd58a-118">È possibile specificare un massimo di 32 valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="bd58a-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="bd58a-119">Per ulteriori informazioni e per un elenco delle proprietà dell'azione che possono usare variabili $ (Arg0), $ (arg1),..., $ (Arg32) nei rispettivi valori, vedere [azioni attività](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bd58a-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd58a-120">*ppRunningTask* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd58a-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd58a-121">Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="bd58a-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd58a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd58a-122">Return value</span></span>

<span data-ttu-id="bd58a-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bd58a-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd58a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd58a-124">Remarks</span></span>

<span data-ttu-id="bd58a-125">La funzione **RegisteredTask. Run** è equivalente alla funzione [**RegisteredTask. RunEx**](registeredtask-runex.md) con il parametro flags uguale a 0 e non è stato specificato alcun valore per il parametro User.</span><span class="sxs-lookup"><span data-stu-id="bd58a-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="bd58a-126">Questo metodo restituirà senza errori, ma l'attività non verrà eseguita se la proprietà [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) è impostata su false per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="bd58a-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd58a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd58a-127">Requirements</span></span>



| <span data-ttu-id="bd58a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd58a-128">Requirement</span></span> | <span data-ttu-id="bd58a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bd58a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd58a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd58a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd58a-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd58a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bd58a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd58a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd58a-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd58a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd58a-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bd58a-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd58a-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd58a-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd58a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bd58a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd58a-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd58a-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd58a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd58a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd58a-139">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bd58a-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bd58a-140">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="bd58a-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





