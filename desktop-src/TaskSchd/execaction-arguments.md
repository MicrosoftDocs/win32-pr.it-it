---
title: Proprietà ExecAction. Arguments
description: Per gli script, ottiene o imposta gli argomenti associati all'operazione della riga di comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Proprietà Arguments Utilità di pianificazione
- Utilità di pianificazione proprietà arguments, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963989"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="3ba85-106">Proprietà ExecAction. Arguments</span><span class="sxs-lookup"><span data-stu-id="3ba85-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="3ba85-107">Per gli script, ottiene o imposta gli argomenti associati all'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3ba85-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba85-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ba85-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="3ba85-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3ba85-109">Property value</span></span>

<span data-ttu-id="3ba85-110">Argomenti necessari per l'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3ba85-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba85-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ba85-111">Remarks</span></span>

<span data-ttu-id="3ba85-112">Durante la lettura o la scrittura di codice XML, gli argomenti dell'operazione della riga di comando vengono specificati nell'elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3ba85-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba85-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ba85-113">Requirements</span></span>



| <span data-ttu-id="3ba85-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba85-114">Requirement</span></span> | <span data-ttu-id="3ba85-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3ba85-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba85-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ba85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba85-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ba85-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ba85-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ba85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba85-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ba85-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ba85-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3ba85-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ba85-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ba85-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ba85-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba85-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ba85-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ba85-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba85-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ba85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba85-125">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="3ba85-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="3ba85-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3ba85-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





