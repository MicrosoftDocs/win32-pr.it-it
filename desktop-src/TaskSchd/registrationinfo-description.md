---
title: Proprietà RegistrationInfo. Description
description: Per la creazione di script, ottiene o imposta la descrizione dell'attività.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Proprietà Description Utilità di pianificazione
- Descrizione Utilità di pianificazione proprietà, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, proprietà Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400206"
---
# <a name="registrationinfodescription-property"></a><span data-ttu-id="c1095-106">Proprietà RegistrationInfo. Description</span><span class="sxs-lookup"><span data-stu-id="c1095-106">RegistrationInfo.Description property</span></span>

<span data-ttu-id="c1095-107">Per la creazione di script, ottiene o imposta la descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c1095-107">For scripting, gets or sets the description of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1095-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1095-108">Syntax</span></span>


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a><span data-ttu-id="c1095-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c1095-109">Property value</span></span>

<span data-ttu-id="c1095-110">Descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c1095-110">The description of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1095-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1095-111">Remarks</span></span>

<span data-ttu-id="c1095-112">Durante la lettura o la scrittura di codice XML per un'attività, la descrizione dell'attività viene specificata utilizzando l'elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c1095-112">When reading or writing XML for a task, the description of the task is specified using the [**Description**](taskschedulerschema-description-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c1095-113">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="c1095-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="c1095-114">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1095-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="c1095-115">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1095-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="c1095-116">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="c1095-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1095-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1095-117">Requirements</span></span>



| <span data-ttu-id="c1095-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1095-118">Requirement</span></span> | <span data-ttu-id="c1095-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c1095-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1095-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1095-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1095-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1095-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c1095-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1095-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1095-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1095-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1095-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c1095-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1095-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1095-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1095-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c1095-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1095-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1095-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1095-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1095-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1095-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c1095-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





