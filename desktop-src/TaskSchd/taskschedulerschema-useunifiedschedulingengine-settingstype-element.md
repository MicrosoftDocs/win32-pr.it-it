---
title: Elemento UseUnifiedSchedulingEngine (settingsType)
description: Specifica che verrà utilizzato il motore di pianificazione unificato per eseguire questa attività.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Utilità di pianificazione elemento UseUnifiedSchedulingEngine
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048148"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="10d0b-104">Elemento UseUnifiedSchedulingEngine (settingsType)</span><span class="sxs-lookup"><span data-stu-id="10d0b-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="10d0b-105">Specifica che verrà utilizzato il motore di pianificazione unificato per eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="10d0b-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="10d0b-106">L'elemento **UseUnifiedSchedulingEngine** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="10d0b-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="10d0b-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="10d0b-107">Parent element</span></span>



| <span data-ttu-id="10d0b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="10d0b-108">Element</span></span>                                                           | <span data-ttu-id="10d0b-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="10d0b-109">Derived from</span></span>                                                         | <span data-ttu-id="10d0b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10d0b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="10d0b-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="10d0b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="10d0b-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="10d0b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="10d0b-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="10d0b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="10d0b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="10d0b-114">Remarks</span></span>

<span data-ttu-id="10d0b-115">L'impostazione predefinita per questo elemento è false.</span><span class="sxs-lookup"><span data-stu-id="10d0b-115">The default setting for this element is False.</span></span>

<span data-ttu-id="10d0b-116">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings2:: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .</span><span class="sxs-lookup"><span data-stu-id="10d0b-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="10d0b-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="10d0b-117">Examples</span></span>

<span data-ttu-id="10d0b-118">Nel codice XML seguente viene definito un elemento Settings che specifica che verrà utilizzato il motore di pianificazione unificato per eseguire questa attività.</span><span class="sxs-lookup"><span data-stu-id="10d0b-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="10d0b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10d0b-119">Requirements</span></span>



| <span data-ttu-id="10d0b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d0b-120">Requirement</span></span> | <span data-ttu-id="10d0b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="10d0b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="10d0b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10d0b-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10d0b-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="10d0b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10d0b-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="10d0b-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10d0b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10d0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d0b-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="10d0b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





