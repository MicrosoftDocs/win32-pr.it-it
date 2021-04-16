---
title: Proprietà Action. Type
description: Per lo scripting, ottiene il tipo dell'azione.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Utilità di pianificazione proprietà di tipo
- Utilità di pianificazione proprietà tipo, oggetto azione
- Oggetto Action Utilità di pianificazione, proprietà Type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477812"
---
# <a name="actiontype-property"></a><span data-ttu-id="78a17-106">Proprietà Action. Type</span><span class="sxs-lookup"><span data-stu-id="78a17-106">Action.Type property</span></span>

<span data-ttu-id="78a17-107">Per lo scripting, ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="78a17-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a17-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78a17-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="78a17-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78a17-109">Property value</span></span>

<span data-ttu-id="78a17-110">Questa proprietà restituisce una delle seguenti costanti di enumerazione del [**\_ \_ tipo di azione dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .</span><span class="sxs-lookup"><span data-stu-id="78a17-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="78a17-111">Valore</span><span class="sxs-lookup"><span data-stu-id="78a17-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="78a17-112">Significato</span><span class="sxs-lookup"><span data-stu-id="78a17-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="78a17-113"><dt>**Attività \_ AZIONE \_ Exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="78a17-114">Questa azione esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="78a17-114">This action performs a command-line operation.</span></span> <span data-ttu-id="78a17-115">Ad esempio, l'azione può eseguire uno script, avviare un eseguibile o, se il nome di un documento viene fornito, trovare l'applicazione associata e avviare l'applicazione con il documento.</span><span class="sxs-lookup"><span data-stu-id="78a17-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="78a17-116"><dt>**Attività \_ \_ \_ Gestore com azione**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="78a17-117">Questa azione attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="78a17-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="78a17-118"><dt>**Attività \_ AZIONE \_ inviare un \_ messaggio di posta elettronica**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="78a17-119">Questa azione Invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="78a17-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="78a17-120"><dt>**Attività \_ AZIONE \_ Mostra \_ messaggio**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="78a17-121">Questa azione Visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="78a17-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="78a17-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="78a17-122">Remarks</span></span>

<span data-ttu-id="78a17-123">Il tipo di azione viene definito quando viene creata l'azione e non può essere modificato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="78a17-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="78a17-124">Per informazioni sulla creazione di un'azione, vedere [**ActionCollection. Create**](actioncollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="78a17-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="78a17-125">Per informazioni sul funzionamento combinato di azioni e attività, vedere [azioni attività](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="78a17-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78a17-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78a17-126">Requirements</span></span>



| <span data-ttu-id="78a17-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a17-127">Requirement</span></span> | <span data-ttu-id="78a17-128">Valore</span><span class="sxs-lookup"><span data-stu-id="78a17-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78a17-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a17-129">Minimum supported client</span></span><br/> | <span data-ttu-id="78a17-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78a17-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="78a17-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a17-131">Minimum supported server</span></span><br/> | <span data-ttu-id="78a17-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78a17-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78a17-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="78a17-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="78a17-134"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="78a17-135">DLL</span><span class="sxs-lookup"><span data-stu-id="78a17-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78a17-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78a17-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a17-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78a17-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a17-138">**\_tipo di azione attività \_**</span><span class="sxs-lookup"><span data-stu-id="78a17-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="78a17-139">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="78a17-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="78a17-140">**Azione**</span><span class="sxs-lookup"><span data-stu-id="78a17-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





