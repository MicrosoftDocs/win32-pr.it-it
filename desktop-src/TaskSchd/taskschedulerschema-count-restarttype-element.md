---
title: Elemento count (restartType)
description: Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Conteggio Utilità di pianificazione elementi
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475970"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="f505f-104">Elemento count (restartType)</span><span class="sxs-lookup"><span data-stu-id="f505f-104">Count (restartType) Element</span></span>

<span data-ttu-id="f505f-105">Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="f505f-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f505f-106">L'elemento è definito dal tipo complesso [**restartType**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f505f-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f505f-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f505f-107">Parent element</span></span>



| <span data-ttu-id="f505f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f505f-108">Element</span></span>                                                                               | <span data-ttu-id="f505f-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="f505f-109">Derived from</span></span>                                                       | <span data-ttu-id="f505f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f505f-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f505f-111">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="f505f-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="f505f-112">**restartType**</span><span class="sxs-lookup"><span data-stu-id="f505f-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="f505f-113">Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="f505f-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f505f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f505f-114">Remarks</span></span>

<span data-ttu-id="f505f-115">Se questo elemento viene specificato, è necessario specificare anche l'elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) per indicare al utilità di pianificazione per quanto tempo provare a riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="f505f-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="f505f-116">Per lo sviluppo in C++, vedere [**la proprietà RestartCount di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="f505f-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="f505f-117">Per lo sviluppo di script, vedere [**TaskSettings. RestartCount**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="f505f-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f505f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f505f-118">Requirements</span></span>



| <span data-ttu-id="f505f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f505f-119">Requirement</span></span> | <span data-ttu-id="f505f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f505f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f505f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f505f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f505f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f505f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f505f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f505f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f505f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f505f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f505f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f505f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f505f-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f505f-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





