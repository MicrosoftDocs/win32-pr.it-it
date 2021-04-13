---
title: Proprietà LogonTrigger. UserId
description: Per lo scripting, ottiene o imposta l'identificatore dell'utente.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Utilità di pianificazione proprietà UserId
- Utilità di pianificazione proprietà UserId, oggetto LogonTrigger
- Oggetto LogonTrigger Utilità di pianificazione, Proprietà UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400348"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="77380-106">Proprietà LogonTrigger. UserId</span><span class="sxs-lookup"><span data-stu-id="77380-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="77380-107">Per lo scripting, ottiene o imposta l'identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77380-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="77380-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77380-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="77380-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="77380-109">Property value</span></span>

<span data-ttu-id="77380-110">Identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77380-110">The identifier of the user.</span></span> <span data-ttu-id="77380-111">Ad esempio, "nome dominio \\ " o per un account locale, "Administrator".</span><span class="sxs-lookup"><span data-stu-id="77380-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="77380-112">Questa proprietà può essere in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="77380-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="77380-113">Nome utente o SID: l'attività viene avviata quando l'utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="77380-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="77380-114">NULL: l'attività viene avviata quando un utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="77380-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="77380-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="77380-115">Remarks</span></span>

<span data-ttu-id="77380-116">Se si desidera che un'attività venga attivata quando un membro di un gruppo accede al computer anziché quando un utente specifico esegue l'accesso, non assegnare un valore alla proprietà **LogonTrigger. UserID** .</span><span class="sxs-lookup"><span data-stu-id="77380-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="77380-117">In alternativa, creare un trigger LOGON con una proprietà **LogonTrigger. UserID** vuota e assegnare un valore all'entità per l'attività usando la proprietà [**Principal. GroupID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="77380-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="77380-118">Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore utente di accesso viene specificato utilizzando l'elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="77380-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="77380-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77380-119">Requirements</span></span>



| <span data-ttu-id="77380-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77380-120">Requirement</span></span> | <span data-ttu-id="77380-121">Valore</span><span class="sxs-lookup"><span data-stu-id="77380-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77380-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77380-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77380-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77380-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77380-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77380-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77380-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77380-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77380-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="77380-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="77380-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77380-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77380-128">DLL</span><span class="sxs-lookup"><span data-stu-id="77380-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77380-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77380-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77380-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77380-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77380-131">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="77380-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="77380-132">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="77380-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





