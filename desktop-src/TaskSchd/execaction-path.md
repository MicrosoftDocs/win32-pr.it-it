---
title: Proprietà ExecAction. Path
description: Per lo scripting, ottiene o imposta il percorso di un file eseguibile.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Utilità di pianificazione proprietà Path
- Utilità di pianificazione proprietà Path, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740858"
---
# <a name="execactionpath-property"></a><span data-ttu-id="c6814-106">Proprietà ExecAction. Path</span><span class="sxs-lookup"><span data-stu-id="c6814-106">ExecAction.Path property</span></span>

<span data-ttu-id="c6814-107">Per lo scripting, ottiene o imposta il percorso di un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="c6814-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6814-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6814-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="c6814-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c6814-109">Property value</span></span>

<span data-ttu-id="c6814-110">Percorso del file eseguibile che deve essere eseguito dall'azione.</span><span class="sxs-lookup"><span data-stu-id="c6814-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6814-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6814-111">Remarks</span></span>

<span data-ttu-id="c6814-112">Questa azione esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c6814-112">This action performs a command-line operation.</span></span> <span data-ttu-id="c6814-113">Ad esempio, l'azione potrebbe eseguire uno script o avviare un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="c6814-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="c6814-114">Durante la lettura o la scrittura di codice XML, il percorso dell'operazione della riga di comando viene specificato nell'elemento [**Command**](taskschedulerschema-command-exectype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c6814-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c6814-115">Il percorso è verificato per assicurarsi che sia valido quando l'attività è registrata, non quando questa proprietà è impostata.</span><span class="sxs-lookup"><span data-stu-id="c6814-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6814-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6814-116">Requirements</span></span>



| <span data-ttu-id="c6814-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6814-117">Requirement</span></span> | <span data-ttu-id="c6814-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c6814-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6814-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6814-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6814-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6814-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c6814-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6814-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6814-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6814-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6814-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c6814-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6814-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6814-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6814-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c6814-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6814-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6814-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6814-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6814-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6814-128">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="c6814-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="c6814-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c6814-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





