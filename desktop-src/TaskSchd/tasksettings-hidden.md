---
title: Proprietà TaskSettings. Hidden
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Utilità di pianificazione proprietà nascosta
- Utilità di pianificazione proprietà nascosta, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742738"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="626b8-106">Proprietà TaskSettings. Hidden</span><span class="sxs-lookup"><span data-stu-id="626b8-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="626b8-107">Per gli script, ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="626b8-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="626b8-108">Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "Master switch" che rende visibili tutte le attività nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="626b8-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="626b8-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="626b8-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="626b8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="626b8-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="626b8-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="626b8-111">Property value</span></span>

<span data-ttu-id="626b8-112">Se **true**, il valore indica che l'attività non sarà visibile nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="626b8-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="626b8-113">Se **false**, l'attività sarà visibile nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="626b8-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="626b8-114">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="626b8-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="626b8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="626b8-115">Remarks</span></span>

<span data-ttu-id="626b8-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="626b8-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="626b8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="626b8-117">Requirements</span></span>



| <span data-ttu-id="626b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="626b8-118">Requirement</span></span> | <span data-ttu-id="626b8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="626b8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="626b8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="626b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="626b8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="626b8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="626b8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="626b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="626b8-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="626b8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="626b8-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="626b8-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="626b8-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="626b8-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="626b8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="626b8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626b8-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="626b8-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="626b8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="626b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626b8-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="626b8-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





