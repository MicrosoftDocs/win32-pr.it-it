---
title: Proprietà Principal. DisplayName
description: Per lo scripting, ottiene o imposta il nome dell'entità.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Proprietà DisplayName Utilità di pianificazione
- Utilità di pianificazione proprietà DisplayName, oggetto Principal
- Utilità di pianificazione oggetto Principal, proprietà DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741874"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="bc835-106">Proprietà Principal. DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc835-106">Principal.DisplayName property</span></span>

<span data-ttu-id="bc835-107">Per lo scripting, ottiene o imposta il nome dell'entità.</span><span class="sxs-lookup"><span data-stu-id="bc835-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="bc835-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc835-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="bc835-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bc835-109">Property value</span></span>

<span data-ttu-id="bc835-110">Nome dell'entità.</span><span class="sxs-lookup"><span data-stu-id="bc835-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc835-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc835-111">Remarks</span></span>

<span data-ttu-id="bc835-112">Durante la lettura o la scrittura di codice XML per un'attività, il nome visualizzato per un'entità viene specificato nell'elemento [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc835-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="bc835-113">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="bc835-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="bc835-114">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc835-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="bc835-115">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc835-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="bc835-116">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="bc835-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc835-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc835-117">Requirements</span></span>



| <span data-ttu-id="bc835-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc835-118">Requirement</span></span> | <span data-ttu-id="bc835-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bc835-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc835-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc835-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc835-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc835-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bc835-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc835-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc835-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc835-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc835-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bc835-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc835-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc835-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc835-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bc835-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc835-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc835-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc835-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc835-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc835-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bc835-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bc835-130">**Principale**</span><span class="sxs-lookup"><span data-stu-id="bc835-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





