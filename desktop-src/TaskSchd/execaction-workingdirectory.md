---
title: Proprietà ExecAction. WorkingDirectory
description: Per la creazione di script, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Utilità di pianificazione proprietà WorkingDirectory
- Utilità di pianificazione proprietà WorkingDirectory, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301342"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="7597a-106">Proprietà ExecAction. WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="7597a-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="7597a-107">Per la creazione di script, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7597a-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7597a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7597a-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="7597a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7597a-109">Property value</span></span>

<span data-ttu-id="7597a-110">Directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7597a-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7597a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7597a-111">Remarks</span></span>

<span data-ttu-id="7597a-112">Durante la lettura o la scrittura di codice XML, la directory di lavoro dell'applicazione viene specificata nell'elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7597a-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="7597a-113">Il percorso è verificato per assicurarsi che sia valido quando l'attività è registrata, non quando questa proprietà è impostata.</span><span class="sxs-lookup"><span data-stu-id="7597a-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7597a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7597a-114">Requirements</span></span>



| <span data-ttu-id="7597a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7597a-115">Requirement</span></span> | <span data-ttu-id="7597a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7597a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7597a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7597a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7597a-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7597a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7597a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7597a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7597a-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7597a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7597a-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7597a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7597a-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7597a-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7597a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7597a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7597a-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7597a-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7597a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7597a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7597a-126">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="7597a-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="7597a-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7597a-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





