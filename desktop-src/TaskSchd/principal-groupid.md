---
title: Proprietà Principal. GroupId
description: Per gli script, ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Utilità di pianificazione proprietà GroupId
- Utilità di pianificazione proprietà GroupId, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302013"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="f4953-106">Proprietà Principal. GroupId</span><span class="sxs-lookup"><span data-stu-id="f4953-106">Principal.GroupId property</span></span>

<span data-ttu-id="f4953-107">Per gli script, ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="f4953-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4953-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4953-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="f4953-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f4953-109">Property value</span></span>

<span data-ttu-id="f4953-110">Identificatore del gruppo di utenti associato a questa entità.</span><span class="sxs-lookup"><span data-stu-id="f4953-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4953-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4953-111">Remarks</span></span>

<span data-ttu-id="f4953-112">Non impostare questa proprietà se nella proprietà [**userid**](principal-userid.md) viene specificato un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="f4953-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="f4953-113">Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore di gruppo per un'entità viene specificato nell'elemento [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f4953-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4953-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4953-114">Requirements</span></span>



| <span data-ttu-id="f4953-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4953-115">Requirement</span></span> | <span data-ttu-id="f4953-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f4953-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4953-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4953-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f4953-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4953-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4953-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4953-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f4953-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4953-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4953-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4953-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4953-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f4953-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f4953-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f4953-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4953-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4953-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4953-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4953-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4953-126">**UserId**</span><span class="sxs-lookup"><span data-stu-id="f4953-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="f4953-127">**Principale**</span><span class="sxs-lookup"><span data-stu-id="f4953-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="f4953-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f4953-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





