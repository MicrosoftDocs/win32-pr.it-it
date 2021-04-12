---
title: Proprietà Principal. UserId
description: Per gli script, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Utilità di pianificazione proprietà UserId
- Utilità di pianificazione proprietà UserId, oggetto Principal
- Utilità di pianificazione oggetto Principal, Proprietà UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120222"
---
# <a name="principaluserid-property"></a><span data-ttu-id="85afb-106">Proprietà Principal. UserId</span><span class="sxs-lookup"><span data-stu-id="85afb-106">Principal.UserId property</span></span>

<span data-ttu-id="85afb-107">Per gli script, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="85afb-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="85afb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85afb-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="85afb-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="85afb-109">Property value</span></span>

<span data-ttu-id="85afb-110">Identificatore utente necessario per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="85afb-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="85afb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="85afb-111">Remarks</span></span>

<span data-ttu-id="85afb-112">Non impostare questa proprietà se nella proprietà [**GroupID**](principal-groupid.md) viene specificato un identificatore di gruppo.</span><span class="sxs-lookup"><span data-stu-id="85afb-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="85afb-113">Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore utente per l'entità viene specificato utilizzando l'elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="85afb-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="85afb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85afb-114">Requirements</span></span>



| <span data-ttu-id="85afb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="85afb-115">Requirement</span></span> | <span data-ttu-id="85afb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="85afb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85afb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85afb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85afb-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85afb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="85afb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85afb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85afb-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85afb-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85afb-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="85afb-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="85afb-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85afb-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85afb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="85afb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85afb-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85afb-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85afb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85afb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85afb-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="85afb-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="85afb-127">**Principale**</span><span class="sxs-lookup"><span data-stu-id="85afb-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="85afb-128">**Entità. GroupId**</span><span class="sxs-lookup"><span data-stu-id="85afb-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





