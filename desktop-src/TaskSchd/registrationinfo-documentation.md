---
title: RegistrationInfo.Docproprietà umentation
description: Per la creazione di script, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Utilità di pianificazione proprietà documentazione
- Utilità di pianificazione proprietà della documentazione, oggetto RegistrationInfo
- Utilità di pianificazione oggetto RegistrationInfo, Proprietà Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118930"
---
# <a name="registrationinfodocumentation-property"></a><span data-ttu-id="624d3-106">RegistrationInfo.Docproprietà umentation</span><span class="sxs-lookup"><span data-stu-id="624d3-106">RegistrationInfo.Documentation property</span></span>

<span data-ttu-id="624d3-107">Per la creazione di script, ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.</span><span class="sxs-lookup"><span data-stu-id="624d3-107">For scripting, gets or sets any additional documentation for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="624d3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="624d3-108">Syntax</span></span>


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a><span data-ttu-id="624d3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="624d3-109">Property value</span></span>

<span data-ttu-id="624d3-110">Documentazione aggiuntiva associata all'attività.</span><span class="sxs-lookup"><span data-stu-id="624d3-110">Any additional documentation that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="624d3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="624d3-111">Remarks</span></span>

<span data-ttu-id="624d3-112">Durante la lettura o la scrittura di codice XML per un'attività, la documentazione aggiuntiva per l'attività viene specificata utilizzando l'elemento [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="624d3-112">When reading or writing XML for a task, the additional documentation for the task is specified using the [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="624d3-113">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="624d3-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="624d3-114">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="624d3-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="624d3-115">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="624d3-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="624d3-116">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="624d3-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="624d3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="624d3-117">Requirements</span></span>



| <span data-ttu-id="624d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="624d3-118">Requirement</span></span> | <span data-ttu-id="624d3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="624d3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="624d3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="624d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="624d3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="624d3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="624d3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="624d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="624d3-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="624d3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="624d3-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="624d3-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="624d3-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="624d3-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="624d3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="624d3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="624d3-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="624d3-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="624d3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="624d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624d3-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="624d3-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





