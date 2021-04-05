---
description: Evento di traccia di rete Winsock per l'operazione di chiusura del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Evento AFD_EVENT_CLOSE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751487"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="54708-103">\_Evento di \_ chiusura evento AFD</span><span class="sxs-lookup"><span data-stu-id="54708-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="54708-104">L'evento di **\_ \_ chiusura evento AFD** è un evento di traccia di rete Winsock per l'operazione di chiusura del socket.</span><span class="sxs-lookup"><span data-stu-id="54708-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="54708-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="54708-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54708-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="54708-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="54708-107">Informazioni su questo evento.</span><span class="sxs-lookup"><span data-stu-id="54708-107">Information on this event.</span></span>

<span data-ttu-id="54708-108">Nella tabella seguente sono elencati i valori possibili per il parametro *EnterExit* :</span><span class="sxs-lookup"><span data-stu-id="54708-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="54708-109">Valore</span><span class="sxs-lookup"><span data-stu-id="54708-109">Value</span></span>                                                                        | <span data-ttu-id="54708-110">Significato</span><span class="sxs-lookup"><span data-stu-id="54708-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54708-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="54708-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="54708-112">Inizio di una richiesta Winsock.</span><span class="sxs-lookup"><span data-stu-id="54708-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="54708-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="54708-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="54708-114">La richiesta Winsock è stata completata.</span><span class="sxs-lookup"><span data-stu-id="54708-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="54708-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="54708-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="54708-116">Il driver AFD Winsock ha intrapreso un'azione interna (ad esempio, l'interruzione di una connessione).</span><span class="sxs-lookup"><span data-stu-id="54708-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="54708-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="54708-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="54708-118">Questo evento è stato generato dal driver TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="54708-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="54708-119">Questo indica in genere una notifica dei dati.</span><span class="sxs-lookup"><span data-stu-id="54708-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="54708-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="54708-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="54708-121">Il driver AFD Winsock ha causato il verificarsi di questo evento (ad esempio, l'impostazione di un'opzione socket).</span><span class="sxs-lookup"><span data-stu-id="54708-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54708-122">*Posizione*</span><span class="sxs-lookup"><span data-stu-id="54708-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="54708-123">Campo privato utilizzato internamente.</span><span class="sxs-lookup"><span data-stu-id="54708-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="54708-124">*Processo*</span><span class="sxs-lookup"><span data-stu-id="54708-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="54708-125">Indirizzo [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del processo a cui appartiene il socket correlato.</span><span class="sxs-lookup"><span data-stu-id="54708-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="54708-126">Si tratta di una struttura opaca che funge da oggetto processo per un processo.</span><span class="sxs-lookup"><span data-stu-id="54708-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="54708-127">Per ulteriori informazioni, vedere la documentazione del kit driver Windows per la struttura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .</span><span class="sxs-lookup"><span data-stu-id="54708-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54708-128">*Endpoint*</span><span class="sxs-lookup"><span data-stu-id="54708-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="54708-129">Indirizzo dell' \_ endpoint AFD del socket.</span><span class="sxs-lookup"><span data-stu-id="54708-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="54708-130">*Status*</span><span class="sxs-lookup"><span data-stu-id="54708-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="54708-131">Codice NTSTATUS per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="54708-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54708-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="54708-132">Remarks</span></span>

<span data-ttu-id="54708-133">L'evento di **\_ \_ chiusura evento AFD** viene tracciato per un'operazione di rete Winsock per la chiusura di un socket.</span><span class="sxs-lookup"><span data-stu-id="54708-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="54708-134">Il canale per questo evento è Winsock-AFD.</span><span class="sxs-lookup"><span data-stu-id="54708-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="54708-135">Il livello per questo evento è informativo.</span><span class="sxs-lookup"><span data-stu-id="54708-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="54708-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54708-136">Requirements</span></span>



| <span data-ttu-id="54708-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="54708-137">Requirement</span></span> | <span data-ttu-id="54708-138">Valore</span><span class="sxs-lookup"><span data-stu-id="54708-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="54708-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54708-139">Minimum supported client</span></span><br/> | <span data-ttu-id="54708-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54708-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="54708-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54708-141">Minimum supported server</span></span><br/> | <span data-ttu-id="54708-142">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="54708-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54708-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54708-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54708-144">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="54708-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="54708-145">**\_descrittore evento**</span><span class="sxs-lookup"><span data-stu-id="54708-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="54708-146">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="54708-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="54708-147">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="54708-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="54708-148">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="54708-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

