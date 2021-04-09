---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Utilità di pianificazione elemento MaintenanceSettings
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120795"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="c3ff2-104">Elemento MaintenanceSettings (maintenanceSettingsType)</span><span class="sxs-lookup"><span data-stu-id="c3ff2-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="c3ff2-105">Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="c3ff2-106">L'elemento **MaintenanceSettings** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3ff2-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c3ff2-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c3ff2-107">Parent element</span></span>



| <span data-ttu-id="c3ff2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3ff2-108">Element</span></span>                                                           | <span data-ttu-id="c3ff2-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="c3ff2-109">Derived from</span></span>                                                         | <span data-ttu-id="c3ff2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3ff2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3ff2-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c3ff2-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c3ff2-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c3ff2-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c3ff2-114">Child elements</span></span>



| <span data-ttu-id="c3ff2-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3ff2-115">Element</span></span>                                                    | <span data-ttu-id="c3ff2-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3ff2-116">Type</span></span>    | <span data-ttu-id="c3ff2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3ff2-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3ff2-118">**Scadenza**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="c3ff2-119">Specifica il periodo di tempo dopo il quale l'utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="c3ff2-120">**Esclusivo**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="c3ff2-121">boolean</span><span class="sxs-lookup"><span data-stu-id="c3ff2-121">boolean</span></span> | <span data-ttu-id="c3ff2-122">Se è impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="c3ff2-123">**Periodo**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="c3ff2-124">Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="c3ff2-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3ff2-125">Remarks</span></span>

<span data-ttu-id="c3ff2-126">Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**ITaskSettings3:: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .</span><span class="sxs-lookup"><span data-stu-id="c3ff2-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c3ff2-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="c3ff2-127">Examples</span></span>

<span data-ttu-id="c3ff2-128">Nel codice XML seguente viene definito un elemento Settings che indica Utilità di pianificazione eseguire un'attività una volta in 5 giorni durante la manutenzione automatica normale e se non riesce per 15 giorni, avviare il tentativo di esecuzione dell'attività durante la manutenzione automatica di emergenza.</span><span class="sxs-lookup"><span data-stu-id="c3ff2-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="c3ff2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3ff2-129">Requirements</span></span>



| <span data-ttu-id="c3ff2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ff2-130">Requirement</span></span> | <span data-ttu-id="c3ff2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c3ff2-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3ff2-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3ff2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ff2-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c3ff2-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="c3ff2-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3ff2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ff2-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c3ff2-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3ff2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3ff2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ff2-137">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c3ff2-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c3ff2-138">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c3ff2-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





