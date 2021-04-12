---
title: Command (execType)-elemento
description: Specifica il file eseguibile o il documento da eseguire.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Utilità di pianificazione dell'elemento Command
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400833"
---
# <a name="command-exectype-element"></a><span data-ttu-id="50f2e-104">Command (execType)-elemento</span><span class="sxs-lookup"><span data-stu-id="50f2e-104">Command (execType) Element</span></span>

<span data-ttu-id="50f2e-105">Specifica il file eseguibile o il documento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="50f2e-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="50f2e-106">L'elemento **Command** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="50f2e-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="50f2e-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="50f2e-107">Parent element</span></span>



| <span data-ttu-id="50f2e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="50f2e-108">Element</span></span>                                                      | <span data-ttu-id="50f2e-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="50f2e-109">Derived from</span></span>                                                 | <span data-ttu-id="50f2e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50f2e-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="50f2e-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="50f2e-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="50f2e-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="50f2e-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="50f2e-113">Specifica un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="50f2e-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50f2e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="50f2e-114">Remarks</span></span>

<span data-ttu-id="50f2e-115">Per lo sviluppo in C++, vedere la [**proprietà Arguments di IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="50f2e-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="50f2e-116">Per lo sviluppo di script, vedere [**ExecAction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="50f2e-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="50f2e-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="50f2e-117">Examples</span></span>

<span data-ttu-id="50f2e-118">Per un esempio completo del codice XML per un'attività che usa un'azione eseguibile, vedere [esempio di trigger temporale (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="50f2e-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50f2e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50f2e-119">Requirements</span></span>



| <span data-ttu-id="50f2e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="50f2e-120">Requirement</span></span> | <span data-ttu-id="50f2e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="50f2e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50f2e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50f2e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50f2e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50f2e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50f2e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50f2e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50f2e-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50f2e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50f2e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50f2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f2e-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="50f2e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





