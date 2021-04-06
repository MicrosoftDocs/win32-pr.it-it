---
title: Proprietà EmailAction. ReplyTo
description: Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica a cui si desidera rispondere.
ms.assetid: 2b267e6e-c0c9-42ca-bc4a-cc18af5bcb9c
keywords:
- ReplyTo Utilità di pianificazione proprietà
- ReplyTo Utilità di pianificazione proprietà, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà ReplyTo
topic_type:
- apiref
api_name:
- EmailAction.ReplyTo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7ed1fd84245e4d938d329f0e9773271efec45b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873957"
---
# <a name="emailactionreplyto-property"></a><span data-ttu-id="f6714-106">Proprietà EmailAction. ReplyTo</span><span class="sxs-lookup"><span data-stu-id="f6714-106">EmailAction.ReplyTo property</span></span>

<span data-ttu-id="f6714-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="f6714-107">\[This object is no longer supported.</span></span> <span data-ttu-id="f6714-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="f6714-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="f6714-109">Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica a cui si desidera rispondere.</span><span class="sxs-lookup"><span data-stu-id="f6714-109">For scripting, gets or sets the email address that you want to reply to.</span></span>

<span data-ttu-id="f6714-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f6714-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6714-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6714-111">Syntax</span></span>


```VB
EmailAction.ReplyTo As String
```



## <a name="property-value"></a><span data-ttu-id="f6714-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f6714-112">Property value</span></span>

<span data-ttu-id="f6714-113">Indirizzo di posta elettronica a cui si desidera rispondere.</span><span class="sxs-lookup"><span data-stu-id="f6714-113">The email address that you want to reply to.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6714-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6714-114">Requirements</span></span>



| <span data-ttu-id="f6714-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6714-115">Requirement</span></span> | <span data-ttu-id="f6714-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f6714-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6714-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6714-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6714-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6714-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f6714-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6714-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6714-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6714-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6714-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f6714-121">End of client support</span></span><br/>    | <span data-ttu-id="f6714-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6714-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="f6714-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f6714-123">End of server support</span></span><br/>    | <span data-ttu-id="f6714-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6714-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f6714-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f6714-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6714-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f6714-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f6714-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f6714-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6714-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6714-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6714-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6714-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6714-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="f6714-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="f6714-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f6714-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

