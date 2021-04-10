---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Utilità di pianificazione elemento StopOnIdleEnd
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964821"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="c9398-104">Elemento StopOnIdleEnd (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="c9398-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="c9398-105">Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c9398-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="c9398-106">L'elemento **StopOnIdleEnd** è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9398-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c9398-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c9398-107">Parent element</span></span>



| <span data-ttu-id="c9398-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9398-108">Element</span></span>                                                                       | <span data-ttu-id="c9398-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="c9398-109">Derived from</span></span>                                                                 | <span data-ttu-id="c9398-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9398-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9398-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="c9398-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="c9398-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="c9398-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="c9398-113">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="c9398-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c9398-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9398-114">Remarks</span></span>

<span data-ttu-id="c9398-115">Per lo sviluppo in C++, vedere [**la proprietà StopOnIdleEnd di IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="c9398-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="c9398-116">Per lo sviluppo di script, vedere [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="c9398-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c9398-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9398-117">Examples</span></span>

<span data-ttu-id="c9398-118">Il codice XML seguente definisce un'impostazione inattiva che indica che l'attività non deve essere eseguita al termine della condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="c9398-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="c9398-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9398-119">Requirements</span></span>



| <span data-ttu-id="c9398-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9398-120">Requirement</span></span> | <span data-ttu-id="c9398-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c9398-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9398-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9398-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9398-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9398-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9398-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9398-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9398-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9398-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9398-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9398-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9398-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c9398-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





