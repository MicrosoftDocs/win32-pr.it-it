---
description: 'MFT_MESSAGE_COMMAND_DRAIN: richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092749"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="9efee-103">SVUOTAMENTO \_ DEL \_ COMANDO MFT MESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="9efee-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="9efee-104">Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="9efee-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="9efee-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="9efee-105">Message Parameter</span></span>

<span data-ttu-id="9efee-106">No.</span><span class="sxs-lookup"><span data-stu-id="9efee-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="9efee-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9efee-107">Remarks</span></span>

<span data-ttu-id="9efee-108">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="9efee-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="9efee-109">Dopo l'invio di questo messaggio, il flusso di input specificato non accetta l'input finché MFT non elabora tutti i dati delle chiamate precedenti a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="9efee-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="9efee-110">Il processo di svuotamento varia leggermente tra MFT sincroni e MFT asincroni:</span><span class="sxs-lookup"><span data-stu-id="9efee-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="9efee-111">**MFT sincroni**</span><span class="sxs-lookup"><span data-stu-id="9efee-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="9efee-112">Dopo che il client ha inviato questo messaggio, chiama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in un ciclo, finché **ProcessOutput** non restituisce il codice di errore **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT**.</span><span class="sxs-lookup"><span data-stu-id="9efee-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="9efee-113">Finché il MFT ha ancora dati da elaborare, le altre chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9efee-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="9efee-114">MFT continua a produrre output fino a quando non usa tutti i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="9efee-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="9efee-115">MFT rimuove tutti i dati che non possono essere elaborati in un esempio di output completo.</span><span class="sxs-lookup"><span data-stu-id="9efee-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="9efee-116">Ad esempio, deve eliminare un fotogramma video parziale.</span><span class="sxs-lookup"><span data-stu-id="9efee-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="9efee-117">**MFT asincroni**</span><span class="sxs-lookup"><span data-stu-id="9efee-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="9efee-118">MFT continua a inviare [eventi METransformHaveOutput](metransformhaveoutput.md) finché non ha più dati da elaborare.</span><span class="sxs-lookup"><span data-stu-id="9efee-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="9efee-119">Non invia eventi [METransformNeedInput](metransformneedinput.md) durante questo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="9efee-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="9efee-120">Dopo che il MFT ha inviato [l'ultimo evento METransformHaveOutput,](metransformhaveoutput.md) invia un [evento METransformDrainComplete.](metransformdraincomplete.md)</span><span class="sxs-lookup"><span data-stu-id="9efee-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="9efee-121">Al termine dello svuotamento, MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) finché non riceve un messaggio [**MFT \_ MESSAGE NOTIFY START \_ OF \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) dal client.</span><span class="sxs-lookup"><span data-stu-id="9efee-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="9efee-122">Dopo che il client ha svuotato il MFT, il client può inviare altri dati di input.</span><span class="sxs-lookup"><span data-stu-id="9efee-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="9efee-123">Il primo esempio dopo l'operazione di svuotamento deve avere l'attributo discontinuità [**(attributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="9efee-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="9efee-124">Nelle versioni precedenti di questa documentazione è stato dichiarato che il parametro *dell'evento ulParam* è un membro [**\_ dell'enumerazione MFT \_ DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type)</span><span class="sxs-lookup"><span data-stu-id="9efee-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="9efee-125">Risposta errata.</span><span class="sxs-lookup"><span data-stu-id="9efee-125">That is not correct.</span></span> <span data-ttu-id="9efee-126">UlParam *contiene* un identificatore di flusso.</span><span class="sxs-lookup"><span data-stu-id="9efee-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="9efee-127">Implementazione</span><span class="sxs-lookup"><span data-stu-id="9efee-127">Implementation</span></span>

<span data-ttu-id="9efee-128">Un MFT asincrono deve sempre restituire [METransformDrainComplete](metransformdraincomplete.md) dopo che è stato svuotato.</span><span class="sxs-lookup"><span data-stu-id="9efee-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="9efee-129">Un MFT sincrono può ignorare questo messaggio e restituire S \_ OK se si verificano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9efee-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="9efee-130">MFT non archivia mai più di un campione di input alla volta.</span><span class="sxs-lookup"><span data-stu-id="9efee-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="9efee-131">Ogni esempio di input produce un singolo esempio di output.</span><span class="sxs-lookup"><span data-stu-id="9efee-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="9efee-132">In caso contrario, un MFT sincrono deve implementare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9efee-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9efee-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9efee-133">Requirements</span></span>



| <span data-ttu-id="9efee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9efee-134">Requirement</span></span> | <span data-ttu-id="9efee-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9efee-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9efee-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9efee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9efee-137">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9efee-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9efee-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9efee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9efee-139">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9efee-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9efee-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9efee-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9efee-141"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="9efee-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9efee-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9efee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efee-143">**TIPO DI \_ MESSAGGIO \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="9efee-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="9efee-144">MFT asincroni</span><span class="sxs-lookup"><span data-stu-id="9efee-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




