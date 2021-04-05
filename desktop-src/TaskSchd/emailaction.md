---
title: Oggetto EmailAction
description: Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Utilità di pianificazione oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874385"
---
# <a name="emailaction-object"></a><span data-ttu-id="b3dc3-105">Oggetto EmailAction</span><span class="sxs-lookup"><span data-stu-id="b3dc3-105">EmailAction object</span></span>

<span data-ttu-id="b3dc3-106">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-106">\[This object is no longer supported.</span></span> <span data-ttu-id="b3dc3-107">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="b3dc3-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="b3dc3-108">Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="b3dc3-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b3dc3-109">Members</span></span>

<span data-ttu-id="b3dc3-110">L'oggetto **EmailAction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3dc3-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b3dc3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3dc3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3dc3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3dc3-112">Properties</span></span>

<span data-ttu-id="b3dc3-113">L'oggetto **EmailAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="b3dc3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3dc3-114">Property</span></span>                                                    | <span data-ttu-id="b3dc3-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b3dc3-115">Access type</span></span>           | <span data-ttu-id="b3dc3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3dc3-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3dc3-117">**Allegati**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="b3dc3-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-118">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-119">Ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="b3dc3-120">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="b3dc3-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-121">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-122">Ottiene o imposta l'indirizzo o gli indirizzi di posta elettronica che si desidera includere nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="b3dc3-123">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="b3dc3-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-124">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-125">Ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="b3dc3-126">**CC**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="b3dc3-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-127">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-128">Ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi da inserire in CC nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="b3dc3-129">**Da**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="b3dc3-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-130">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-131">Ottiene o imposta l'indirizzo di posta elettronica da cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="b3dc3-132">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="b3dc3-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-133">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-134">Ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si desidera inviare.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="b3dc3-135">**ID**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="b3dc3-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-136">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-137">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b3dc3-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b3dc3-138">Ottiene o imposta l'identificatore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="b3dc3-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="b3dc3-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-140">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-141">Ottiene o imposta l'indirizzo di posta elettronica a cui si desidera rispondere.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="b3dc3-142">**Server**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="b3dc3-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-143">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-144">Ottiene o imposta il nome del server da utilizzare per l'invio di messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="b3dc3-145">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="b3dc3-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-146">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-147">Ottiene o imposta l'oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="b3dc3-148">**A**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="b3dc3-149">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-149">Read/write</span></span><br/> | <span data-ttu-id="b3dc3-150">Ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi a cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="b3dc3-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="b3dc3-152">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3dc3-152">Read-only</span></span><br/>  | <span data-ttu-id="b3dc3-153">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b3dc3-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="b3dc3-154">Ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="b3dc3-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3dc3-155">Remarks</span></span>

<span data-ttu-id="b3dc3-156">L'azione di posta elettronica deve avere un valore valido per le proprietà [**Server**](emailaction-server.md), [**da**](emailaction-from.md)e [**a**](emailaction-to.md) o [**CC**](emailaction-cc.md) per la registrazione e l'esecuzione corretta dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="b3dc3-157">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata un'azione di posta elettronica utilizzando l'elemento [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b3dc3-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3dc3-158">Examples</span></span>

<span data-ttu-id="b3dc3-159">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di evento (scripting)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3dc3-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dc3-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3dc3-160">Requirements</span></span>



| <span data-ttu-id="b3dc3-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3dc3-161">Requirement</span></span> | <span data-ttu-id="b3dc3-162">Valore</span><span class="sxs-lookup"><span data-stu-id="b3dc3-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dc3-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3dc3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b3dc3-164">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3dc3-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3dc3-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3dc3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b3dc3-166">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3dc3-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3dc3-167">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b3dc3-167">End of client support</span></span><br/>    | <span data-ttu-id="b3dc3-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3dc3-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b3dc3-169">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b3dc3-169">End of server support</span></span><br/>    | <span data-ttu-id="b3dc3-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3dc3-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b3dc3-171">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b3dc3-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3dc3-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc3-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3dc3-173">DLL</span><span class="sxs-lookup"><span data-stu-id="b3dc3-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3dc3-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc3-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

