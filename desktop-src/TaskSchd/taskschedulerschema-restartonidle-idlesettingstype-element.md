---
title: Elemento RestartOnIdle (idleSettingsType)
description: Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Utilità di pianificazione elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302684"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="ff22d-104">Elemento RestartOnIdle (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="ff22d-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="ff22d-105">Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.</span><span class="sxs-lookup"><span data-stu-id="ff22d-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="ff22d-106">L'elemento **RestartOnIdle** è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ff22d-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ff22d-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ff22d-107">Parent element</span></span>



| <span data-ttu-id="ff22d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff22d-108">Element</span></span>                                                                       | <span data-ttu-id="ff22d-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="ff22d-109">Derived from</span></span>                                                                 | <span data-ttu-id="ff22d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff22d-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff22d-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="ff22d-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="ff22d-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ff22d-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="ff22d-113">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="ff22d-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ff22d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff22d-114">Remarks</span></span>

<span data-ttu-id="ff22d-115">Questo elemento viene utilizzato solo se l'elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="ff22d-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="ff22d-116">Per lo sviluppo di script, questa impostazione di attività viene specificata tramite la proprietà [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .</span><span class="sxs-lookup"><span data-stu-id="ff22d-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="ff22d-117">Per lo sviluppo in C++, questa impostazione di attività viene specificata tramite la proprietà [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .</span><span class="sxs-lookup"><span data-stu-id="ff22d-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ff22d-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff22d-118">Examples</span></span>

<span data-ttu-id="ff22d-119">Il codice XML seguente definisce un'impostazione inattiva che indica che l'attività non deve essere riavviata quando viene ciclita la condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="ff22d-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="ff22d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff22d-120">Requirements</span></span>



| <span data-ttu-id="ff22d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff22d-121">Requirement</span></span> | <span data-ttu-id="ff22d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ff22d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff22d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff22d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ff22d-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff22d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff22d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff22d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ff22d-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff22d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff22d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff22d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff22d-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ff22d-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ff22d-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ff22d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





