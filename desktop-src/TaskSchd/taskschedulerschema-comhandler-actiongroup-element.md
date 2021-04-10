---
title: Elemento comhandler (actionGroup)
description: Specifica un'azione che attiva un gestore.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento comhandler Utilità di pianificazione
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964675"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="e2751-104">Elemento comhandler (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="e2751-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="e2751-105">Specifica un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="e2751-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="e2751-106">L'elemento **Comhandler** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="e2751-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="e2751-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e2751-107">Parent element</span></span>



| <span data-ttu-id="e2751-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e2751-108">Element</span></span>                                                         | <span data-ttu-id="e2751-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e2751-109">Derived from</span></span>                                                       | <span data-ttu-id="e2751-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2751-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e2751-111">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="e2751-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="e2751-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="e2751-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="e2751-113">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e2751-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e2751-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e2751-114">Child elements</span></span>



| <span data-ttu-id="e2751-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e2751-115">Element</span></span>                                                               | <span data-ttu-id="e2751-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2751-116">Type</span></span>                                                         | <span data-ttu-id="e2751-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2751-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e2751-118">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="e2751-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="e2751-119">**guidType**</span><span class="sxs-lookup"><span data-stu-id="e2751-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="e2751-120">Specifica l'identificatore della classe del gestore.</span><span class="sxs-lookup"><span data-stu-id="e2751-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="e2751-121">**Data**</span><span class="sxs-lookup"><span data-stu-id="e2751-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="e2751-122">**dataType**</span><span class="sxs-lookup"><span data-stu-id="e2751-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="e2751-123">Specifica i dati aggiuntivi associati al gestore.</span><span class="sxs-lookup"><span data-stu-id="e2751-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e2751-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2751-124">Remarks</span></span>

<span data-ttu-id="e2751-125">Le applicazioni definiscono un'azione del gestore COM usando l'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="e2751-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="e2751-126">Attributi</span><span class="sxs-lookup"><span data-stu-id="e2751-126">Attributes</span></span>

<span data-ttu-id="e2751-127">L'attributo seguente viene definito dal tipo complesso [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e2751-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="e2751-128">ID: identificatore dell'azione eseguita dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e2751-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="e2751-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="e2751-129">Examples</span></span>

<span data-ttu-id="e2751-130">Il codice XML seguente definisce un'azione del gestore COM.</span><span class="sxs-lookup"><span data-stu-id="e2751-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="e2751-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2751-131">Requirements</span></span>



| <span data-ttu-id="e2751-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2751-132">Requirement</span></span> | <span data-ttu-id="e2751-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e2751-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2751-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2751-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e2751-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2751-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2751-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2751-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e2751-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2751-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2751-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2751-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2751-139">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e2751-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





