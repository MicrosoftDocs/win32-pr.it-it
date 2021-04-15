---
title: Proprietà EmailAction.To
description: Per gli script, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi a cui si desidera inviare il messaggio di posta elettronica.
ms.assetid: 592ae58c-a519-4f1b-8976-315befa77e1e
keywords:
- Alla proprietà Utilità di pianificazione
- Per Utilità di pianificazione proprietà, oggetto EmailAction
- Utilità di pianificazione oggetto EmailAction, proprietà
topic_type:
- apiref
api_name:
- EmailAction.To
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a7d09a0962fa4fbd680341ba7f046ef4a5eacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477212"
---
# <a name="emailactionto-property"></a><span data-ttu-id="144b3-106">Proprietà EmailAction.To</span><span class="sxs-lookup"><span data-stu-id="144b3-106">EmailAction.To property</span></span>

<span data-ttu-id="144b3-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="144b3-107">\[This object is no longer supported.</span></span> <span data-ttu-id="144b3-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="144b3-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="144b3-109">Per gli script, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi a cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="144b3-109">For scripting, gets or sets the email address or addresses that you want to send the email to.</span></span>

<span data-ttu-id="144b3-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="144b3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="144b3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="144b3-111">Syntax</span></span>


```VB
EmailAction.To As String
```



## <a name="property-value"></a><span data-ttu-id="144b3-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="144b3-112">Property value</span></span>

<span data-ttu-id="144b3-113">Indirizzo di posta elettronica o indirizzi a cui si desidera inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="144b3-113">The email address or addresses that you want to send the email to.</span></span>

## <a name="requirements"></a><span data-ttu-id="144b3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="144b3-114">Requirements</span></span>



| <span data-ttu-id="144b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="144b3-115">Requirement</span></span> | <span data-ttu-id="144b3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="144b3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="144b3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="144b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="144b3-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="144b3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="144b3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="144b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="144b3-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="144b3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="144b3-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="144b3-121">End of client support</span></span><br/>    | <span data-ttu-id="144b3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="144b3-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="144b3-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="144b3-123">End of server support</span></span><br/>    | <span data-ttu-id="144b3-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="144b3-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="144b3-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="144b3-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="144b3-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="144b3-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="144b3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="144b3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="144b3-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="144b3-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144b3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="144b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144b3-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="144b3-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="144b3-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="144b3-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

