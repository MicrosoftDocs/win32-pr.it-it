---
title: Elemento Exec (actionGroup)
description: Specifica un'azione che esegue un'operazione della riga di comando.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Utilità di pianificazione elemento Exec
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320835"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="212cd-104">Elemento Exec (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="212cd-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="212cd-105">Specifica un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="212cd-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="212cd-106">L'elemento **Exec** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="212cd-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="212cd-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="212cd-107">Parent element</span></span>



| <span data-ttu-id="212cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="212cd-108">Element</span></span>                                                         | <span data-ttu-id="212cd-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="212cd-109">Derived from</span></span>                                                       | <span data-ttu-id="212cd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="212cd-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="212cd-111">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="212cd-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="212cd-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="212cd-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="212cd-113">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="212cd-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="212cd-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="212cd-114">Child elements</span></span>



| <span data-ttu-id="212cd-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="212cd-115">Element</span></span>                                                                           | <span data-ttu-id="212cd-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="212cd-116">Type</span></span>       | <span data-ttu-id="212cd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="212cd-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="212cd-118">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="212cd-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="212cd-119">**string**</span><span class="sxs-lookup"><span data-stu-id="212cd-119">**string**</span></span> | <span data-ttu-id="212cd-120">Specifica gli argomenti associati all'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="212cd-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="212cd-121">**Comando**</span><span class="sxs-lookup"><span data-stu-id="212cd-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="212cd-122">**string**</span><span class="sxs-lookup"><span data-stu-id="212cd-122">**string**</span></span> | <span data-ttu-id="212cd-123">Specifica il file eseguibile o il documento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="212cd-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="212cd-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="212cd-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="212cd-125">string</span><span class="sxs-lookup"><span data-stu-id="212cd-125">string</span></span>     | <span data-ttu-id="212cd-126">Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="212cd-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="212cd-127">Attributi</span><span class="sxs-lookup"><span data-stu-id="212cd-127">Attributes</span></span>



| <span data-ttu-id="212cd-128">Nome</span><span class="sxs-lookup"><span data-stu-id="212cd-128">Name</span></span> | <span data-ttu-id="212cd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="212cd-129">Type</span></span>       | <span data-ttu-id="212cd-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="212cd-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="212cd-131">id</span><span class="sxs-lookup"><span data-stu-id="212cd-131">id</span></span>   | <span data-ttu-id="212cd-132">**string**</span><span class="sxs-lookup"><span data-stu-id="212cd-132">**string**</span></span> | <span data-ttu-id="212cd-133">Identificatore dell'azione eseguita dall'attività.</span><span class="sxs-lookup"><span data-stu-id="212cd-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="212cd-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="212cd-134">Remarks</span></span>

<span data-ttu-id="212cd-135">Gli elementi figlio elencati sopra sono definiti dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="212cd-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="212cd-136">Per lo sviluppo di script, un'azione di esecuzione viene definita dall'oggetto [**ExecAction**](execaction.md) .</span><span class="sxs-lookup"><span data-stu-id="212cd-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="212cd-137">Per lo sviluppo in C++, un'azione di esecuzione viene definita dall'interfaccia [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .</span><span class="sxs-lookup"><span data-stu-id="212cd-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="212cd-138">Se le variabili di ambiente vengono usate negli elementi [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)o [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , i valori delle variabili di ambiente vengono memorizzati nella cache e usati quando viene avviata la Taskeng.exe (il motore attività).</span><span class="sxs-lookup"><span data-stu-id="212cd-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="212cd-139">Le modifiche apportate alle variabili di ambiente che si verificano dopo l'avvio del motore attività non verranno usate dal motore delle attività.</span><span class="sxs-lookup"><span data-stu-id="212cd-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="212cd-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="212cd-140">Examples</span></span>

<span data-ttu-id="212cd-141">Per un esempio completo del codice XML per un'attività che usa un trigger di evento, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="212cd-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="212cd-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="212cd-142">Requirements</span></span>



| <span data-ttu-id="212cd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="212cd-143">Requirement</span></span> | <span data-ttu-id="212cd-144">Valore</span><span class="sxs-lookup"><span data-stu-id="212cd-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="212cd-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="212cd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="212cd-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="212cd-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="212cd-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="212cd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="212cd-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="212cd-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="212cd-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="212cd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="212cd-150">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="212cd-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





