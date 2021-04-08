---
title: Proprietà EmailAction. HeaderFields
description: Per gli script, ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si desidera inviare.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Utilità di pianificazione proprietà HeaderFields
- Utilità di pianificazione proprietà HeaderFields, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà HeaderFields
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873958"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="58ef1-106">Proprietà EmailAction. HeaderFields</span><span class="sxs-lookup"><span data-stu-id="58ef1-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="58ef1-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="58ef1-107">\[This object is no longer supported.</span></span> <span data-ttu-id="58ef1-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="58ef1-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="58ef1-109">Per gli script, ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si desidera inviare.</span><span class="sxs-lookup"><span data-stu-id="58ef1-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="58ef1-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="58ef1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ef1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58ef1-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="58ef1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="58ef1-112">Property value</span></span>

<span data-ttu-id="58ef1-113">Informazioni di intestazione nel messaggio di posta elettronica che si desidera inviare.</span><span class="sxs-lookup"><span data-stu-id="58ef1-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ef1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ef1-114">Requirements</span></span>



| <span data-ttu-id="58ef1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ef1-115">Requirement</span></span> | <span data-ttu-id="58ef1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="58ef1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ef1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ef1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58ef1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58ef1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58ef1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ef1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58ef1-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58ef1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58ef1-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="58ef1-121">End of client support</span></span><br/>    | <span data-ttu-id="58ef1-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58ef1-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="58ef1-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="58ef1-123">End of server support</span></span><br/>    | <span data-ttu-id="58ef1-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58ef1-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="58ef1-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="58ef1-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="58ef1-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58ef1-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58ef1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="58ef1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58ef1-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ef1-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ef1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ef1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ef1-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="58ef1-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="58ef1-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="58ef1-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

