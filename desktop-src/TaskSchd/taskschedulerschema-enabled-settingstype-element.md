---
title: Elemento Enabled (settingsType)
description: Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Elemento Enabled Utilità di pianificazione
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302491"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="6616f-105">Elemento Enabled (settingsType)</span><span class="sxs-lookup"><span data-stu-id="6616f-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="6616f-106">Specifica che l'attività è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6616f-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="6616f-107">L'attività può essere eseguita solo quando questa impostazione è true.</span><span class="sxs-lookup"><span data-stu-id="6616f-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="6616f-108">L'elemento **Enabled** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6616f-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6616f-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6616f-109">Parent element</span></span>



| <span data-ttu-id="6616f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="6616f-110">Element</span></span>                                                           | <span data-ttu-id="6616f-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="6616f-111">Derived from</span></span>                                                         | <span data-ttu-id="6616f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6616f-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6616f-113">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6616f-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6616f-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="6616f-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6616f-115">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="6616f-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6616f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6616f-116">Remarks</span></span>

<span data-ttu-id="6616f-117">Per lo sviluppo in C++, vedere [**Enabled property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="6616f-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="6616f-118">Per lo sviluppo di script, vedere [**TaskSettings. Enabled**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="6616f-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6616f-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="6616f-119">Examples</span></span>

<span data-ttu-id="6616f-120">Per un esempio completo del codice XML per un'attività abilitata, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="6616f-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6616f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6616f-121">Requirements</span></span>



| <span data-ttu-id="6616f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6616f-122">Requirement</span></span> | <span data-ttu-id="6616f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6616f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6616f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6616f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6616f-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6616f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6616f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6616f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6616f-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6616f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





