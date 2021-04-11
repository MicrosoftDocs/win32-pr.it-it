---
title: Proprietà TaskSettings. DisallowStartIfOnBatteries
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Utilità di pianificazione proprietà DisallowStartIfOnBatteries
- Utilità di pianificazione proprietà DisallowStartIfOnBatteries, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120882"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="744a1-106">Proprietà TaskSettings. DisallowStartIfOnBatteries</span><span class="sxs-lookup"><span data-stu-id="744a1-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="744a1-107">Per gli script, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="744a1-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="744a1-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="744a1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="744a1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="744a1-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="744a1-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="744a1-110">Property value</span></span>

<span data-ttu-id="744a1-111">Valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="744a1-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="744a1-112">Se true, l'attività non verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="744a1-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="744a1-113">Se false, l'attività verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="744a1-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="744a1-114">Il valore predefinito è True.</span><span class="sxs-lookup"><span data-stu-id="744a1-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="744a1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="744a1-115">Remarks</span></span>

<span data-ttu-id="744a1-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="744a1-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="744a1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="744a1-117">Requirements</span></span>



| <span data-ttu-id="744a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="744a1-118">Requirement</span></span> | <span data-ttu-id="744a1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="744a1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="744a1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="744a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="744a1-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="744a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="744a1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="744a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="744a1-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="744a1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="744a1-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="744a1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="744a1-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="744a1-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="744a1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="744a1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="744a1-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="744a1-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744a1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="744a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744a1-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="744a1-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





