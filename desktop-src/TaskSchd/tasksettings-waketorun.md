---
title: Proprietà TaskSettings. WakeToRun
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Utilità di pianificazione proprietà WakeToRun
- Utilità di pianificazione proprietà WakeToRun, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740802"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="638d8-106">Proprietà TaskSettings. WakeToRun</span><span class="sxs-lookup"><span data-stu-id="638d8-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="638d8-107">Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="638d8-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="638d8-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="638d8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="638d8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="638d8-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="638d8-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="638d8-110">Property value</span></span>

<span data-ttu-id="638d8-111">Se true, la proprietà indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="638d8-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="638d8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="638d8-112">Remarks</span></span>

<span data-ttu-id="638d8-113">Quando il servizio Utilità di pianificazione riattiva il computer per eseguire un'attività, è possibile che lo schermo rimanga disattivato anche se il computer non è più in modalità di sospensione o di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="638d8-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="638d8-114">La schermata viene accesa quando Windows Vista rileva che un utente ha restituito l'utilizzo del computer.</span><span class="sxs-lookup"><span data-stu-id="638d8-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="638d8-115">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="638d8-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="638d8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="638d8-116">Requirements</span></span>



| <span data-ttu-id="638d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="638d8-117">Requirement</span></span> | <span data-ttu-id="638d8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="638d8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="638d8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="638d8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="638d8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="638d8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="638d8-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="638d8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="638d8-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="638d8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="638d8-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="638d8-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="638d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="638d8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="638d8-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="638d8-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638d8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="638d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638d8-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="638d8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





