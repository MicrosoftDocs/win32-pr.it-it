---
title: Proprietà TaskSettings. StopIfGoingOnBatteries
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Utilità di pianificazione proprietà StopIfGoingOnBatteries
- Utilità di pianificazione proprietà StopIfGoingOnBatteries, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478353"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="3b700-106">Proprietà TaskSettings. StopIfGoingOnBatteries</span><span class="sxs-lookup"><span data-stu-id="3b700-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="3b700-107">Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="3b700-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="3b700-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3b700-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b700-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b700-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3b700-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3b700-110">Property value</span></span>

<span data-ttu-id="3b700-111">Valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="3b700-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3b700-112">Se true, la proprietà indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="3b700-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3b700-113">Se false, la proprietà indica che l'attività non verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="3b700-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="3b700-114">Il valore predefinito è True.</span><span class="sxs-lookup"><span data-stu-id="3b700-114">The default is True.</span></span> <span data-ttu-id="3b700-115">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3b700-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b700-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b700-116">Remarks</span></span>

<span data-ttu-id="3b700-117">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3b700-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b700-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b700-118">Requirements</span></span>



| <span data-ttu-id="3b700-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b700-119">Requirement</span></span> | <span data-ttu-id="3b700-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3b700-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b700-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b700-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b700-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b700-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3b700-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b700-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b700-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b700-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b700-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3b700-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b700-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b700-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b700-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b700-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b700-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b700-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b700-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b700-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b700-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3b700-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





