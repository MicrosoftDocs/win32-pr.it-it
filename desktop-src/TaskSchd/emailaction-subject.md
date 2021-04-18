---
title: Proprietà EmailAction. Subject
description: Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Proprietà Subject Utilità di pianificazione
- Utilità di pianificazione proprietà Subject, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304746"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="3ddd7-106">Proprietà EmailAction. Subject</span><span class="sxs-lookup"><span data-stu-id="3ddd7-106">EmailAction.Subject property</span></span>

<span data-ttu-id="3ddd7-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-107">\[This object is no longer supported.</span></span> <span data-ttu-id="3ddd7-108">Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) di PowerShell.\]</span><span class="sxs-lookup"><span data-stu-id="3ddd7-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="3ddd7-109">Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="3ddd7-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddd7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ddd7-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="3ddd7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3ddd7-112">Property value</span></span>

<span data-ttu-id="3ddd7-113">Oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddd7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ddd7-114">Remarks</span></span>

<span data-ttu-id="3ddd7-115">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="3ddd7-116">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="3ddd7-117">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="3ddd7-118">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="3ddd7-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddd7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ddd7-119">Requirements</span></span>



| <span data-ttu-id="3ddd7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ddd7-120">Requirement</span></span> | <span data-ttu-id="3ddd7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3ddd7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddd7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ddd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddd7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ddd7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ddd7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ddd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddd7-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ddd7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ddd7-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3ddd7-126">End of client support</span></span><br/>    | <span data-ttu-id="3ddd7-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ddd7-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="3ddd7-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3ddd7-128">End of server support</span></span><br/>    | <span data-ttu-id="3ddd7-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ddd7-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3ddd7-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3ddd7-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ddd7-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd7-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ddd7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3ddd7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ddd7-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd7-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddd7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ddd7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddd7-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="3ddd7-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="3ddd7-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3ddd7-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

