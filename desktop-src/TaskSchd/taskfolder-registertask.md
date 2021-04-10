---
title: TaskFolder. l'RegisterTask, metodo
description: Per la creazione di script, registra (Crea) una nuova attività nella cartella usando XML per definire l'attività.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- Utilità di pianificazione del metodo l'RegisterTask
- Metodo l'RegisterTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo l'RegisterTask
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964677"
---
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="ba19f-106">TaskFolder. l'RegisterTask, metodo</span><span class="sxs-lookup"><span data-stu-id="ba19f-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="ba19f-107">Per la creazione di script, registra (Crea) una nuova attività nella cartella usando XML per definire l'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba19f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba19f-108">Syntax</span></span>


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a><span data-ttu-id="ba19f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba19f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba19f-110">*percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-111">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-111">The name of the task.</span></span> <span data-ttu-id="ba19f-112">Se questo valore è **Nothing**, l'attività verrà registrata nella cartella radice dell'attività e il nome dell'attività sarà un valore GUID creato dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ba19f-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="ba19f-113">Un nome di attività non può iniziare o terminare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="ba19f-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="ba19f-114">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="ba19f-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="ba19f-115">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="ba19f-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="ba19f-116">*XmlText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-117">Descrizione dell'attività in formato XML.</span><span class="sxs-lookup"><span data-stu-id="ba19f-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="ba19f-118">Negli argomenti seguenti sono contenute attività definite utilizzando XML.</span><span class="sxs-lookup"><span data-stu-id="ba19f-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="ba19f-119">Esempio di trigger time (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="ba19f-120">[Esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba19f-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="ba19f-121">Esempio di trigger giornaliero (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="ba19f-122">Esempio di trigger di registrazione (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="ba19f-123">Esempio di trigger settimanale (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="ba19f-124">Esempio di trigger LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="ba19f-125">Esempio di trigger di avvio (XML)</span><span class="sxs-lookup"><span data-stu-id="ba19f-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="ba19f-126">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-127">Costante [**di \_ creazione**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) di un'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="ba19f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ba19f-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="ba19f-129">Significato</span><span class="sxs-lookup"><span data-stu-id="ba19f-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="ba19f-130"><dt>**Attività \_ CONVALIDA \_ solo**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="ba19f-131">Il Utilità di pianificazione controlla la sintassi del codice XML che descrive l'attività ma non registra l'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="ba19f-132">Questa costante non può essere combinata con i valori di **\_ creazione**, **\_ aggiornamento** attività **o \_ creazione \_ o \_ aggiornamento** dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="ba19f-133"><dt>**Attività \_ Crea**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="ba19f-134">Il Utilità di pianificazione registra l'attività come nuova attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="ba19f-135"><dt>**Attività \_ AGGIORNARE**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="ba19f-136">Il Utilità di pianificazione registra l'attività come versione aggiornata di un'attività esistente.</span><span class="sxs-lookup"><span data-stu-id="ba19f-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="ba19f-137">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ba19f-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="ba19f-138"><dt>**Attività \_ Crea \_ o \_ Aggiorna**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="ba19f-139">Il Utilità di pianificazione registra l'attività come nuova attività o come versione aggiornata se l'attività esiste già.</span><span class="sxs-lookup"><span data-stu-id="ba19f-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="ba19f-140">Equivale a attività di creazione attività di \_ \| \_ aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ba19f-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="ba19f-141"><dt>**Attività \_ DISABILITARE**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="ba19f-142">Il Utilità di pianificazione Disabilita l'attività esistente.</span><span class="sxs-lookup"><span data-stu-id="ba19f-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="ba19f-143"><dt>**Attività \_ Non \_ aggiungere \_ 0x10 \_ ACE principale**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="ba19f-144">Al Utilità di pianificazione viene impedito di aggiungere la voce di controllo di accesso (ACE) Consenti per l'entità di contesto.</span><span class="sxs-lookup"><span data-stu-id="ba19f-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="ba19f-145">Quando viene chiamata la funzione **TaskFolder. l'RegisterTask** con questo flag per aggiornare un'attività, il servizio Utilità di pianificazione non aggiunge la voce ACE per la nuova entità di contesto e non rimuove la voce ACE dall'entità di contesto precedente.</span><span class="sxs-lookup"><span data-stu-id="ba19f-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="ba19f-146"><dt>**Attività \_ IGNORARE \_ i \_ trigger di registrazione**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="ba19f-147">Il Utilità di pianificazione crea l'attività, ma ignora i trigger di registrazione nell'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="ba19f-148">Ignorando i trigger di registrazione, l'attività non verrà eseguita quando viene registrata, a meno che un trigger basato sul tempo non ne provochi l'esecuzione alla registrazione.</span><span class="sxs-lookup"><span data-stu-id="ba19f-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="ba19f-149">*ID utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-150">Le credenziali utente utilizzate per registrare l'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="ba19f-151">Se l'attività è definita come un'attività Utilità di pianificazione 1,0, non usare il nome di un gruppo (anziché un nome utente specifico) in questo parametro userId.</span><span class="sxs-lookup"><span data-stu-id="ba19f-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="ba19f-152">Un'attività viene definita come un'attività Utilità di pianificazione 1,0 quando l'attributo Version dell'elemento Task nel codice XML dell'attività è impostato su 1,1.</span><span class="sxs-lookup"><span data-stu-id="ba19f-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="ba19f-153">*password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-154">Password per l'ID utente usato per registrare l'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="ba19f-155">Quando \_ viene usato il tipo di accesso dell'account del servizio di accesso all'attività \_ \_ , la password deve essere un valore **Variant** vuoto, ad esempio **VT \_ null** o **VT \_ vuoto**.</span><span class="sxs-lookup"><span data-stu-id="ba19f-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="ba19f-156">*LogonType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-157">Definisce quale tecnica di accesso viene utilizzata per eseguire l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="ba19f-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="ba19f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="ba19f-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ba19f-159">Significato</span><span class="sxs-lookup"><span data-stu-id="ba19f-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="ba19f-160"><dt>**Attività \_ \_Nessun accesso**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="ba19f-161">Metodo di accesso non specificato.</span><span class="sxs-lookup"><span data-stu-id="ba19f-161">The logon method is not specified.</span></span> <span data-ttu-id="ba19f-162">Utilizzato per le credenziali non NT.</span><span class="sxs-lookup"><span data-stu-id="ba19f-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="ba19f-163"><dt>**Attività \_ \_Password di accesso**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="ba19f-164">Usare una password per la registrazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ba19f-164">Use a password for logging on the user.</span></span> <span data-ttu-id="ba19f-165">La password deve essere fornita in fase di registrazione.</span><span class="sxs-lookup"><span data-stu-id="ba19f-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="ba19f-166"><dt>**Attività \_ \_S4U di accesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="ba19f-167">Usare un token interattivo esistente per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="ba19f-168">L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U).</span><span class="sxs-lookup"><span data-stu-id="ba19f-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="ba19f-169">Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.</span><span class="sxs-lookup"><span data-stu-id="ba19f-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="ba19f-170"><dt>**Attività \_ \_ \_ Token interattivo di accesso**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="ba19f-171">L'utente deve essere già connesso.</span><span class="sxs-lookup"><span data-stu-id="ba19f-171">User must already be logged on.</span></span> <span data-ttu-id="ba19f-172">L'attività verrà eseguita solo in una sessione interattiva esistente.</span><span class="sxs-lookup"><span data-stu-id="ba19f-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="ba19f-173"><dt>**Attività \_ \_Gruppo di accesso**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="ba19f-174">Attivazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ba19f-174">Group activation.</span></span> <span data-ttu-id="ba19f-175">Il campo **GroupID** specifica il gruppo.</span><span class="sxs-lookup"><span data-stu-id="ba19f-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="ba19f-176"><dt>**Attività \_ \_ \_ Account del servizio di accesso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="ba19f-177">Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="ba19f-178"><dt>**Attività \_ \_Token interattivo di accesso \_ \_ o \_ password**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ba19f-179">Usare prima il token interattivo.</span><span class="sxs-lookup"><span data-stu-id="ba19f-179">First use the interactive token.</span></span> <span data-ttu-id="ba19f-180">Se l'utente non è connesso (non è disponibile alcun token interattivo), viene utilizzata la password.</span><span class="sxs-lookup"><span data-stu-id="ba19f-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="ba19f-181">Quando un'attività è registrata, è necessario specificare la password.</span><span class="sxs-lookup"><span data-stu-id="ba19f-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="ba19f-182">Questo flag non è consigliato per le nuove attività perché è meno affidabile rispetto alla \_ password di accesso dell'attività \_ .</span><span class="sxs-lookup"><span data-stu-id="ba19f-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba19f-183">*SDDL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-184">Descrittore di sicurezza associato all'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="ba19f-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="ba19f-185">È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="ba19f-186">Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="ba19f-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="ba19f-187">*pTask* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19f-188">Oggetto [**RegisteredTask**](registeredtask.md) che rappresenta la nuova attività.</span><span class="sxs-lookup"><span data-stu-id="ba19f-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba19f-189">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba19f-189">Return value</span></span>

<span data-ttu-id="ba19f-190">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ba19f-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba19f-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba19f-191">Remarks</span></span>

<span data-ttu-id="ba19f-192">Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="ba19f-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="ba19f-193">Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività oppure nel parametro *LogonType* di **TaskFolder. l'RegisterTask** o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ba19f-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="ba19f-194">Solo un membro del gruppo Administrators può creare un'attività con un trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="ba19f-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="ba19f-195">È possibile registrare correttamente un'attività con un gruppo specificato nel parametro *userid* e 3 (**\_ \_ \_ token interattivo accesso attività**) specificato nel parametro *LogonType* di **TaskFolder. l'RegisterTask** o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), ma l'attività non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="ba19f-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba19f-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba19f-196">Requirements</span></span>



| <span data-ttu-id="ba19f-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba19f-197">Requirement</span></span> | <span data-ttu-id="ba19f-198">Valore</span><span class="sxs-lookup"><span data-stu-id="ba19f-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba19f-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba19f-199">Minimum supported client</span></span><br/> | <span data-ttu-id="ba19f-200">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ba19f-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba19f-201">Minimum supported server</span></span><br/> | <span data-ttu-id="ba19f-202">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba19f-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba19f-203">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ba19f-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba19f-204"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ba19f-205">DLL</span><span class="sxs-lookup"><span data-stu-id="ba19f-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba19f-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba19f-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba19f-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba19f-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba19f-208">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ba19f-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="ba19f-209">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="ba19f-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="ba19f-210">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="ba19f-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

