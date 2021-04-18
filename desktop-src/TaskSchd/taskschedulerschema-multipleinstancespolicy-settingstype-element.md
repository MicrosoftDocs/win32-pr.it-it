---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Utilità di pianificazione elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301906"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="6e851-104">Elemento MultipleInstancesPolicy (settingsType)</span><span class="sxs-lookup"><span data-stu-id="6e851-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="6e851-105">Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6e851-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="6e851-106">L'elemento **MultipleInstancesPolicy** è definito dal tipo semplice [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="6e851-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6e851-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6e851-107">Parent element</span></span>



| <span data-ttu-id="6e851-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6e851-108">Element</span></span>                                                           | <span data-ttu-id="6e851-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="6e851-109">Derived from</span></span>                                                         | <span data-ttu-id="6e851-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e851-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e851-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6e851-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6e851-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="6e851-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6e851-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="6e851-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6e851-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e851-114">Remarks</span></span>

<span data-ttu-id="6e851-115">Per lo sviluppo in C++, vedere [**la proprietà MultipleInstances di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="6e851-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="6e851-116">Per lo sviluppo di script, vedere [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="6e851-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="6e851-117">Valori con restrizioni</span><span class="sxs-lookup"><span data-stu-id="6e851-117">Restricted Values</span></span>

<span data-ttu-id="6e851-118">Questo elemento è limitato ai valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e851-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="6e851-119">Parallel: avvia una nuova istanza mentre è in esecuzione un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="6e851-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="6e851-120">Queue: avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6e851-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="6e851-121">IgnoreNew: valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6e851-121">IgnoreNew: Default.</span></span> <span data-ttu-id="6e851-122">Non avvia una nuova istanza di se è in esecuzione un'istanza esistente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6e851-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="6e851-123">StopExisting: arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="6e851-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="6e851-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="6e851-124">Examples</span></span>

<span data-ttu-id="6e851-125">Nel codice XML seguente viene definito un elemento Settings che consente l'esecuzione in parallelo di più istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6e851-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="6e851-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e851-126">Requirements</span></span>



| <span data-ttu-id="6e851-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e851-127">Requirement</span></span> | <span data-ttu-id="6e851-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6e851-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e851-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e851-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6e851-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e851-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e851-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e851-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6e851-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e851-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e851-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e851-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e851-134">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6e851-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





