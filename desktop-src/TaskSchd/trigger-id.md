---
title: Proprietà Trigger.Id
description: Per lo scripting, ottiene o imposta l'identificatore per il trigger.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- ID Utilità di pianificazione proprietà
- ID Utilità di pianificazione proprietà, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517559"
---
# <a name="triggerid-property"></a><span data-ttu-id="aaf68-106">Proprietà Trigger.Id</span><span class="sxs-lookup"><span data-stu-id="aaf68-106">Trigger.Id property</span></span>

<span data-ttu-id="aaf68-107">Per lo scripting, ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="aaf68-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf68-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaf68-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="aaf68-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aaf68-109">Property value</span></span>

<span data-ttu-id="aaf68-110">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="aaf68-110">The identifier for the trigger.</span></span> <span data-ttu-id="aaf68-111">Questo identificatore viene utilizzato dal Utilità di pianificazione a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="aaf68-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf68-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaf68-112">Remarks</span></span>

<span data-ttu-id="aaf68-113">Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore del trigger viene specificato nell'attributo ID dei singoli elementi trigger (ad esempio, l'attributo ID dell'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="aaf68-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf68-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaf68-114">Requirements</span></span>



| <span data-ttu-id="aaf68-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaf68-115">Requirement</span></span> | <span data-ttu-id="aaf68-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aaf68-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf68-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaf68-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf68-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaf68-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aaf68-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaf68-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf68-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aaf68-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aaf68-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="aaf68-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="aaf68-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aaf68-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aaf68-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aaf68-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaf68-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaf68-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf68-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaf68-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf68-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="aaf68-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





