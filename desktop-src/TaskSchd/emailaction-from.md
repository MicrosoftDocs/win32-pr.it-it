---
title: Proprietà EmailAction. from
description: Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica da cui si desidera inviare il messaggio di posta elettronica.
ms.assetid: befe6900-6fbe-4ba2-aeda-271b770e971a
keywords:
- Da proprietà Utilità di pianificazione
- Da Property Utilità di pianificazione, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, da proprietà
topic_type:
- apiref
api_name:
- EmailAction.From
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d91b132e8d56caba1a21768e4aacfdda855fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120062"
---
# <a name="emailactionfrom-property"></a><span data-ttu-id="bb8e2-106">Proprietà EmailAction. from</span><span class="sxs-lookup"><span data-stu-id="bb8e2-106">EmailAction.From property</span></span>

<span data-ttu-id="bb8e2-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="bb8e2-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="bb8e2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="bb8e2-109">Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica da cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-109">For scripting, gets or sets the email address that you want to send the email from.</span></span>

<span data-ttu-id="bb8e2-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8e2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb8e2-111">Syntax</span></span>


```VB
EmailAction.From As String
```



## <a name="property-value"></a><span data-ttu-id="bb8e2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb8e2-112">Property value</span></span>

<span data-ttu-id="bb8e2-113">Indirizzo di posta elettronica da cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="bb8e2-113">The email address that you want to send the email from.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8e2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb8e2-114">Requirements</span></span>



| <span data-ttu-id="bb8e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb8e2-115">Requirement</span></span> | <span data-ttu-id="bb8e2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bb8e2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8e2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb8e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8e2-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb8e2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb8e2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb8e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8e2-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb8e2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb8e2-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb8e2-121">End of client support</span></span><br/>    | <span data-ttu-id="bb8e2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb8e2-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="bb8e2-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bb8e2-123">End of server support</span></span><br/>    | <span data-ttu-id="bb8e2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb8e2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="bb8e2-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bb8e2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb8e2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb8e2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bb8e2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb8e2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb8e2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb8e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8e2-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="bb8e2-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="bb8e2-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bb8e2-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

