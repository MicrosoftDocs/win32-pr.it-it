---
title: Esecuzione (SystemPropertiesType) (elemento)
description: Contiene informazioni sul processo e sul thread che hanno registrato l'evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- EventLog elemento esecuzione
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740359"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="4727d-104">Esecuzione (SystemPropertiesType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="4727d-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="4727d-105">Contiene informazioni sul processo e sul thread che hanno registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4727d-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4727d-106">L'elemento **Execution** viene definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4727d-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="4727d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="4727d-107">Attributes</span></span>



| <span data-ttu-id="4727d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="4727d-108">Name</span></span>          | <span data-ttu-id="4727d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4727d-109">Type</span></span>         | <span data-ttu-id="4727d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4727d-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4727d-111">KernelTime</span><span class="sxs-lookup"><span data-stu-id="4727d-111">KernelTime</span></span>    | <span data-ttu-id="4727d-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-112">unsignedInt</span></span>  | <span data-ttu-id="4727d-113">Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in unità di tempo della CPU.</span><span class="sxs-lookup"><span data-stu-id="4727d-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="4727d-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="4727d-114">ProcessID</span></span>     | <span data-ttu-id="4727d-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-115">unsignedInt</span></span>  | <span data-ttu-id="4727d-116">Identifica il processo che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4727d-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="4727d-117">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="4727d-117">ProcessorID</span></span>   | <span data-ttu-id="4727d-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="4727d-118">unsignedByte</span></span> | <span data-ttu-id="4727d-119">Numero di identificazione del processore che ha elaborato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4727d-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="4727d-120">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="4727d-120">ProcessorTime</span></span> | <span data-ttu-id="4727d-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-121">unsignedInt</span></span>  | <span data-ttu-id="4727d-122">Per le sessioni private ETW, il tempo di esecuzione trascorso per le istruzioni in modalità utente, in cicli della CPU.</span><span class="sxs-lookup"><span data-stu-id="4727d-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="4727d-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="4727d-123">SessionID</span></span>     | <span data-ttu-id="4727d-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-124">unsignedInt</span></span>  | <span data-ttu-id="4727d-125">Numero di identificazione per la sessione di Terminal Server in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4727d-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="4727d-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="4727d-126">ThreadID</span></span>      | <span data-ttu-id="4727d-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-127">unsignedInt</span></span>  | <span data-ttu-id="4727d-128">Identifica il thread che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4727d-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="4727d-129">Tempi</span><span class="sxs-lookup"><span data-stu-id="4727d-129">UserTime</span></span>      | <span data-ttu-id="4727d-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4727d-130">unsignedInt</span></span>  | <span data-ttu-id="4727d-131">Tempo di esecuzione trascorso per le istruzioni in modalità utente, in unità di tempo della CPU.</span><span class="sxs-lookup"><span data-stu-id="4727d-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="4727d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4727d-132">Requirements</span></span>



| <span data-ttu-id="4727d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4727d-133">Requirement</span></span> | <span data-ttu-id="4727d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4727d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4727d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4727d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4727d-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4727d-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4727d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4727d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4727d-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4727d-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4727d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4727d-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="4727d-140">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="4727d-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4727d-141">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="4727d-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="4727d-142">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="4727d-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4727d-143">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="4727d-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





