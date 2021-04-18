---
title: Proprietà EmailAction. Body
description: Per lo scripting, ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Utilità di pianificazione proprietà corpo
- Utilità di pianificazione proprietà corpo, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301786"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="a4fb1-106">Proprietà EmailAction. Body</span><span class="sxs-lookup"><span data-stu-id="a4fb1-106">EmailAction.Body property</span></span>

<span data-ttu-id="a4fb1-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-107">\[This object is no longer supported.</span></span> <span data-ttu-id="a4fb1-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="a4fb1-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="a4fb1-109">Per lo scripting, ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="a4fb1-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4fb1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4fb1-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="a4fb1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a4fb1-112">Property value</span></span>

<span data-ttu-id="a4fb1-113">Corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4fb1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4fb1-114">Remarks</span></span>

<span data-ttu-id="a4fb1-115">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="a4fb1-116">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="a4fb1-117">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="a4fb1-118">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4fb1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4fb1-119">Requirements</span></span>



| <span data-ttu-id="a4fb1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4fb1-120">Requirement</span></span> | <span data-ttu-id="a4fb1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a4fb1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4fb1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a4fb1-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4fb1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a4fb1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4fb1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a4fb1-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4fb1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4fb1-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a4fb1-126">End of client support</span></span><br/>    | <span data-ttu-id="a4fb1-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4fb1-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a4fb1-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a4fb1-128">End of server support</span></span><br/>    | <span data-ttu-id="a4fb1-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4fb1-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a4fb1-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a4fb1-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4fb1-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4fb1-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4fb1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a4fb1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4fb1-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4fb1-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4fb1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4fb1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4fb1-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="a4fb1-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="a4fb1-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a4fb1-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

