---
title: Proprietà EmailAction. Attachments
description: Per gli script, ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Utilità di pianificazione proprietà allegati
- Utilità di pianificazione proprietà allegati, oggetto EmailAction
- Utilità di pianificazione oggetto EmailAction, proprietà Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741903"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="b042a-106">Proprietà EmailAction. Attachments</span><span class="sxs-lookup"><span data-stu-id="b042a-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="b042a-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="b042a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b042a-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="b042a-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="b042a-109">Per gli script, ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b042a-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="b042a-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b042a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b042a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b042a-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="b042a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b042a-112">Property value</span></span>

<span data-ttu-id="b042a-113">Matrice di allegati inviata con il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b042a-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b042a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b042a-114">Remarks</span></span>

<span data-ttu-id="b042a-115">Un massimo di otto allegati può essere nella matrice di allegati.</span><span class="sxs-lookup"><span data-stu-id="b042a-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="b042a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b042a-116">Requirements</span></span>



| <span data-ttu-id="b042a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b042a-117">Requirement</span></span> | <span data-ttu-id="b042a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b042a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b042a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b042a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b042a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b042a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b042a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b042a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b042a-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b042a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b042a-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b042a-123">End of client support</span></span><br/>    | <span data-ttu-id="b042a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b042a-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b042a-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b042a-125">End of server support</span></span><br/>    | <span data-ttu-id="b042a-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b042a-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b042a-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b042a-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b042a-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b042a-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b042a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b042a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b042a-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b042a-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b042a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b042a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b042a-132">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="b042a-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="b042a-133">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b042a-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

