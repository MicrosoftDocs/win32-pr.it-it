---
title: Proprietà IdleSettings. RestartOnIdle
description: Per gli script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre una condizione di inattività più di una volta.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Utilità di pianificazione proprietà RestartOnIdle
- Utilità di pianificazione proprietà RestartOnIdle, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301782"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="5e8c1-106">Proprietà IdleSettings. RestartOnIdle</span><span class="sxs-lookup"><span data-stu-id="5e8c1-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="5e8c1-107">Per gli script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre una condizione di inattività più di una volta.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8c1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e8c1-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5e8c1-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5e8c1-109">Property value</span></span>

<span data-ttu-id="5e8c1-110">Valore booleano che indica se l'attività deve essere riavviata quando il computer scorre in una condizione di inattività più di una volta.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="5e8c1-111">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8c1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e8c1-112">Remarks</span></span>

<span data-ttu-id="5e8c1-113">Questa proprietà viene utilizzata solo se la proprietà [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="5e8c1-114">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e8c1-115">Requirements</span></span>



| <span data-ttu-id="5e8c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e8c1-116">Requirement</span></span> | <span data-ttu-id="5e8c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5e8c1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8c1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e8c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8c1-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e8c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5e8c1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e8c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8c1-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e8c1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e8c1-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5e8c1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e8c1-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e8c1-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e8c1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5e8c1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e8c1-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e8c1-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e8c1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e8c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8c1-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5e8c1-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5e8c1-128">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="5e8c1-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





