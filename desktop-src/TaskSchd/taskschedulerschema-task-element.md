---
title: Elemento Task
description: Definisce l'attività eseguita dal servizio Utilità di pianificazione.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Utilità di pianificazione elemento attività
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873485"
---
# <a name="task-element"></a><span data-ttu-id="bb809-104">Elemento Task</span><span class="sxs-lookup"><span data-stu-id="bb809-104">Task Element</span></span>

<span data-ttu-id="bb809-105">Definisce l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bb809-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="bb809-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bb809-106">Child elements</span></span>



| <span data-ttu-id="bb809-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb809-107">Element</span></span>                                                                           | <span data-ttu-id="bb809-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb809-108">Type</span></span>                                                                                 | <span data-ttu-id="bb809-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb809-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb809-110">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="bb809-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="bb809-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="bb809-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="bb809-112">Specifica le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="bb809-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="bb809-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="bb809-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="bb809-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="bb809-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="bb809-115">Specifica i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bb809-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="bb809-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="bb809-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="bb809-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="bb809-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="bb809-118">Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="bb809-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="bb809-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="bb809-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="bb809-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="bb809-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="bb809-121">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="bb809-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="bb809-122">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="bb809-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="bb809-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="bb809-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="bb809-124">Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="bb809-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="bb809-125">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="bb809-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="bb809-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="bb809-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="bb809-127">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="bb809-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="bb809-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb809-128">Remarks</span></span>

<span data-ttu-id="bb809-129">Per lo sviluppo in C++, vedere [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="bb809-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="bb809-130">Per lo sviluppo di script, vedere [**TaskDefinition**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="bb809-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb809-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb809-131">Requirements</span></span>



| <span data-ttu-id="bb809-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb809-132">Requirement</span></span> | <span data-ttu-id="bb809-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bb809-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb809-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb809-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb809-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb809-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb809-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb809-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb809-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb809-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





