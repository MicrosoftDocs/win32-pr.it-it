---
title: Tipo semplice multipleInstancesPolicyType
description: Definisce le costanti dei criteri dell'istanza per l'elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Utilità di pianificazione di tipo semplice multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964435"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="0985d-104">Tipo semplice multipleInstancesPolicyType</span><span class="sxs-lookup"><span data-stu-id="0985d-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="0985d-105">Definisce le costanti dei criteri dell'istanza per l'elemento [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0985d-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="0985d-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="0985d-106">Enumeration values</span></span>

<span data-ttu-id="0985d-107">Il tipo semplice **multipleInstancesPolicyType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0985d-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="0985d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0985d-108">Value</span></span>        | <span data-ttu-id="0985d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0985d-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0985d-110">Parallelo</span><span class="sxs-lookup"><span data-stu-id="0985d-110">Parallel</span></span>     | <span data-ttu-id="0985d-111">Avvia una nuova istanza di mentre è in esecuzione un'istanza esistente.</span><span class="sxs-lookup"><span data-stu-id="0985d-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="0985d-112">Coda</span><span class="sxs-lookup"><span data-stu-id="0985d-112">Queue</span></span>        | <span data-ttu-id="0985d-113">Avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0985d-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="0985d-114">IgnoreNew</span><span class="sxs-lookup"><span data-stu-id="0985d-114">IgnoreNew</span></span>    | <span data-ttu-id="0985d-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0985d-115">Default.</span></span> <span data-ttu-id="0985d-116">Non avvia una nuova istanza se è in esecuzione un'istanza esistente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0985d-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="0985d-117">StopExisting</span><span class="sxs-lookup"><span data-stu-id="0985d-117">StopExisting</span></span> | <span data-ttu-id="0985d-118">Arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="0985d-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="0985d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0985d-119">Requirements</span></span>



| <span data-ttu-id="0985d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0985d-120">Requirement</span></span> | <span data-ttu-id="0985d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0985d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0985d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0985d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0985d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0985d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0985d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0985d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0985d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0985d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0985d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0985d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0985d-127">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0985d-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0985d-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0985d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





