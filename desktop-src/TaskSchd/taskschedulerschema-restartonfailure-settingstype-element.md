---
title: Elemento RestartOnFailure (settingsType)
description: Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Utilità di pianificazione elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225242"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="c124e-104">Elemento RestartOnFailure (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c124e-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="c124e-105">Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="c124e-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="c124e-106">L'elemento **RestartOnFailure** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c124e-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c124e-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c124e-107">Parent element</span></span>



| <span data-ttu-id="c124e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c124e-108">Element</span></span>                                                           | <span data-ttu-id="c124e-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="c124e-109">Derived from</span></span>                                                         | <span data-ttu-id="c124e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c124e-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c124e-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="c124e-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c124e-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c124e-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c124e-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="c124e-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c124e-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c124e-114">Child elements</span></span>



| <span data-ttu-id="c124e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c124e-115">Element</span></span>                                                              | <span data-ttu-id="c124e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c124e-116">Type</span></span>         | <span data-ttu-id="c124e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c124e-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c124e-118">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="c124e-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="c124e-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c124e-119">unsignedByte</span></span> | <span data-ttu-id="c124e-120">Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="c124e-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="c124e-121">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c124e-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="c124e-122">duration</span><span class="sxs-lookup"><span data-stu-id="c124e-122">duration</span></span>     | <span data-ttu-id="c124e-123">Specifica il periodo di tempo durante il quale il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="c124e-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="c124e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c124e-124">Remarks</span></span>

<span data-ttu-id="c124e-125">Quando un'applicazione specifica le impostazioni delle attività, queste informazioni sono accessibili tramite le proprietà [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) e [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) dell'interfaccia [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) .</span><span class="sxs-lookup"><span data-stu-id="c124e-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="c124e-126">Per gli script, è possibile accedere a queste informazioni tramite le proprietà [**TaskSettings. RestartCount**](tasksettings-restartcount.md) e [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="c124e-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="c124e-127">È necessario impostare entrambi gli elementi figlio per specificare il modo in cui il Utilità di pianificazione riavvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="c124e-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="c124e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c124e-128">Requirements</span></span>



| <span data-ttu-id="c124e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c124e-129">Requirement</span></span> | <span data-ttu-id="c124e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c124e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c124e-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c124e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c124e-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c124e-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c124e-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c124e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c124e-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c124e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c124e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c124e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c124e-136">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c124e-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





