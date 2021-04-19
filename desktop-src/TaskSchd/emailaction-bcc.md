---
title: Proprietà EmailAction. BCC
description: Per la creazione di script, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi che si desidera inserire nel messaggio di posta elettronica.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- Utilità di pianificazione proprietà Ccn
- Utilità di pianificazione proprietà Ccn, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà Ccn
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bded5e88c236123832956ce42413352348ea535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301787"
---
# <a name="emailactionbcc-property"></a><span data-ttu-id="8ccc1-106">Proprietà EmailAction. BCC</span><span class="sxs-lookup"><span data-stu-id="8ccc1-106">EmailAction.Bcc property</span></span>

<span data-ttu-id="8ccc1-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="8ccc1-107">\[This object is no longer supported.</span></span> <span data-ttu-id="8ccc1-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="8ccc1-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="8ccc1-109">Per la creazione di script, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi che si desidera inserire nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="8ccc1-109">For scripting, gets or sets the email address or addresses that you want to Bcc in the email message.</span></span>

<span data-ttu-id="8ccc1-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8ccc1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ccc1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ccc1-111">Syntax</span></span>


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a><span data-ttu-id="8ccc1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8ccc1-112">Property value</span></span>

<span data-ttu-id="8ccc1-113">Indirizzo di posta elettronica o indirizzi che si desidera inserire nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="8ccc1-113">The email address or addresses that you want to Bcc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ccc1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ccc1-114">Requirements</span></span>



| <span data-ttu-id="8ccc1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ccc1-115">Requirement</span></span> | <span data-ttu-id="8ccc1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8ccc1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ccc1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ccc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccc1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ccc1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8ccc1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ccc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccc1-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ccc1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ccc1-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8ccc1-121">End of client support</span></span><br/>    | <span data-ttu-id="8ccc1-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ccc1-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="8ccc1-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8ccc1-123">End of server support</span></span><br/>    | <span data-ttu-id="8ccc1-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ccc1-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8ccc1-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ccc1-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ccc1-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ccc1-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ccc1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8ccc1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ccc1-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ccc1-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ccc1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ccc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ccc1-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="8ccc1-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="8ccc1-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8ccc1-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

