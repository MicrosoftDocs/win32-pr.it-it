---
title: Oggetto RepetitionPattern
description: Oggetto di script che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- trigger Utilità di pianificazione, oggetto modello di ripetizione
- modello di ripetizione Utilità di pianificazione, oggetto
- Utilità di pianificazione oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475976"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="570f2-107">Oggetto RepetitionPattern</span><span class="sxs-lookup"><span data-stu-id="570f2-107">RepetitionPattern object</span></span>

<span data-ttu-id="570f2-108">Oggetto di script che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="570f2-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="570f2-109">Membri</span><span class="sxs-lookup"><span data-stu-id="570f2-109">Members</span></span>

<span data-ttu-id="570f2-110">L'oggetto **RepetitionPattern** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="570f2-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="570f2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="570f2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="570f2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="570f2-112">Properties</span></span>

<span data-ttu-id="570f2-113">L'oggetto **RepetitionPattern** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="570f2-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="570f2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="570f2-114">Property</span></span>                                                                    | <span data-ttu-id="570f2-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="570f2-115">Access type</span></span>           | <span data-ttu-id="570f2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="570f2-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="570f2-117">**Duration**</span><span class="sxs-lookup"><span data-stu-id="570f2-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="570f2-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="570f2-118">Read/write</span></span><br/> | <span data-ttu-id="570f2-119">Ottiene o imposta il tempo di ripetizione del pattern.</span><span class="sxs-lookup"><span data-stu-id="570f2-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="570f2-120">**Interval**</span><span class="sxs-lookup"><span data-stu-id="570f2-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="570f2-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="570f2-121">Read/write</span></span><br/> | <span data-ttu-id="570f2-122">Ottiene o imposta la quantità di tempo che intercorre tra il riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="570f2-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="570f2-123">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="570f2-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="570f2-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="570f2-124">Read/write</span></span><br/> | <span data-ttu-id="570f2-125">Ottiene o imposta un valore booleano che indica se un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del criterio di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="570f2-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="570f2-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="570f2-126">Remarks</span></span>

<span data-ttu-id="570f2-127">Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="570f2-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="570f2-128">Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte.</span><span class="sxs-lookup"><span data-stu-id="570f2-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="570f2-129">Le cinque ripetizioni possono essere definite dal modello seguente.</span><span class="sxs-lookup"><span data-stu-id="570f2-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="570f2-130">Un'attività viene avviata all'inizio del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="570f2-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="570f2-131">L'attività successiva inizia alla fine del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="570f2-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="570f2-132">L'attività successiva inizia alla fine del secondo minuto.</span><span class="sxs-lookup"><span data-stu-id="570f2-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="570f2-133">L'attività successiva inizia alla fine del terzo minuto.</span><span class="sxs-lookup"><span data-stu-id="570f2-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="570f2-134">L'attività successiva inizia alla fine del quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="570f2-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="570f2-135">**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.</span><span class="sxs-lookup"><span data-stu-id="570f2-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="570f2-136">Durante la lettura o la scrittura di codice XML per un'attività, il modello di ripetizione viene specificato utilizzando l'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema di utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="570f2-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="570f2-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="570f2-137">Examples</span></span>

<span data-ttu-id="570f2-138">Per ulteriori informazioni e codice di esempio per questa proprietà, vedere [esempio di trigger giornalieri (scripting)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="570f2-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="570f2-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="570f2-139">Requirements</span></span>



| <span data-ttu-id="570f2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="570f2-140">Requirement</span></span> | <span data-ttu-id="570f2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="570f2-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="570f2-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570f2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="570f2-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="570f2-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="570f2-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570f2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="570f2-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="570f2-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="570f2-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="570f2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="570f2-147"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="570f2-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="570f2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="570f2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="570f2-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="570f2-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="570f2-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="570f2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570f2-151">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="570f2-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="570f2-152">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="570f2-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





