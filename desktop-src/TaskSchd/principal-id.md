---
title: Proprietà Principal.Id
description: Per lo scripting, ottiene o imposta l'identificatore dell'entità.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- ID Utilità di pianificazione proprietà
- Utilità di pianificazione proprietà ID, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400799"
---
# <a name="principalid-property"></a><span data-ttu-id="be351-106">Proprietà Principal.Id</span><span class="sxs-lookup"><span data-stu-id="be351-106">Principal.Id property</span></span>

<span data-ttu-id="be351-107">Per lo scripting, ottiene o imposta l'identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="be351-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="be351-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be351-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="be351-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="be351-109">Property value</span></span>

<span data-ttu-id="be351-110">Identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="be351-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="be351-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="be351-111">Remarks</span></span>

<span data-ttu-id="be351-112">Questo identificatore viene usato anche quando si specifica la proprietà [**ActionCollection. Context**](actioncollection-context.md) .</span><span class="sxs-lookup"><span data-stu-id="be351-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="be351-113">Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore dell'entità viene specificato nell'attributo ID dell'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="be351-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="be351-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be351-114">Requirements</span></span>



| <span data-ttu-id="be351-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="be351-115">Requirement</span></span> | <span data-ttu-id="be351-116">Valore</span><span class="sxs-lookup"><span data-stu-id="be351-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be351-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be351-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be351-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be351-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="be351-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be351-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be351-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be351-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be351-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="be351-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="be351-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="be351-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="be351-123">DLL</span><span class="sxs-lookup"><span data-stu-id="be351-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be351-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be351-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be351-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be351-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be351-126">**ActionCollection. Context**</span><span class="sxs-lookup"><span data-stu-id="be351-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="be351-127">**Principale**</span><span class="sxs-lookup"><span data-stu-id="be351-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="be351-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="be351-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





