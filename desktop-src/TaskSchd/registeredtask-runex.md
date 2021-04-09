---
title: RegisteredTask. RunEx, metodo
description: Per gli script, esegue l'attività registrata immediatamente usando i flag specificati e un identificatore di sessione.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Utilità di pianificazione del metodo RunEx
- Metodo RunEx Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120426"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="2f2ae-106">RegisteredTask. RunEx, metodo</span><span class="sxs-lookup"><span data-stu-id="2f2ae-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="2f2ae-107">Per gli script, esegue l'attività registrata immediatamente usando i flag specificati e un identificatore di sessione.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f2ae-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="2f2ae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f2ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2ae-110">*parametri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2ae-111">Parametri utilizzati come valori nelle azioni dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="2f2ae-112">Per non specificare i valori dei parametri per le azioni dell'attività, impostare questo parametro su **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="2f2ae-113">In caso contrario, è possibile specificare un solo valore stringa o una matrice di valori stringa.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="2f2ae-114">I valori stringa specificati sono associati a nomi e archiviati come coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="2f2ae-115">Se si specifica un solo valore stringa, Arg0 sarà il nome assegnato al valore.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="2f2ae-116">Il valore può essere utilizzato nell'azione dell'attività in cui la variabile $ (Arg0) viene utilizzata nelle proprietà dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="2f2ae-117">Se si passano valori quali "0", "100" e "250" come matrice di valori stringa, "0" sostituirà le variabili $ (Arg0), "100" sostituiranno le variabili $ (arg1) e "250" sostituiranno le variabili $ (arg2) utilizzate nelle proprietà dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="2f2ae-118">È possibile specificare un massimo di 32 valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="2f2ae-119">Per ulteriori informazioni e per un elenco delle proprietà dell'azione che possono usare variabili $ (Arg0), $ (arg1),..., $ (Arg32) nei rispettivi valori, vedere [azioni attività](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2f2ae-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2ae-120">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2ae-121">Costante [dei \_ \_ flag di esecuzione](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) di un'attività che definisce la modalità di esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="2f2ae-122">*ID sessione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2ae-123">Sessione di Terminal Server in cui si desidera avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="2f2ae-124">Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID di sessione (0x4) non viene passata nel parametro *Flags* , il valore specificato in questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="2f2ae-125">Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è minore o uguale a 0, verrà restituito un errore di argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="2f2ae-126">Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è un ID di sessione valido maggiore di 0 e se non viene specificato alcun valore per il parametro *User* , il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo quando l'utente è connesso alla sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="2f2ae-127">Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è un ID di sessione valido maggiore di 0 e se un utente viene specificato nel parametro *User* , il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo come l'utente specificato nel parametro *User* .</span><span class="sxs-lookup"><span data-stu-id="2f2ae-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2f2ae-128">*runningTask* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2ae-129">Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2ae-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f2ae-130">Return value</span></span>

<span data-ttu-id="2f2ae-131">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2ae-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f2ae-132">Remarks</span></span>

<span data-ttu-id="2f2ae-133">Questo metodo restituirà senza errori, ma l'attività non verrà eseguita se la proprietà [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) è impostata su false per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="2f2ae-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2ae-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2ae-134">Requirements</span></span>



| <span data-ttu-id="2f2ae-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2ae-135">Requirement</span></span> | <span data-ttu-id="2f2ae-136">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2ae-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2ae-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2ae-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2ae-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f2ae-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2ae-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2ae-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f2ae-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f2ae-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2f2ae-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f2ae-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ae-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f2ae-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2ae-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2ae-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2ae-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2ae-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f2ae-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2ae-146">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2f2ae-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="2f2ae-147">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="2f2ae-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





