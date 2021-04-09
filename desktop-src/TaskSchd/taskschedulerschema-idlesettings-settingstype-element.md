---
title: Elemento IdleSettings (settingsType)
description: Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Utilità di pianificazione elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120798"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="e1b31-104">Elemento IdleSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="e1b31-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="e1b31-105">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="e1b31-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="e1b31-106">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="e1b31-107">L'elemento **IdleSettings** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b31-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e1b31-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e1b31-108">Parent element</span></span>

| <span data-ttu-id="e1b31-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1b31-109">Element</span></span>                                                           | <span data-ttu-id="e1b31-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e1b31-110">Derived from</span></span>                                                         | <span data-ttu-id="e1b31-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1b31-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1b31-112">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="e1b31-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e1b31-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e1b31-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e1b31-114">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="e1b31-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e1b31-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="e1b31-116">Le impostazioni *Duration* e *WaitTimeout* sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="e1b31-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="e1b31-117">Sono ancora presenti nel Utilità di pianificazione interfaccia utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.</span><span class="sxs-lookup"><span data-stu-id="e1b31-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="e1b31-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1b31-118">Element</span></span>                                                                                  | <span data-ttu-id="e1b31-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1b31-119">Type</span></span>     | <span data-ttu-id="e1b31-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1b31-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1b31-121">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="e1b31-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="e1b31-122">boolean</span><span class="sxs-lookup"><span data-stu-id="e1b31-122">boolean</span></span>  | <span data-ttu-id="e1b31-123">Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.</span><span class="sxs-lookup"><span data-stu-id="e1b31-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="e1b31-124">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="e1b31-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="e1b31-125">boolean</span><span class="sxs-lookup"><span data-stu-id="e1b31-125">boolean</span></span>  | <span data-ttu-id="e1b31-126">Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="e1b31-127">**Deprecato**: [ **durata**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="e1b31-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="e1b31-128">duration</span><span class="sxs-lookup"><span data-stu-id="e1b31-128">duration</span></span> | <span data-ttu-id="e1b31-129">Specifica per quanto tempo il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="e1b31-130">**Deprecato**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="e1b31-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="e1b31-131">duration</span><span class="sxs-lookup"><span data-stu-id="e1b31-131">duration</span></span> | <span data-ttu-id="e1b31-132">Specifica la quantità di tempo per cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="e1b31-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1b31-133">Remarks</span></span>

<span data-ttu-id="e1b31-134">Per lo sviluppo di script, le impostazioni di inattività vengono specificate utilizzando la proprietà [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b31-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="e1b31-135">Per lo sviluppo in C++, le impostazioni di inattività vengono specificate usando la proprietà [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .</span><span class="sxs-lookup"><span data-stu-id="e1b31-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e1b31-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="e1b31-136">Examples</span></span>

<span data-ttu-id="e1b31-137">Il codice XML seguente definisce un elemento Settings che consente Utilità di pianificazione di attendere 24 ore per una condizione di inattività e quindi consente solo 10 minuti {IdleDuration) di avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="e1b31-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="e1b31-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1b31-138">Requirements</span></span>

| <span data-ttu-id="e1b31-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b31-139">Requirement</span></span> | <span data-ttu-id="e1b31-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e1b31-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1b31-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b31-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b31-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1b31-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1b31-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b31-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b31-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e1b31-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="e1b31-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1b31-145">See also</span></span>

[<span data-ttu-id="e1b31-146">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e1b31-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="e1b31-147">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e1b31-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
