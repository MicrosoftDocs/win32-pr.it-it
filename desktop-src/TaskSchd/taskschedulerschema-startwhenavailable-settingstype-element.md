---
title: Elemento StartWhenAvailable (settingsType)
description: Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Utilità di pianificazione elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963914"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="fc8b7-104">Elemento StartWhenAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="fc8b7-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="fc8b7-105">Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.</span><span class="sxs-lookup"><span data-stu-id="fc8b7-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="fc8b7-106">L'elemento **StartWhenAvailable** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fc8b7-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fc8b7-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="fc8b7-107">Parent element</span></span>



| <span data-ttu-id="fc8b7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fc8b7-108">Element</span></span>                                                           | <span data-ttu-id="fc8b7-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="fc8b7-109">Derived from</span></span>                                                         | <span data-ttu-id="fc8b7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc8b7-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc8b7-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="fc8b7-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="fc8b7-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="fc8b7-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="fc8b7-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="fc8b7-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fc8b7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc8b7-114">Remarks</span></span>

<span data-ttu-id="fc8b7-115">Questa proprietà si applica solo alle attività temporizzate.</span><span class="sxs-lookup"><span data-stu-id="fc8b7-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="fc8b7-116">Per lo sviluppo in C++, vedere [**la proprietà StartWhenAvailable di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="fc8b7-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="fc8b7-117">Per lo sviluppo di script, vedere [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="fc8b7-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc8b7-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="fc8b7-118">Examples</span></span>

<span data-ttu-id="fc8b7-119">Nel codice XML seguente viene definito un elemento Settings che consente all'Utilità di pianificazione di avviare l'attività quando è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fc8b7-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="fc8b7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc8b7-120">Requirements</span></span>



| <span data-ttu-id="fc8b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8b7-121">Requirement</span></span> | <span data-ttu-id="fc8b7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fc8b7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc8b7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc8b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8b7-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc8b7-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc8b7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc8b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8b7-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc8b7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc8b7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc8b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8b7-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="fc8b7-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





