---
title: Arguments (execType)-elemento
description: Specifica gli argomenti associati all'operazione della riga di comando.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento arguments Utilità di pianificazione
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518195"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="e4f26-104">Arguments (execType)-elemento</span><span class="sxs-lookup"><span data-stu-id="e4f26-104">Arguments (execType) Element</span></span>

<span data-ttu-id="e4f26-105">Specifica gli argomenti associati all'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e4f26-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="e4f26-106">L'elemento **arguments** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f26-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e4f26-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e4f26-107">Parent element</span></span>



| <span data-ttu-id="e4f26-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e4f26-108">Element</span></span>                                                      | <span data-ttu-id="e4f26-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e4f26-109">Derived from</span></span>                                                 | <span data-ttu-id="e4f26-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f26-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="e4f26-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="e4f26-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="e4f26-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="e4f26-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="e4f26-113">Specifica un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e4f26-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4f26-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4f26-114">Remarks</span></span>

<span data-ttu-id="e4f26-115">Per lo sviluppo in C++, vedere la [**proprietà Arguments di IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="e4f26-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="e4f26-116">Per lo sviluppo di script, vedere [**ExecAction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="e4f26-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e4f26-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e4f26-117">Examples</span></span>

<span data-ttu-id="e4f26-118">Per un esempio completo del codice XML per un'attività che usa un'azione eseguibile, vedere [esempio di trigger temporale (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e4f26-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f26-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4f26-119">Requirements</span></span>



| <span data-ttu-id="e4f26-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f26-120">Requirement</span></span> | <span data-ttu-id="e4f26-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4f26-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4f26-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4f26-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f26-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4f26-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4f26-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4f26-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f26-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4f26-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4f26-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f26-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e4f26-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





