---
title: Elemento DisallowStartIfOnBatteries (settingsType)
description: Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Utilità di pianificazione elemento DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743775"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a><span data-ttu-id="bf681-104">Elemento DisallowStartIfOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="bf681-104">DisallowStartIfOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="bf681-105">Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="bf681-105">Specifies that the task will not be started if the computer is running on batteries.</span></span>

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

<span data-ttu-id="bf681-106">L'elemento **DisallowStartIfOnBatteries** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bf681-106">The **DisallowStartIfOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bf681-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="bf681-107">Parent element</span></span>



| <span data-ttu-id="bf681-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf681-108">Element</span></span>                                                           | <span data-ttu-id="bf681-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="bf681-109">Derived from</span></span>                                                         | <span data-ttu-id="bf681-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf681-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf681-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="bf681-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="bf681-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="bf681-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="bf681-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="bf681-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf681-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf681-114">Remarks</span></span>

<span data-ttu-id="bf681-115">L'impostazione predefinita per questo elemento è true.</span><span class="sxs-lookup"><span data-stu-id="bf681-115">The default setting for this element is True.</span></span>

<span data-ttu-id="bf681-116">Per lo sviluppo di script, è possibile accedere a queste informazioni tramite la proprietà [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="bf681-116">For scripting development, this information is accessed through the [**TaskSettings.DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) property.</span></span>

<span data-ttu-id="bf681-117">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="bf681-117">For C++ development, this information is accessed through the [**ITaskSettings::DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="bf681-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf681-118">Examples</span></span>

<span data-ttu-id="bf681-119">Nel codice XML seguente viene definito un elemento Settings che non consente l'esecuzione dell'attività se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="bf681-119">The following XML defines a settings element that does not allow the task to run if the computer is running on batteries.</span></span>


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="bf681-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf681-120">Requirements</span></span>



| <span data-ttu-id="bf681-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf681-121">Requirement</span></span> | <span data-ttu-id="bf681-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bf681-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf681-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf681-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bf681-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf681-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf681-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf681-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bf681-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf681-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf681-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf681-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf681-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bf681-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





