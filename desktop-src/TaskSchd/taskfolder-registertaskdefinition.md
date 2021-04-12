---
title: TaskFolder. RegisterTaskDefinition, metodo
description: Per lo scripting, registra (Crea) un'attività in una posizione specificata usando l'oggetto TaskDefinition per definire un'attività.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Utilità di pianificazione del metodo RegisterTaskDefinition
- Metodo RegisterTaskDefinition Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo RegisterTaskDefinition
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400753"
---
# <a name="taskfolderregistertaskdefinition-method"></a><span data-ttu-id="3c4ef-106">TaskFolder. RegisterTaskDefinition, metodo</span><span class="sxs-lookup"><span data-stu-id="3c4ef-106">TaskFolder.RegisterTaskDefinition method</span></span>

<span data-ttu-id="3c4ef-107">Per lo scripting, registra (Crea) un'attività in una posizione specificata usando l'oggetto [**TaskDefinition**](taskdefinition.md) per definire un'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-107">For scripting, registers (creates) a task in a specified location using the [**TaskDefinition**](taskdefinition.md) object to define a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c4ef-108">Syntax</span></span>


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a><span data-ttu-id="3c4ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c4ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4ef-110">*percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-111">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-111">The name of the task.</span></span> <span data-ttu-id="3c4ef-112">Se questo valore è **Nothing**, l'attività verrà registrata nella cartella radice dell'attività e il nome dell'attività sarà un valore GUID creato dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="3c4ef-113">Un nome di attività non può iniziare o terminare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="3c4ef-114">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="3c4ef-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="3c4ef-115">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="3c4ef-116">*definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-116">*definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-117">Definizione dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-117">The definition of the task that is registered.</span></span>

</dd> <dt>

<span data-ttu-id="3c4ef-118">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-119">Costante [**di \_ creazione**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) di un'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-119">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="3c4ef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3c4ef-120">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="3c4ef-121">Significato</span><span class="sxs-lookup"><span data-stu-id="3c4ef-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="3c4ef-122"><dt>**Attività \_ CONVALIDA \_ solo**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-122"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="3c4ef-123">Il Utilità di pianificazione controlla la sintassi del codice XML che descrive l'attività ma non registra l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-123">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="3c4ef-124">Questa costante non può essere combinata con i valori di **\_ creazione**, **\_ aggiornamento** attività **o \_ creazione \_ o \_ aggiornamento** dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-124">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="3c4ef-125"><dt>**Attività \_ Crea**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-125"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="3c4ef-126">Il Utilità di pianificazione registra l'attività come nuova attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-126">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="3c4ef-127"><dt>**Attività \_ AGGIORNARE**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-127"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="3c4ef-128">Il Utilità di pianificazione registra l'attività come versione aggiornata di un'attività esistente.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-128">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="3c4ef-129">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-129">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="3c4ef-130"><dt>**Attività \_ Crea \_ o \_ Aggiorna**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-130"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="3c4ef-131">Il Utilità di pianificazione registra l'attività come nuova attività o come versione aggiornata se l'attività esiste già.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-131">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="3c4ef-132">Equivale a attività di creazione attività di \_ \| \_ aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-132">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="3c4ef-133"><dt>**Attività \_ DISABILITARE**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-133"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="3c4ef-134">Il Utilità di pianificazione Disabilita l'attività esistente.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-134">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="3c4ef-135"><dt>**Attività \_ Non \_ aggiungere \_ 0x10 \_ ACE principale**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-135"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="3c4ef-136">Al Utilità di pianificazione viene impedito di aggiungere la voce di controllo di accesso (ACE) Consenti per l'entità di contesto.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-136">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="3c4ef-137">Quando viene chiamata la funzione **TaskFolder. RegisterTaskDefinition** con questo flag per aggiornare un'attività, il servizio Utilità di pianificazione non aggiunge la voce ACE per la nuova entità di contesto e non rimuove la voce ACE dall'entità di contesto precedente.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-137">When the **TaskFolder.RegisterTaskDefinition** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="3c4ef-138"><dt>**Attività \_ IGNORARE \_ i \_ trigger di registrazione**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-138"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="3c4ef-139">Il Utilità di pianificazione crea l'attività, ma ignora i trigger di registrazione nell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-139">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="3c4ef-140">Ignorando i trigger di registrazione, l'attività non verrà eseguita quando viene registrata, a meno che un trigger basato sul tempo non ne provochi l'esecuzione alla registrazione.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-140">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="3c4ef-141">*ID utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-141">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-142">Le credenziali utente utilizzate per registrare l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-142">The user credentials that are used to register the task.</span></span> <span data-ttu-id="3c4ef-143">Se presenti, queste credenziali hanno la priorità sulle credenziali specificate nell'oggetto definizione di attività a cui punta il parametro della *definizione* .</span><span class="sxs-lookup"><span data-stu-id="3c4ef-143">If present, these credentials take priority over the credentials specified in the task definition object pointed to by the *definition* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3c4ef-144">Se l'attività è definita come un'attività Utilità di pianificazione 1,0, non usare il nome di un gruppo (anziché un nome utente specifico) in questo parametro userId.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-144">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="3c4ef-145">Un'attività è definita come un'attività Utilità di pianificazione 1,0 quando la proprietà [**compatibilità**](tasksettings-compatibility.md) è impostata su 1 nelle impostazioni dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-145">A task is defined as a Task Scheduler 1.0 task when the [**Compatibility**](tasksettings-compatibility.md) property is set to 1 in the task's settings.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c4ef-146">*password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-146">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-147">Password per l'ID utente usato per registrare l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-147">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="3c4ef-148">Quando \_ viene usato il tipo di accesso dell'account del servizio di accesso all'attività \_ \_ , la password deve essere un valore **Variant** vuoto, ad esempio **VT \_ null** o **VT \_ vuoto**.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-148">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="3c4ef-149">*LogonType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-149">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-150">Definisce quale tecnica di accesso viene utilizzata per eseguire l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-150">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="3c4ef-151">Valore</span><span class="sxs-lookup"><span data-stu-id="3c4ef-151">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="3c4ef-152">Significato</span><span class="sxs-lookup"><span data-stu-id="3c4ef-152">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="3c4ef-153"><dt>**Attività \_ \_Nessun accesso**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-153"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="3c4ef-154">Metodo di accesso non specificato.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-154">The logon method is not specified.</span></span> <span data-ttu-id="3c4ef-155">Utilizzato per le credenziali non NT.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-155">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="3c4ef-156"><dt>**Attività \_ \_Password di accesso**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-156"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="3c4ef-157">Usare una password per la registrazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-157">Use a password for logging on the user.</span></span> <span data-ttu-id="3c4ef-158">La password deve essere fornita in fase di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-158">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="3c4ef-159"><dt>**Attività \_ \_S4U di accesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-159"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="3c4ef-160">Usare un token interattivo esistente per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-160">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="3c4ef-161">L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U).</span><span class="sxs-lookup"><span data-stu-id="3c4ef-161">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="3c4ef-162">Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-162">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="3c4ef-163"><dt>**Attività \_ \_ \_ Token interattivo di accesso**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-163"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="3c4ef-164">L'utente deve essere già connesso.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-164">User must already be logged on.</span></span> <span data-ttu-id="3c4ef-165">L'attività verrà eseguita solo in una sessione interattiva esistente.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-165">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="3c4ef-166"><dt>**Attività \_ \_Gruppo di accesso**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-166"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="3c4ef-167">Attivazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-167">Group activation.</span></span> <span data-ttu-id="3c4ef-168">Il campo **GroupID** specifica il gruppo.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-168">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="3c4ef-169"><dt>**Attività \_ \_ \_ Account del servizio di accesso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-169"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="3c4ef-170">Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-170">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="3c4ef-171"><dt>**Attività \_ \_Token interattivo di accesso \_ \_ o \_ password**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-171"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="3c4ef-172">Usare prima il token interattivo.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-172">First use the interactive token.</span></span> <span data-ttu-id="3c4ef-173">Se l'utente non è connesso (non è disponibile alcun token interattivo), viene utilizzata la password.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-173">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="3c4ef-174">Quando un'attività è registrata, è necessario specificare la password.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-174">The password must be specified when a task is registered.</span></span> <span data-ttu-id="3c4ef-175">Questo flag non è consigliato per le nuove attività perché è meno affidabile rispetto alla \_ password di accesso dell'attività \_ .</span><span class="sxs-lookup"><span data-stu-id="3c4ef-175">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c4ef-176">*SDDL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-176">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-177">Descrittore di sicurezza associato all'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-177">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="3c4ef-178">È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-178">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="3c4ef-179">Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-179">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c4ef-180">*attività* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-180">*task* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4ef-181">Oggetto [**RegisteredTask**](registeredtask.md) che rappresenta la nuova attività.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-181">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4ef-182">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c4ef-182">Return value</span></span>

<span data-ttu-id="3c4ef-183">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-183">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4ef-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c4ef-184">Remarks</span></span>

<span data-ttu-id="3c4ef-185">Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-185">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="3c4ef-186">Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-186">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**.</span></span>

<span data-ttu-id="3c4ef-187">Solo un membro del gruppo Administrators può creare un'attività con un trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-187">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="3c4ef-188">È possibile registrare correttamente un'attività con un gruppo specificato nel parametro *userid* e 3 (**\_ \_ \_ token interattivo accesso attività**) specificato nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**, ma l'attività non viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="3c4ef-188">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**, but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4ef-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c4ef-189">Requirements</span></span>



| <span data-ttu-id="3c4ef-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c4ef-190">Requirement</span></span> | <span data-ttu-id="3c4ef-191">Valore</span><span class="sxs-lookup"><span data-stu-id="3c4ef-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4ef-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c4ef-192">Minimum supported client</span></span><br/> | <span data-ttu-id="3c4ef-193">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-193">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3c4ef-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c4ef-194">Minimum supported server</span></span><br/> | <span data-ttu-id="3c4ef-195">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c4ef-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c4ef-196">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3c4ef-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c4ef-197"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-197"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c4ef-198">DLL</span><span class="sxs-lookup"><span data-stu-id="3c4ef-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c4ef-199"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c4ef-199"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c4ef-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c4ef-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4ef-201">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3c4ef-201">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3c4ef-202">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="3c4ef-202">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="3c4ef-203">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="3c4ef-203">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

 





