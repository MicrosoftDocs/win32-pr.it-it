---
title: Elemento volatile
description: Indica se l'attività viene disabilitata automaticamente ogni volta che viene avviato Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Utilità di pianificazione elemento volatile
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743314"
---
# <a name="volatile-element"></a><span data-ttu-id="ef419-104">Elemento volatile</span><span class="sxs-lookup"><span data-stu-id="ef419-104">Volatile Element</span></span>

<span data-ttu-id="ef419-105">Indica se l'attività viene disabilitata automaticamente ogni volta che viene avviato Windows.</span><span class="sxs-lookup"><span data-stu-id="ef419-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="ef419-106">L'elemento **volatile** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ef419-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ef419-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ef419-107">Parent element</span></span>



| <span data-ttu-id="ef419-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ef419-108">Element</span></span>                                                           | <span data-ttu-id="ef419-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="ef419-109">Derived from</span></span> | <span data-ttu-id="ef419-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef419-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef419-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="ef419-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="ef419-112">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="ef419-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ef419-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef419-113">Remarks</span></span>

<span data-ttu-id="ef419-114">Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .</span><span class="sxs-lookup"><span data-stu-id="ef419-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef419-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef419-115">Requirements</span></span>



| <span data-ttu-id="ef419-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef419-116">Requirement</span></span> | <span data-ttu-id="ef419-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ef419-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef419-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef419-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef419-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef419-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="ef419-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef419-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef419-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef419-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef419-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef419-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef419-123">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ef419-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ef419-124">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ef419-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





