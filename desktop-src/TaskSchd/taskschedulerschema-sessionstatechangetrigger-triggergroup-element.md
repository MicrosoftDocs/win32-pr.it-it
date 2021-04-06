---
title: Elemento SessionStateChangeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Utilità di pianificazione elemento SessionStateChangeTrigger
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742754"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="f979f-104">Elemento SessionStateChangeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="f979f-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="f979f-105">Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="f979f-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="f979f-106">L'elemento **SessionStateChangeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="f979f-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f979f-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f979f-107">Parent element</span></span>



| <span data-ttu-id="f979f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f979f-108">Element</span></span>                                                           | <span data-ttu-id="f979f-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="f979f-109">Derived from</span></span>                                                         | <span data-ttu-id="f979f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f979f-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f979f-111">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="f979f-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="f979f-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="f979f-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="f979f-113">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="f979f-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f979f-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f979f-114">Child elements</span></span>



| <span data-ttu-id="f979f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f979f-115">Element</span></span>                                                                                      | <span data-ttu-id="f979f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="f979f-116">Type</span></span>                                                                                    | <span data-ttu-id="f979f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f979f-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f979f-118">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="f979f-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="f979f-119">duration</span><span class="sxs-lookup"><span data-stu-id="f979f-119">duration</span></span>                                                                                | <span data-ttu-id="f979f-120">Specifica un valore che indica la lunghezza del ritardo prima che un'attività venga avviata quando viene rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="f979f-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="f979f-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="f979f-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="f979f-122">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="f979f-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="f979f-123">Specifica il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.</span><span class="sxs-lookup"><span data-stu-id="f979f-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="f979f-124">**UserId**</span><span class="sxs-lookup"><span data-stu-id="f979f-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="f979f-125">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f979f-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="f979f-126">Specifica l'utente per la sessione di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="f979f-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="f979f-127">Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.</span><span class="sxs-lookup"><span data-stu-id="f979f-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="f979f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f979f-128">Remarks</span></span>

<span data-ttu-id="f979f-129">Per lo sviluppo di script, viene specificato un trigger di modifica dello stato della sessione utilizzando l'oggetto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f979f-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="f979f-130">Per lo sviluppo in C++, un trigger di modifica dello stato della sessione viene specificato tramite l'interfaccia [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .</span><span class="sxs-lookup"><span data-stu-id="f979f-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f979f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f979f-131">Requirements</span></span>



| <span data-ttu-id="f979f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f979f-132">Requirement</span></span> | <span data-ttu-id="f979f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f979f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f979f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f979f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f979f-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f979f-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f979f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f979f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f979f-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f979f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





