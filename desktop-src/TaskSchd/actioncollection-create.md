---
title: Metodo ActionCollection. Create
description: Per lo scripting, crea e aggiunge una nuova azione alla raccolta.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Utilità di pianificazione Crea metodo
- Metodo Create Utilità di pianificazione, oggetto ActionCollection
- Oggetto ActionCollection Utilità di pianificazione, metodo create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518232"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="4f25f-106">Metodo ActionCollection. Create</span><span class="sxs-lookup"><span data-stu-id="4f25f-106">ActionCollection.Create method</span></span>

<span data-ttu-id="4f25f-107">Per lo scripting, crea e aggiunge una nuova azione alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4f25f-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f25f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f25f-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="4f25f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f25f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f25f-110">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4f25f-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f25f-111">Questo parametro è impostato su una delle seguenti costanti di enumerazione del [**\_ \_ tipo di azione attività**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="4f25f-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="4f25f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4f25f-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4f25f-113">Significato</span><span class="sxs-lookup"><span data-stu-id="4f25f-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="4f25f-114"><dt>**Attività \_ AZIONE \_ Exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="4f25f-115">L'azione esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4f25f-115">The action performs a command-line operation.</span></span> <span data-ttu-id="4f25f-116">Ad esempio, l'azione può eseguire uno script, avviare un eseguibile o, se il nome di un documento viene fornito, trovare l'applicazione associata e avviare l'applicazione con il documento.</span><span class="sxs-lookup"><span data-stu-id="4f25f-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="4f25f-117"><dt>**Attività \_ \_ \_ Gestore com azione**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="4f25f-118">L'azione genera un gestore.</span><span class="sxs-lookup"><span data-stu-id="4f25f-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="4f25f-119"><dt>**Attività \_ AZIONE \_ inviare un \_ messaggio di posta elettronica**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="4f25f-120">Questa azione Invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4f25f-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="4f25f-121"><dt>**Attività \_ AZIONE \_ Mostra \_ messaggio**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="4f25f-122">Questa azione Visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4f25f-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f25f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f25f-123">Return value</span></span>

<span data-ttu-id="4f25f-124">Oggetto [**azione**](action.md) che rappresenta la nuova azione.</span><span class="sxs-lookup"><span data-stu-id="4f25f-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f25f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f25f-125">Remarks</span></span>

<span data-ttu-id="4f25f-126">Non è possibile aggiungere più di 32 azioni alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4f25f-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f25f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f25f-127">Requirements</span></span>



| <span data-ttu-id="4f25f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f25f-128">Requirement</span></span> | <span data-ttu-id="4f25f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4f25f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f25f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f25f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4f25f-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f25f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4f25f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f25f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4f25f-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f25f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f25f-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4f25f-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f25f-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f25f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f25f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f25f-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f25f-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f25f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f25f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f25f-139">**\_tipo di azione attività \_**</span><span class="sxs-lookup"><span data-stu-id="4f25f-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="4f25f-140">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4f25f-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4f25f-141">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="4f25f-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="4f25f-142">**Azione**</span><span class="sxs-lookup"><span data-stu-id="4f25f-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="4f25f-143">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="4f25f-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="4f25f-144">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="4f25f-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="4f25f-145">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="4f25f-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="4f25f-146">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="4f25f-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





