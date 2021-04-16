---
title: Tipo complesso taskType (Utilità di pianificazione)
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- Utilità di pianificazione di tipo complesso taskType
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477776"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="f214b-104">Tipo complesso taskType</span><span class="sxs-lookup"><span data-stu-id="f214b-104">taskType Complex Type</span></span>

<span data-ttu-id="f214b-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**Task**](taskschedulerschema-task-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f214b-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f214b-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f214b-106">Child elements</span></span>



| <span data-ttu-id="f214b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f214b-107">Element</span></span>                                                                           | <span data-ttu-id="f214b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f214b-108">Type</span></span>                                                                                 | <span data-ttu-id="f214b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f214b-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f214b-110">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="f214b-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="f214b-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="f214b-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="f214b-112">Specifica le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="f214b-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="f214b-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="f214b-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="f214b-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="f214b-115">Specifica i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f214b-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="f214b-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="f214b-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="f214b-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="f214b-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="f214b-118">Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="f214b-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="f214b-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="f214b-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="f214b-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="f214b-121">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="f214b-122">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="f214b-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="f214b-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="f214b-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="f214b-124">Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="f214b-125">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="f214b-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="f214b-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="f214b-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="f214b-127">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="f214b-128">Attributi</span><span class="sxs-lookup"><span data-stu-id="f214b-128">Attributes</span></span>



| <span data-ttu-id="f214b-129">Nome</span><span class="sxs-lookup"><span data-stu-id="f214b-129">Name</span></span>    | <span data-ttu-id="f214b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="f214b-130">Type</span></span>                                                              | <span data-ttu-id="f214b-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f214b-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="f214b-132">version</span><span class="sxs-lookup"><span data-stu-id="f214b-132">version</span></span> | [<span data-ttu-id="f214b-133">**versionType**</span><span class="sxs-lookup"><span data-stu-id="f214b-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="f214b-134">Specifica la versione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f214b-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f214b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f214b-135">Requirements</span></span>



| <span data-ttu-id="f214b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f214b-136">Requirement</span></span> | <span data-ttu-id="f214b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f214b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f214b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f214b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f214b-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f214b-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f214b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f214b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f214b-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f214b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f214b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f214b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f214b-143">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f214b-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f214b-144">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f214b-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





