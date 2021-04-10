---
title: Elemento SendEmail (actionGroup)
description: Rappresenta un'azione che invia un messaggio di posta elettronica.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Utilità di pianificazione elemento SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964672"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="3a79c-104">Elemento SendEmail (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="3a79c-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="3a79c-105">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="3a79c-106">L'elemento **SendEmail** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="3a79c-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="3a79c-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3a79c-107">Parent element</span></span>



| <span data-ttu-id="3a79c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3a79c-108">Element</span></span>                                                         | <span data-ttu-id="3a79c-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="3a79c-109">Derived from</span></span>                                                       | <span data-ttu-id="3a79c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a79c-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="3a79c-111">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="3a79c-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="3a79c-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="3a79c-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="3a79c-113">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="3a79c-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3a79c-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3a79c-114">Child elements</span></span>



| <span data-ttu-id="3a79c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="3a79c-115">Element</span></span>                                                                        | <span data-ttu-id="3a79c-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a79c-116">Type</span></span>                                                                         | <span data-ttu-id="3a79c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a79c-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a79c-118">**Allegati**</span><span class="sxs-lookup"><span data-stu-id="3a79c-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="3a79c-119">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="3a79c-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="3a79c-120">Specifica un elenco di allegati nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="3a79c-121">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="3a79c-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="3a79c-122">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-122">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-123">Specifica gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="3a79c-124">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="3a79c-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="3a79c-125">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-125">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-126">Specifica il testo nel corpo del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="3a79c-127">**CC**</span><span class="sxs-lookup"><span data-stu-id="3a79c-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="3a79c-128">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-128">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-129">Specifica gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="3a79c-130">**Da**</span><span class="sxs-lookup"><span data-stu-id="3a79c-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="3a79c-131">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-131">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-132">Specifica l'indirizzo di posta elettronica del mittente.</span><span class="sxs-lookup"><span data-stu-id="3a79c-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="3a79c-133">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="3a79c-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="3a79c-134">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="3a79c-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="3a79c-135">Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="3a79c-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="3a79c-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="3a79c-137">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-137">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-138">Specifica gli indirizzi di posta elettronica a cui risponde nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="3a79c-139">**Server**</span><span class="sxs-lookup"><span data-stu-id="3a79c-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="3a79c-140">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="3a79c-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="3a79c-141">Specifica il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="3a79c-142">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="3a79c-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="3a79c-143">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-143">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-144">Specifica l'oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="3a79c-145">**A**</span><span class="sxs-lookup"><span data-stu-id="3a79c-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="3a79c-146">**string**</span><span class="sxs-lookup"><span data-stu-id="3a79c-146">**string**</span></span>                                                                   | <span data-ttu-id="3a79c-147">Specifica gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3a79c-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="3a79c-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a79c-148">Remarks</span></span>

<span data-ttu-id="3a79c-149">Per lo sviluppo in C++, vedere l'interfaccia [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .</span><span class="sxs-lookup"><span data-stu-id="3a79c-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="3a79c-150">Per lo sviluppo di script, vedere l'oggetto [**EmailAction**](emailaction.md) .</span><span class="sxs-lookup"><span data-stu-id="3a79c-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="3a79c-151">**Windows 8 e Windows Server 2012:** Questo elemento è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="3a79c-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="3a79c-152">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a79c-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="3a79c-153">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a79c-153">Examples</span></span>

<span data-ttu-id="3a79c-154">Per un esempio completo del codice XML per un'attività che specifica un'azione di posta elettronica, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a79c-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a79c-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a79c-155">Requirements</span></span>



| <span data-ttu-id="3a79c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a79c-156">Requirement</span></span> | <span data-ttu-id="3a79c-157">Valore</span><span class="sxs-lookup"><span data-stu-id="3a79c-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a79c-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a79c-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3a79c-159">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a79c-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a79c-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a79c-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3a79c-161">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a79c-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3a79c-162">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3a79c-162">End of client support</span></span><br/>    | <span data-ttu-id="3a79c-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a79c-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="3a79c-164">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3a79c-164">End of server support</span></span><br/>    | <span data-ttu-id="3a79c-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a79c-165">Windows Server 2008 R2</span></span><br/>                    |



 

