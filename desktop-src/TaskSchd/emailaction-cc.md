---
title: Proprietà EmailAction.Cc
description: Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi da inserire in CC nel messaggio di posta elettronica.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Utilità di pianificazione proprietà CC
- Utilità di pianificazione proprietà CC, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà CC
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741898"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="ca516-106">Proprietà EmailAction.Cc</span><span class="sxs-lookup"><span data-stu-id="ca516-106">EmailAction.Cc property</span></span>

<span data-ttu-id="ca516-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="ca516-107">\[This object is no longer supported.</span></span> <span data-ttu-id="ca516-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="ca516-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="ca516-109">Per lo scripting, ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi da inserire in CC nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ca516-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="ca516-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ca516-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca516-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca516-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="ca516-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ca516-112">Property value</span></span>

<span data-ttu-id="ca516-113">Indirizzo di posta elettronica o indirizzi da inserire in CC nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ca516-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca516-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca516-114">Requirements</span></span>



| <span data-ttu-id="ca516-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca516-115">Requirement</span></span> | <span data-ttu-id="ca516-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ca516-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca516-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca516-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca516-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca516-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ca516-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca516-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca516-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca516-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca516-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ca516-121">End of client support</span></span><br/>    | <span data-ttu-id="ca516-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca516-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="ca516-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ca516-123">End of server support</span></span><br/>    | <span data-ttu-id="ca516-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca516-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ca516-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca516-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca516-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca516-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca516-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ca516-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca516-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca516-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca516-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca516-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca516-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="ca516-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="ca516-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ca516-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

