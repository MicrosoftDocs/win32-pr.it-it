---
title: Elemento DisallowStartOnRemoteAppSession (settingsType)
description: Specifica che l'attività non verrà avviata se attivata per l'esecuzione in una sessione di applicazioni remote integrate localmente (RAIL).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Utilità di pianificazione elemento DisallowStartOnRemoteAppSession
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301339"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="5fadf-104">Elemento DisallowStartOnRemoteAppSession (settingsType)</span><span class="sxs-lookup"><span data-stu-id="5fadf-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="5fadf-105">Specifica che l'attività non verrà avviata se attivata per l'esecuzione in una sessione di applicazioni remote integrate localmente (RAIL).</span><span class="sxs-lookup"><span data-stu-id="5fadf-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="5fadf-106">L'elemento **DisallowStartOnRemoteAppSession** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5fadf-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5fadf-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5fadf-107">Parent element</span></span>



| <span data-ttu-id="5fadf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5fadf-108">Element</span></span>                                                           | <span data-ttu-id="5fadf-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="5fadf-109">Derived from</span></span>                                                         | <span data-ttu-id="5fadf-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fadf-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fadf-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5fadf-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5fadf-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5fadf-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5fadf-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="5fadf-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5fadf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fadf-114">Remarks</span></span>

<span data-ttu-id="5fadf-115">L'impostazione predefinita per questo elemento è false.</span><span class="sxs-lookup"><span data-stu-id="5fadf-115">The default setting for this element is False.</span></span>

<span data-ttu-id="5fadf-116">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .</span><span class="sxs-lookup"><span data-stu-id="5fadf-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5fadf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="5fadf-117">Examples</span></span>

<span data-ttu-id="5fadf-118">Nel codice XML seguente viene definito un elemento Settings che non consente l'avvio dell'attività se l'attività viene attivata per l'esecuzione in una sessione BINARIa.</span><span class="sxs-lookup"><span data-stu-id="5fadf-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="5fadf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fadf-119">Requirements</span></span>



| <span data-ttu-id="5fadf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fadf-120">Requirement</span></span> | <span data-ttu-id="5fadf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5fadf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5fadf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fadf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fadf-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5fadf-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5fadf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fadf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fadf-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5fadf-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fadf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fadf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fadf-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5fadf-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





