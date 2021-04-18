---
title: Elemento WakeToRun (settingsType)
description: Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Utilità di pianificazione elemento WakeToRun
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302486"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="4a375-104">Elemento WakeToRun (settingsType)</span><span class="sxs-lookup"><span data-stu-id="4a375-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="4a375-105">Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4a375-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="4a375-106">L'elemento **WakeToRun** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a375-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4a375-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4a375-107">Parent element</span></span>



| <span data-ttu-id="4a375-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a375-108">Element</span></span>                                                           | <span data-ttu-id="4a375-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4a375-109">Derived from</span></span>                                                         | <span data-ttu-id="4a375-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a375-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a375-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="4a375-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="4a375-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="4a375-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="4a375-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="4a375-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4a375-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a375-114">Remarks</span></span>

<span data-ttu-id="4a375-115">Quando il servizio Utilità di pianificazione riattiva il computer per eseguire un'attività, è possibile che lo schermo rimanga disattivato anche se il computer non è più in modalità di sospensione o di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="4a375-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="4a375-116">La schermata viene accesa quando Windows Vista rileva che un utente ha restituito l'utilizzo del computer.</span><span class="sxs-lookup"><span data-stu-id="4a375-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="4a375-117">Per lo sviluppo in C++, vedere [**la proprietà WakeToRun di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="4a375-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="4a375-118">Per lo sviluppo di script, vedere [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="4a375-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a375-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a375-119">Requirements</span></span>



| <span data-ttu-id="4a375-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a375-120">Requirement</span></span> | <span data-ttu-id="4a375-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4a375-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a375-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a375-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4a375-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a375-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a375-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a375-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4a375-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a375-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a375-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a375-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a375-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4a375-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4a375-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4a375-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





