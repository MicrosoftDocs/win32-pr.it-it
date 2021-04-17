---
title: Proprietà Principal. LogonType
description: Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Utilità di pianificazione proprietà LogonType
- Utilità di pianificazione proprietà LogonType, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477200"
---
# <a name="principallogontype-property"></a><span data-ttu-id="f3be8-106">Proprietà Principal. LogonType</span><span class="sxs-lookup"><span data-stu-id="f3be8-106">Principal.LogonType property</span></span>

<span data-ttu-id="f3be8-107">Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="f3be8-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3be8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3be8-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="f3be8-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3be8-109">Property value</span></span>

<span data-ttu-id="f3be8-110">Impostare su una delle costanti di enumerazione dei [**\_ tipi di accesso alle attività**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3be8-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="f3be8-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f3be8-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="f3be8-112">Significato</span><span class="sxs-lookup"><span data-stu-id="f3be8-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="f3be8-113"><dt>**Attività \_ \_Nessun accesso**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="f3be8-114">Metodo di accesso non specificato.</span><span class="sxs-lookup"><span data-stu-id="f3be8-114">The logon method is not specified.</span></span> <span data-ttu-id="f3be8-115">Utilizzato per le credenziali non NT.</span><span class="sxs-lookup"><span data-stu-id="f3be8-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="f3be8-116"><dt>**Attività \_ \_Password di accesso**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="f3be8-117">Usare una password per la registrazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f3be8-117">Use a password for logging on the user.</span></span> <span data-ttu-id="f3be8-118">La password deve essere fornita in fase di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f3be8-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="f3be8-119"><dt>**Attività \_ \_S4U di accesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="f3be8-120">Usare un token interattivo esistente per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="f3be8-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="f3be8-121">L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U).</span><span class="sxs-lookup"><span data-stu-id="f3be8-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="f3be8-122">Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.</span><span class="sxs-lookup"><span data-stu-id="f3be8-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="f3be8-123"><dt>**Attività \_ \_ \_ Token interattivo di accesso**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="f3be8-124">L'utente deve essere già connesso.</span><span class="sxs-lookup"><span data-stu-id="f3be8-124">User must already be logged on.</span></span> <span data-ttu-id="f3be8-125">L'attività verrà eseguita solo in una sessione interattiva esistente.</span><span class="sxs-lookup"><span data-stu-id="f3be8-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="f3be8-126"><dt>**Attività \_ \_Gruppo di accesso**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="f3be8-127">Attivazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3be8-127">Group activation.</span></span> <span data-ttu-id="f3be8-128">Il campo userId specifica il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3be8-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="f3be8-129"><dt>**Attività \_ \_ \_ Account del servizio di accesso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="f3be8-130">Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="f3be8-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="f3be8-131"><dt>**Attività \_ \_Token interattivo di accesso \_ \_ o \_ password**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="f3be8-132">Usare prima il token interattivo.</span><span class="sxs-lookup"><span data-stu-id="f3be8-132">First use the interactive token.</span></span> <span data-ttu-id="f3be8-133">Se l'utente non è connesso (non è disponibile alcun token interattivo), viene utilizzata la password.</span><span class="sxs-lookup"><span data-stu-id="f3be8-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="f3be8-134">Quando un'attività è registrata, è necessario specificare la password.</span><span class="sxs-lookup"><span data-stu-id="f3be8-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="f3be8-135">Questo flag non è consigliato per le nuove attività perché è meno affidabile rispetto alla \_ password di accesso dell'attività \_ .</span><span class="sxs-lookup"><span data-stu-id="f3be8-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3be8-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3be8-136">Remarks</span></span>

<span data-ttu-id="f3be8-137">Questa proprietà è valida solo quando un identificatore utente viene specificato dalla proprietà [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="f3be8-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="f3be8-138">Durante la lettura o la scrittura di codice XML per un'attività, il tipo di accesso viene specificato nell' [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f3be8-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="f3be8-139">Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="f3be8-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="f3be8-140">Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà **LogonType** dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="f3be8-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3be8-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3be8-141">Requirements</span></span>



| <span data-ttu-id="f3be8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3be8-142">Requirement</span></span> | <span data-ttu-id="f3be8-143">Valore</span><span class="sxs-lookup"><span data-stu-id="f3be8-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3be8-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3be8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f3be8-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3be8-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3be8-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3be8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f3be8-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3be8-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3be8-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f3be8-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3be8-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f3be8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f3be8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3be8-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3be8-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3be8-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3be8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3be8-153">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f3be8-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f3be8-154">**Principale**</span><span class="sxs-lookup"><span data-stu-id="f3be8-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





