---
title: Proprietà TaskSettings. RunOnlyIfNetworkAvailable
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Utilità di pianificazione proprietà RunOnlyIfNetworkAvailable
- Utilità di pianificazione proprietà RunOnlyIfNetworkAvailable, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874289"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="369ab-106">Proprietà TaskSettings. RunOnlyIfNetworkAvailable</span><span class="sxs-lookup"><span data-stu-id="369ab-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="369ab-107">Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="369ab-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="369ab-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="369ab-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="369ab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="369ab-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="369ab-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="369ab-110">Property value</span></span>

<span data-ttu-id="369ab-111">Se true, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="369ab-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="369ab-112">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="369ab-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="369ab-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="369ab-113">Remarks</span></span>

<span data-ttu-id="369ab-114">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="369ab-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="369ab-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="369ab-115">Requirements</span></span>



| <span data-ttu-id="369ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="369ab-116">Requirement</span></span> | <span data-ttu-id="369ab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="369ab-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="369ab-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="369ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="369ab-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="369ab-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="369ab-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="369ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="369ab-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="369ab-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="369ab-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="369ab-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="369ab-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="369ab-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="369ab-124">DLL</span><span class="sxs-lookup"><span data-stu-id="369ab-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369ab-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="369ab-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="369ab-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="369ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369ab-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="369ab-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





