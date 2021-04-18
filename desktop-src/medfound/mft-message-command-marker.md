---
description: Contrassegna un punto nel flusso. Questo messaggio si applica solo ai MFTs asincroni.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310218"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="221cd-104">\_ \_ marcatore del comando del messaggio MFT \_</span><span class="sxs-lookup"><span data-stu-id="221cd-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="221cd-105">Contrassegna un punto nel flusso.</span><span class="sxs-lookup"><span data-stu-id="221cd-105">Marks a point in the stream.</span></span> <span data-ttu-id="221cd-106">Questo messaggio si applica solo ai [MFTS asincroni](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="221cd-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="221cd-107">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="221cd-107">Message Parameter</span></span>

<span data-ttu-id="221cd-108">Valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="221cd-108">An arbitrary value.</span></span> <span data-ttu-id="221cd-109">Il MFT restituisce il valore al client nell'evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="221cd-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="221cd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="221cd-110">Remarks</span></span>

<span data-ttu-id="221cd-111">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="221cd-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="221cd-112">Il MFT risponde ai messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="221cd-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="221cd-113">Il MFT genera il numero di campioni di output possibili dai dati di input esistenti, inviando un evento [METransformHaveOutput](metransformhaveoutput.md) per ogni esempio di output.</span><span class="sxs-lookup"><span data-stu-id="221cd-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="221cd-114">Una volta generato tutto l'output, il MFT Invia un evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="221cd-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="221cd-115">Questo evento deve essere inviato dopo tutti gli eventi [METransformHaveOutput](metransformhaveoutput.md) .</span><span class="sxs-lookup"><span data-stu-id="221cd-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="221cd-116">Il client non è necessario per inviare questo messaggio e deve inviare questo messaggio solo a MFTs asincrono.</span><span class="sxs-lookup"><span data-stu-id="221cd-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="221cd-117">Un MFT sincrono non invierà un evento [METransformMarker](metransformmarker.md) in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="221cd-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="221cd-118">Implementazione</span><span class="sxs-lookup"><span data-stu-id="221cd-118">Implementation</span></span>

<span data-ttu-id="221cd-119">Il MFTs asincrono deve rispondere a questo messaggio come descritto.</span><span class="sxs-lookup"><span data-stu-id="221cd-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="221cd-120">Il MFTs sincrono deve ignorare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="221cd-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="221cd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="221cd-121">Requirements</span></span>



| <span data-ttu-id="221cd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="221cd-122">Requirement</span></span> | <span data-ttu-id="221cd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="221cd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="221cd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="221cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="221cd-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="221cd-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="221cd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="221cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="221cd-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="221cd-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="221cd-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="221cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="221cd-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="221cd-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221cd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="221cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221cd-131">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="221cd-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




