---
title: Oggetto IdleSettings
description: Oggetto di scripting che specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Utilità di pianificazione oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400478"
---
# <a name="idlesettings-object"></a><span data-ttu-id="e3a74-105">Oggetto IdleSettings</span><span class="sxs-lookup"><span data-stu-id="e3a74-105">IdleSettings object</span></span>

<span data-ttu-id="e3a74-106">Oggetto di scripting che specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="e3a74-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="e3a74-107">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="e3a74-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="e3a74-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e3a74-108">Members</span></span>

<span data-ttu-id="e3a74-109">L'oggetto **IdleSettings** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3a74-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="e3a74-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3a74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3a74-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3a74-111">Properties</span></span>

<span data-ttu-id="e3a74-112">L'oggetto **IdleSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3a74-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="e3a74-113">Le impostazioni *IdleDuration* e *WaitTimeout* sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="e3a74-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="e3a74-114">Sono ancora presenti nel Utilità di pianificazione interfaccia utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.</span><span class="sxs-lookup"><span data-stu-id="e3a74-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="e3a74-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3a74-115">Property</span></span>                                                       | <span data-ttu-id="e3a74-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e3a74-116">Access type</span></span>           | <span data-ttu-id="e3a74-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a74-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3a74-118">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="e3a74-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="e3a74-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e3a74-119">Read/write</span></span><br/> | <span data-ttu-id="e3a74-120">Ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre in una condizione di inattività più di una volta.</span><span class="sxs-lookup"><span data-stu-id="e3a74-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="e3a74-121">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="e3a74-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="e3a74-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e3a74-122">Read/write</span></span><br/> | <span data-ttu-id="e3a74-123">Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e3a74-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="e3a74-124">**Deprecato**: [ **IdleDuration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="e3a74-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="e3a74-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e3a74-125">Read/write</span></span><br/> | <span data-ttu-id="e3a74-126">Ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve essere in uno stato inattivo prima dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e3a74-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="e3a74-127">**Deprecato**: [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="e3a74-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="e3a74-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e3a74-128">Read/write</span></span><br/> | <span data-ttu-id="e3a74-129">Ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="e3a74-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="e3a74-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a74-130">Remarks</span></span>

<span data-ttu-id="e3a74-131">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e3a74-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e3a74-132">Se un'attività viene attivata da un trigger inattivo, la proprietà [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="e3a74-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="e3a74-133">*IdleSettings. IdleDuration* e *IdleSettings. WaitTimeout* sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="e3a74-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a74-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a74-134">Requirements</span></span>

| <span data-ttu-id="e3a74-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a74-135">Requirement</span></span> | <span data-ttu-id="e3a74-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a74-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a74-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3a74-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a74-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3a74-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3a74-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3a74-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a74-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3a74-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3a74-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e3a74-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3a74-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3a74-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3a74-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a74-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a74-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a74-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e3a74-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a74-145">See also</span></span>

[<span data-ttu-id="e3a74-146">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e3a74-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="e3a74-147">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e3a74-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
