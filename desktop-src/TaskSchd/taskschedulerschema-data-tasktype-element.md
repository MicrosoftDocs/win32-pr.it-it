---
title: Elemento data (taskType)
description: Definisce i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Utilità di pianificazione elemento dati
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740826"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="205fa-104">Elemento data (taskType)</span><span class="sxs-lookup"><span data-stu-id="205fa-104">Data (taskType) Element</span></span>

<span data-ttu-id="205fa-105">Definisce i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="205fa-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="205fa-106">L'elemento **dati** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="205fa-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="205fa-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="205fa-107">Parent element</span></span>



| <span data-ttu-id="205fa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="205fa-108">Element</span></span>                                          | <span data-ttu-id="205fa-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="205fa-109">Derived from</span></span>                                                 | <span data-ttu-id="205fa-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="205fa-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="205fa-111">**Attività**</span><span class="sxs-lookup"><span data-stu-id="205fa-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="205fa-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="205fa-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="205fa-113">Definisce l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="205fa-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="205fa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="205fa-114">Remarks</span></span>

<span data-ttu-id="205fa-115">Come esempio di questo tipo di dati, il servizio Avvisi e registri di prestazioni usa questa proprietà come contenitore di archiviazione per la query del contatore delle prestazioni associata a un'attività.</span><span class="sxs-lookup"><span data-stu-id="205fa-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="205fa-116">Per lo sviluppo in C++, i dati di un'attività vengono specificati utilizzando la [**proprietà Data di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span><span class="sxs-lookup"><span data-stu-id="205fa-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="205fa-117">Per lo sviluppo di script, i dati di un'attività vengono specificati utilizzando la proprietà [**TaskDefinition. Data**](taskdefinition-data.md) .</span><span class="sxs-lookup"><span data-stu-id="205fa-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="205fa-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="205fa-118">Requirements</span></span>



| <span data-ttu-id="205fa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="205fa-119">Requirement</span></span> | <span data-ttu-id="205fa-120">Valore</span><span class="sxs-lookup"><span data-stu-id="205fa-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="205fa-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="205fa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="205fa-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="205fa-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="205fa-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="205fa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="205fa-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="205fa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="205fa-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="205fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205fa-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="205fa-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="205fa-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="205fa-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





