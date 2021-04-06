---
title: Elemento Principals (taskType)
description: Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento Principals Utilità di pianificazione
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963858"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="48a5f-104">Elemento Principals (taskType)</span><span class="sxs-lookup"><span data-stu-id="48a5f-104">Principals (taskType) Element</span></span>

<span data-ttu-id="48a5f-105">Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="48a5f-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="48a5f-106">L'elemento **Principals** viene definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="48a5f-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="48a5f-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="48a5f-107">Parent element</span></span>



| <span data-ttu-id="48a5f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="48a5f-108">Element</span></span>                                          | <span data-ttu-id="48a5f-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="48a5f-109">Derived from</span></span>                                                 | <span data-ttu-id="48a5f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a5f-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="48a5f-111">**Attività**</span><span class="sxs-lookup"><span data-stu-id="48a5f-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="48a5f-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="48a5f-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="48a5f-113">Definisce l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="48a5f-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="48a5f-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="48a5f-114">Child elements</span></span>



| <span data-ttu-id="48a5f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="48a5f-115">Element</span></span>                                                                  | <span data-ttu-id="48a5f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a5f-116">Type</span></span>                                                                   | <span data-ttu-id="48a5f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a5f-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="48a5f-118">**Principale**</span><span class="sxs-lookup"><span data-stu-id="48a5f-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="48a5f-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="48a5f-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="48a5f-120">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="48a5f-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48a5f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="48a5f-121">Remarks</span></span>

<span data-ttu-id="48a5f-122">È possibile specificare fino a 32 entità per un'attività.</span><span class="sxs-lookup"><span data-stu-id="48a5f-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="48a5f-123">Per lo sviluppo di script, le entità di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. Principal**](taskdefinition-principal.md) .</span><span class="sxs-lookup"><span data-stu-id="48a5f-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="48a5f-124">Per lo sviluppo in C++, le entità di un'attività vengono specificate utilizzando la [**Proprietà Principal di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span><span class="sxs-lookup"><span data-stu-id="48a5f-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="48a5f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="48a5f-125">Examples</span></span>

<span data-ttu-id="48a5f-126">Il codice XML seguente definisce due entità: un identificatore utente e un'entità identificatore di gruppo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="48a5f-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="48a5f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a5f-127">Requirements</span></span>



| <span data-ttu-id="48a5f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a5f-128">Requirement</span></span> | <span data-ttu-id="48a5f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="48a5f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48a5f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a5f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="48a5f-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48a5f-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48a5f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a5f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="48a5f-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48a5f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48a5f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48a5f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a5f-135">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="48a5f-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="48a5f-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="48a5f-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





