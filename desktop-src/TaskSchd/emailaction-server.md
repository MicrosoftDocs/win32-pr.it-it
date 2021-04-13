---
title: Proprietà EmailAction. Server
description: Per la creazione di script, ottiene o imposta il nome del server SMTP da usare per l'invio di messaggi di posta elettronica.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Utilità di pianificazione proprietà server
- Proprietà Server Utilità di pianificazione, oggetto EmailAction
- Utilità di pianificazione oggetto EmailAction, proprietà server
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340772"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="f4559-106">Proprietà EmailAction. Server</span><span class="sxs-lookup"><span data-stu-id="f4559-106">EmailAction.Server property</span></span>

<span data-ttu-id="f4559-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="f4559-107">\[This object is no longer supported.</span></span> <span data-ttu-id="f4559-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="f4559-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="f4559-109">Per la creazione di script, ottiene o imposta il nome del server SMTP da usare per l'invio di messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f4559-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="f4559-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f4559-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4559-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4559-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="f4559-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f4559-112">Property value</span></span>

<span data-ttu-id="f4559-113">Nome del server utilizzato per l'invio di messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f4559-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4559-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4559-114">Remarks</span></span>

<span data-ttu-id="f4559-115">Verificare che il server SMTP che invia il messaggio di posta elettronica sia configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f4559-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="f4559-116">La posta elettronica viene inviata utilizzando l'autenticazione NTLM per i server SMTP di Windows, il che significa che le credenziali di sicurezza utilizzate per l'esecuzione dell'attività devono disporre anche dei privilegi sul server SMTP per l'invio di messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f4559-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="f4559-117">Se il server SMTP è un server non basato su Windows, il messaggio di posta elettronica verrà inviato se il server consente l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="f4559-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="f4559-118">Per informazioni sulla configurazione del server SMTP, vedere [configurazione del server SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e per informazioni sulla gestione delle impostazioni del server SMTP, vedere [Amministrazione SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="f4559-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4559-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4559-119">Requirements</span></span>



| <span data-ttu-id="f4559-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4559-120">Requirement</span></span> | <span data-ttu-id="f4559-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f4559-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4559-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4559-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4559-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4559-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4559-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4559-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4559-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4559-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4559-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f4559-126">End of client support</span></span><br/>    | <span data-ttu-id="f4559-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4559-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="f4559-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f4559-128">End of server support</span></span><br/>    | <span data-ttu-id="f4559-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4559-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f4559-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4559-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4559-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f4559-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f4559-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f4559-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4559-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4559-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4559-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4559-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4559-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="f4559-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="f4559-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f4559-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

