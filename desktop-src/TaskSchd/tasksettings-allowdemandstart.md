---
title: Proprietà TaskSettings. AllowDemandStart
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Utilità di pianificazione proprietà AllowDemandStart
- Utilità di pianificazione proprietà AllowDemandStart, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400340"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="9fedc-106">Proprietà TaskSettings. AllowDemandStart</span><span class="sxs-lookup"><span data-stu-id="9fedc-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="9fedc-107">Per gli script, ottiene o imposta un valore booleano che indica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="9fedc-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="9fedc-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9fedc-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fedc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fedc-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9fedc-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9fedc-110">Property value</span></span>

<span data-ttu-id="9fedc-111">Se true, l'attività può essere eseguita tramite il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="9fedc-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="9fedc-112">Se false, l'attività non può essere eseguita con il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="9fedc-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="9fedc-113">Il valore predefinito è True.</span><span class="sxs-lookup"><span data-stu-id="9fedc-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fedc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fedc-114">Remarks</span></span>

<span data-ttu-id="9fedc-115">Quando questa proprietà è impostata su true, l'attività può essere avviata indipendentemente dall'avvio dell'attività da parte dei trigger.</span><span class="sxs-lookup"><span data-stu-id="9fedc-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="9fedc-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="9fedc-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fedc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fedc-117">Requirements</span></span>



| <span data-ttu-id="9fedc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fedc-118">Requirement</span></span> | <span data-ttu-id="9fedc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9fedc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fedc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fedc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fedc-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fedc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9fedc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fedc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fedc-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fedc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fedc-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9fedc-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fedc-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9fedc-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9fedc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9fedc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fedc-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fedc-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fedc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fedc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fedc-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9fedc-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





