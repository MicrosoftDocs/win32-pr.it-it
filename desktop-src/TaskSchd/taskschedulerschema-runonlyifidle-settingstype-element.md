---
title: Elemento RunOnlyIfIdle (settingsType)
description: Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Utilità di pianificazione elemento RunOnlyIfIdle
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048625"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="77985-104">Elemento RunOnlyIfIdle (settingsType)</span><span class="sxs-lookup"><span data-stu-id="77985-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="77985-105">Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="77985-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="77985-106">L'elemento **RunOnlyIfIdle** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="77985-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="77985-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="77985-107">Parent element</span></span>



| <span data-ttu-id="77985-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="77985-108">Element</span></span>                                                           | <span data-ttu-id="77985-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="77985-109">Derived from</span></span>                                                         | <span data-ttu-id="77985-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77985-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="77985-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="77985-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="77985-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="77985-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="77985-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="77985-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77985-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="77985-114">Remarks</span></span>

<span data-ttu-id="77985-115">Per lo sviluppo in C++, vedere [**la proprietà RunOnlyIfIdle di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="77985-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="77985-116">Per lo sviluppo di script, vedere [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="77985-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77985-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77985-117">Requirements</span></span>



| <span data-ttu-id="77985-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="77985-118">Requirement</span></span> | <span data-ttu-id="77985-119">Valore</span><span class="sxs-lookup"><span data-stu-id="77985-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77985-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77985-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77985-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77985-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77985-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77985-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77985-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77985-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77985-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77985-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77985-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="77985-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="77985-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="77985-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





