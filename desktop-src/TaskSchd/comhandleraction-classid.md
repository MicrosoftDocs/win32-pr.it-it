---
title: Proprietà ComHandlerAction. ClassID
description: Per gli script, ottiene o imposta l'identificatore della classe del gestore.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Utilità di pianificazione proprietà ClassID
- Utilità di pianificazione proprietà ClassID, oggetto ComHandlerAction
- Oggetto ComHandlerAction Utilità di pianificazione, proprietà ClassID
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740866"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="e96c7-106">Proprietà ComHandlerAction. ClassID</span><span class="sxs-lookup"><span data-stu-id="e96c7-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="e96c7-107">Per gli script, ottiene o imposta l'identificatore della classe del gestore.</span><span class="sxs-lookup"><span data-stu-id="e96c7-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="e96c7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e96c7-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="e96c7-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e96c7-109">Property value</span></span>

<span data-ttu-id="e96c7-110">Identificatore della classe che definisce il gestore da attivare.</span><span class="sxs-lookup"><span data-stu-id="e96c7-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="e96c7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e96c7-111">Remarks</span></span>

<span data-ttu-id="e96c7-112">Durante la lettura o la scrittura di codice XML, la classe di un gestore COM viene specificata nell'elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e96c7-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96c7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e96c7-113">Requirements</span></span>



| <span data-ttu-id="e96c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96c7-114">Requirement</span></span> | <span data-ttu-id="e96c7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e96c7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e96c7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e96c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e96c7-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e96c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e96c7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e96c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e96c7-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e96c7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e96c7-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e96c7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e96c7-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e96c7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e96c7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e96c7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e96c7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e96c7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e96c7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e96c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96c7-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e96c7-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e96c7-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="e96c7-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





