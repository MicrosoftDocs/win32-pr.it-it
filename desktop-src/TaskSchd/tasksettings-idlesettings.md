---
title: Proprietà TaskSettings. IdleSettings
description: Per gli script, ottiene o imposta le informazioni che specificano il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Utilità di pianificazione proprietà IdleSettings
- Utilità di pianificazione proprietà IdleSettings, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301995"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="26799-106">Proprietà TaskSettings. IdleSettings</span><span class="sxs-lookup"><span data-stu-id="26799-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="26799-107">Per gli script, ottiene o imposta le informazioni che specificano il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="26799-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="26799-108">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="26799-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="26799-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="26799-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="26799-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26799-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="26799-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="26799-111">Property value</span></span>

<span data-ttu-id="26799-112">Oggetto [**IdleSettings**](idlesettings.md) che specifica il modo in cui il utilità di pianificazione gestisce l'attività quando il computer entra in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="26799-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="26799-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="26799-113">Remarks</span></span>

<span data-ttu-id="26799-114">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="26799-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="26799-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26799-115">Requirements</span></span>



| <span data-ttu-id="26799-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="26799-116">Requirement</span></span> | <span data-ttu-id="26799-117">Valore</span><span class="sxs-lookup"><span data-stu-id="26799-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26799-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26799-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26799-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26799-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="26799-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26799-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26799-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26799-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26799-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="26799-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="26799-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26799-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26799-124">DLL</span><span class="sxs-lookup"><span data-stu-id="26799-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26799-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26799-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26799-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26799-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26799-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="26799-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





