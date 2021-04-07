---
title: Elemento AllowStartOnDemand (settingsType)
description: Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Utilità di pianificazione elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963917"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="1dbf3-104">Elemento AllowStartOnDemand (settingsType)</span><span class="sxs-lookup"><span data-stu-id="1dbf3-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="1dbf3-105">Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="1dbf3-106">L'elemento **AllowStartOnDemand** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1dbf3-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1dbf3-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1dbf3-107">Parent element</span></span>



| <span data-ttu-id="1dbf3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1dbf3-108">Element</span></span>                                                           | <span data-ttu-id="1dbf3-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1dbf3-109">Derived from</span></span>                                                         | <span data-ttu-id="1dbf3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dbf3-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dbf3-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="1dbf3-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1dbf3-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="1dbf3-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1dbf3-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1dbf3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dbf3-114">Remarks</span></span>

<span data-ttu-id="1dbf3-115">Quando questo elemento è impostato su true, l'attività può essere avviata indipendentemente dall'avvio dell'attività da parte dei trigger.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="1dbf3-116">Per lo sviluppo in C++, vedere la [**Proprietà AllowDemandStart di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="1dbf3-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="1dbf3-117">Per lo sviluppo di script, vedere [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="1dbf3-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1dbf3-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1dbf3-118">Examples</span></span>

<span data-ttu-id="1dbf3-119">Per un esempio completo del codice XML per un'attività che consente l'avvio della richiesta, vedere l' [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1dbf3-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dbf3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dbf3-120">Requirements</span></span>



| <span data-ttu-id="1dbf3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dbf3-121">Requirement</span></span> | <span data-ttu-id="1dbf3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1dbf3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1dbf3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dbf3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1dbf3-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dbf3-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1dbf3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dbf3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1dbf3-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1dbf3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1dbf3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dbf3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbf3-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1dbf3-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





