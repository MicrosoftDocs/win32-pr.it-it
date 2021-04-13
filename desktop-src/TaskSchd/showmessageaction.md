---
title: Oggetto ShowMessageAction
description: Per gli script, rappresenta un'azione che visualizza una finestra di messaggio quando un'attività viene attivata.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Utilità di pianificazione oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400410"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="2c87d-105">Oggetto ShowMessageAction</span><span class="sxs-lookup"><span data-stu-id="2c87d-105">ShowMessageAction object</span></span>

<span data-ttu-id="2c87d-106">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="2c87d-106">\[This object is no longer supported.</span></span> <span data-ttu-id="2c87d-107">È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]</span><span class="sxs-lookup"><span data-stu-id="2c87d-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="2c87d-108">Per gli script, rappresenta un'azione che visualizza una finestra di messaggio quando un'attività viene attivata.</span><span class="sxs-lookup"><span data-stu-id="2c87d-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="2c87d-109">Membri</span><span class="sxs-lookup"><span data-stu-id="2c87d-109">Members</span></span>

<span data-ttu-id="2c87d-110">L'oggetto **ShowMessageAction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2c87d-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="2c87d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c87d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c87d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c87d-112">Properties</span></span>

<span data-ttu-id="2c87d-113">L'oggetto **ShowMessageAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c87d-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="2c87d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c87d-114">Property</span></span>                                                        | <span data-ttu-id="2c87d-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2c87d-115">Access type</span></span>           | <span data-ttu-id="2c87d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c87d-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c87d-117">**ID**</span><span class="sxs-lookup"><span data-stu-id="2c87d-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="2c87d-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2c87d-118">Read/write</span></span><br/> | <span data-ttu-id="2c87d-119">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="2c87d-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="2c87d-120">Ottiene o imposta l'identificatore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2c87d-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="2c87d-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="2c87d-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="2c87d-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2c87d-122">Read/write</span></span><br/> | <span data-ttu-id="2c87d-123">Ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2c87d-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="2c87d-124">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="2c87d-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="2c87d-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2c87d-125">Read/write</span></span><br/> | <span data-ttu-id="2c87d-126">Ottiene o imposta il titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2c87d-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="2c87d-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2c87d-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="2c87d-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c87d-128">Read-only</span></span><br/>  | <span data-ttu-id="2c87d-129">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="2c87d-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="2c87d-130">Ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2c87d-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="2c87d-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c87d-131">Remarks</span></span>

<span data-ttu-id="2c87d-132">Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="2c87d-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="2c87d-133">Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="2c87d-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="2c87d-134">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, un'azione della finestra di messaggio viene specificata utilizzando l'elemento [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="2c87d-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="2c87d-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c87d-135">Examples</span></span>

<span data-ttu-id="2c87d-136">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di finestra di messaggio (scripting)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2c87d-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c87d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c87d-137">Requirements</span></span>



| <span data-ttu-id="2c87d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c87d-138">Requirement</span></span> | <span data-ttu-id="2c87d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2c87d-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c87d-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c87d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2c87d-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c87d-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2c87d-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c87d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2c87d-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c87d-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c87d-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2c87d-144">End of client support</span></span><br/>    | <span data-ttu-id="2c87d-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c87d-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="2c87d-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2c87d-146">End of server support</span></span><br/>    | <span data-ttu-id="2c87d-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c87d-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2c87d-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c87d-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c87d-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c87d-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c87d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2c87d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c87d-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c87d-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

