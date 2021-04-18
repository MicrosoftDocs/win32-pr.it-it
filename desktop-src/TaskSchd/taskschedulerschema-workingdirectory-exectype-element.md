---
title: Elemento WorkingDirectory (execType)
description: Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Utilità di pianificazione elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302674"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="a432c-104">Elemento WorkingDirectory (execType)</span><span class="sxs-lookup"><span data-stu-id="a432c-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="a432c-105">Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="a432c-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="a432c-106">L'elemento **WorkingDirectory** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a432c-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a432c-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="a432c-107">Parent element</span></span>



| <span data-ttu-id="a432c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a432c-108">Element</span></span>                                                      | <span data-ttu-id="a432c-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="a432c-109">Derived from</span></span>                                                 | <span data-ttu-id="a432c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a432c-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a432c-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="a432c-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="a432c-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="a432c-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="a432c-113">Specifica un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a432c-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a432c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a432c-114">Remarks</span></span>

<span data-ttu-id="a432c-115">Per lo sviluppo di script, la directory di lavoro viene specificata dalla proprietà [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="a432c-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="a432c-116">Per lo sviluppo in C++, la directory di lavoro viene specificata dalla proprietà [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="a432c-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a432c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a432c-117">Examples</span></span>

<span data-ttu-id="a432c-118">Il codice XML seguente definisce un'azione di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a432c-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="a432c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a432c-119">Requirements</span></span>



| <span data-ttu-id="a432c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a432c-120">Requirement</span></span> | <span data-ttu-id="a432c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a432c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a432c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a432c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a432c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a432c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a432c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a432c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a432c-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a432c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a432c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a432c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a432c-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a432c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a432c-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a432c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





