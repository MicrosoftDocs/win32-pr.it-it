---
title: Elemento StopIfGoingOnBatteries (settingsType)
description: Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Utilità di pianificazione elemento StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301329"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="5d7cc-104">Elemento StopIfGoingOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="5d7cc-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="5d7cc-105">Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="5d7cc-106">L'elemento **StopIfGoingOnBatteries** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7cc-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5d7cc-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5d7cc-107">Parent element</span></span>



| <span data-ttu-id="5d7cc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5d7cc-108">Element</span></span>                                                           | <span data-ttu-id="5d7cc-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="5d7cc-109">Derived from</span></span>                                                         | <span data-ttu-id="5d7cc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d7cc-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d7cc-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5d7cc-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5d7cc-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5d7cc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d7cc-114">Remarks</span></span>

<span data-ttu-id="5d7cc-115">L'impostazione predefinita per questo elemento è false.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-115">The default setting for this element is False.</span></span> <span data-ttu-id="5d7cc-116">Si noti che il valore predefinito è stato modificato rispetto alle versioni precedenti di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="5d7cc-117">Per lo sviluppo di script, questa impostazione viene specificata tramite la proprietà [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7cc-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="5d7cc-118">Per lo sviluppo in C++, questa impostazione viene specificata tramite la proprietà [**ITaskSettings:: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="5d7cc-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5d7cc-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5d7cc-119">Examples</span></span>

<span data-ttu-id="5d7cc-120">Nel codice XML seguente viene definito un elemento Settings che consente la terminazione rigida dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="5d7cc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d7cc-121">Requirements</span></span>



| <span data-ttu-id="5d7cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7cc-122">Requirement</span></span> | <span data-ttu-id="5d7cc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5d7cc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d7cc-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7cc-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d7cc-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5d7cc-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7cc-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d7cc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d7cc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d7cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7cc-129">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5d7cc-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





