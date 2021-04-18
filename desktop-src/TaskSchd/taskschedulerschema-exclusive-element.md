---
title: Elemento Exclusive
description: Indica se l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elemento esclusivo Utilità di pianificazione
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301152"
---
# <a name="exclusive-element"></a><span data-ttu-id="4945e-104">Elemento Exclusive</span><span class="sxs-lookup"><span data-stu-id="4945e-104">Exclusive Element</span></span>

<span data-ttu-id="4945e-105">Indica se l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="4945e-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="4945e-106">L'esclusività è garantita solo tra altre attività di manutenzione e non concede alcuna priorità di ordinamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4945e-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="4945e-107">Se l'esclusività non è specificata, l'attività viene avviata in parallelo con altre attività di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="4945e-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="4945e-108">L'elemento **Exclusive** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4945e-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4945e-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4945e-109">Parent element</span></span>



| <span data-ttu-id="4945e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="4945e-110">Element</span></span>                                                                                                                          | <span data-ttu-id="4945e-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4945e-111">Derived from</span></span>                                                                               | <span data-ttu-id="4945e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4945e-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4945e-113">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="4945e-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="4945e-114">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="4945e-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="4945e-115">Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="4945e-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4945e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4945e-116">Remarks</span></span>

<span data-ttu-id="4945e-117">Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .</span><span class="sxs-lookup"><span data-stu-id="4945e-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="4945e-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="4945e-118">Examples</span></span>

<span data-ttu-id="4945e-119">Il codice XML seguente definisce l'attività di manutenzione con requisito di scadenza impostato su 15 giorni.</span><span class="sxs-lookup"><span data-stu-id="4945e-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="4945e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4945e-120">Requirements</span></span>



| <span data-ttu-id="4945e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4945e-121">Requirement</span></span> | <span data-ttu-id="4945e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4945e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4945e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4945e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4945e-124">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4945e-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="4945e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4945e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4945e-126">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4945e-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4945e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4945e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4945e-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4945e-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4945e-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4945e-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





