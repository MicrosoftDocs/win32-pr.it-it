---
title: Oggetto TaskDefinition
description: Oggetto di scripting che definisce tutti i componenti di un'attività, ad esempio le impostazioni di attività, i trigger, le azioni e le informazioni di registrazione.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Utilità di pianificazione oggetto TaskDefinition
- Oggetto TaskDefinition Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518076"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="35a42-105">Oggetto TaskDefinition</span><span class="sxs-lookup"><span data-stu-id="35a42-105">TaskDefinition object</span></span>

<span data-ttu-id="35a42-106">Oggetto di scripting che definisce tutti i componenti di un'attività, ad esempio le impostazioni di attività, i trigger, le azioni e le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="35a42-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="35a42-107">Membri</span><span class="sxs-lookup"><span data-stu-id="35a42-107">Members</span></span>

<span data-ttu-id="35a42-108">L'oggetto **TaskDefinition** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35a42-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="35a42-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35a42-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35a42-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35a42-110">Properties</span></span>

<span data-ttu-id="35a42-111">L'oggetto **TaskDefinition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="35a42-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="35a42-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35a42-112">Property</span></span>                                                               | <span data-ttu-id="35a42-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="35a42-113">Access type</span></span>           | <span data-ttu-id="35a42-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35a42-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35a42-115">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="35a42-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="35a42-116">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-116">Read/write</span></span><br/> | <span data-ttu-id="35a42-117">Ottiene o imposta una raccolta di azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="35a42-118">**Data**</span><span class="sxs-lookup"><span data-stu-id="35a42-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="35a42-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-119">Read/write</span></span><br/> | <span data-ttu-id="35a42-120">Ottiene o imposta i dati associati all'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="35a42-121">Questi dati vengono ignorati dal servizio Utilità di pianificazione, ma vengono utilizzati da terze parti che desiderano estendere il formato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="35a42-122">**Principale**</span><span class="sxs-lookup"><span data-stu-id="35a42-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="35a42-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-123">Read/write</span></span><br/> | <span data-ttu-id="35a42-124">Ottiene o imposta l'entità per l'attività che fornisce le credenziali di sicurezza per l'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="35a42-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="35a42-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="35a42-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-126">Read/write</span></span><br/> | <span data-ttu-id="35a42-127">Ottiene o imposta le informazioni di registrazione utilizzate per descrivere un'attività, ad esempio la descrizione dell'attività, l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="35a42-128">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="35a42-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="35a42-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-129">Read/write</span></span><br/> | <span data-ttu-id="35a42-130">Ottiene o imposta le impostazioni che definiscono il modo in cui il servizio Utilità di pianificazione esegue l'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="35a42-131">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="35a42-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="35a42-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-132">Read/write</span></span><br/> | <span data-ttu-id="35a42-133">Ottiene o imposta una raccolta di trigger utilizzati per avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="35a42-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="35a42-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="35a42-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35a42-135">Read/write</span></span><br/> | <span data-ttu-id="35a42-136">Ottiene o imposta la definizione in formato XML dell'attività.</span><span class="sxs-lookup"><span data-stu-id="35a42-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="35a42-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a42-137">Remarks</span></span>

<span data-ttu-id="35a42-138">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata una definizione di attività usando l'elemento [**Task**](taskschedulerschema-task-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="35a42-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="35a42-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="35a42-139">Examples</span></span>

<span data-ttu-id="35a42-140">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md) , esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="35a42-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35a42-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a42-141">Requirements</span></span>



| <span data-ttu-id="35a42-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a42-142">Requirement</span></span> | <span data-ttu-id="35a42-143">Valore</span><span class="sxs-lookup"><span data-stu-id="35a42-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a42-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a42-144">Minimum supported client</span></span><br/> | <span data-ttu-id="35a42-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35a42-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35a42-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a42-146">Minimum supported server</span></span><br/> | <span data-ttu-id="35a42-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35a42-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35a42-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="35a42-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="35a42-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35a42-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35a42-150">DLL</span><span class="sxs-lookup"><span data-stu-id="35a42-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a42-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a42-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





