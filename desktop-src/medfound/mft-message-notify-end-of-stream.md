---
description: Notifica a un Media Foundation trasformazione (MFT) che un flusso di input è terminato.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310215"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="a1236-103">\_ \_ \_ fine \_ del flusso di notifica del messaggio MFT \_</span><span class="sxs-lookup"><span data-stu-id="a1236-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="a1236-104">Notifica a un Media Foundation trasformazione (MFT) che un flusso di input è terminato.</span><span class="sxs-lookup"><span data-stu-id="a1236-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="a1236-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="a1236-105">Message Parameter</span></span>

<span data-ttu-id="a1236-106">Il parametro *ulParam* contiene l'identificatore del flusso di input, specificato come valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a1236-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="a1236-107">Nelle applicazioni a 64 bit, inserire questo valore nei 32 bit inferiori del **\_ ptr ULONG**.</span><span class="sxs-lookup"><span data-stu-id="a1236-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1236-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1236-108">Remarks</span></span>

<span data-ttu-id="a1236-109">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="a1236-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="a1236-110">Il client non è necessario per l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a1236-110">The client is not required to send this message.</span></span>

<span data-ttu-id="a1236-111">Al termine di un flusso, il client può chiamare nuovamente [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per inviare i nuovi dati per il flusso.</span><span class="sxs-lookup"><span data-stu-id="a1236-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="a1236-112">In tal caso, il client deve impostare l'attributo discontinuity (attributo [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) ) sul primo campione di input dopo la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="a1236-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="a1236-113">Il client deve sempre impostare questo attributo sul primo nuovo campione dopo la fine di un flusso, indipendentemente dal fatto che il client abbia inviato il messaggio MFT per la **\_ \_ notifica \_ \_ della fine del \_ flusso** .</span><span class="sxs-lookup"><span data-stu-id="a1236-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="a1236-114">Per ulteriori informazioni sulla gestione delle discontinuità, vedere [Basic MFT Processing Model](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="a1236-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="a1236-115">Dopo l'invio di questo messaggio per ogni flusso di input, il client in genere invia un comando di **\_ svuotamento del \_ comando \_ del messaggio MFT** e quindi raccoglie l'output rimanente.</span><span class="sxs-lookup"><span data-stu-id="a1236-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="a1236-116">Tuttavia, non è necessario che il client scarichi il MFT.</span><span class="sxs-lookup"><span data-stu-id="a1236-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="a1236-117">Se il client non svuota il computer MFT, in genere il MFT eliminerà tutti i dati non elaborati alla chiamata successiva a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), quando rileverà la discontinuità del flusso.</span><span class="sxs-lookup"><span data-stu-id="a1236-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="a1236-118">In alternativa, il client potrebbe scaricare il MFT prima di chiamare **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="a1236-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="a1236-119">Questo messaggio non rimuove il flusso di input o Reimposta il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a1236-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="a1236-120">Implementazione</span><span class="sxs-lookup"><span data-stu-id="a1236-120">Implementation</span></span>

<span data-ttu-id="a1236-121">Non è necessario un MFT per rispondere a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a1236-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1236-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1236-122">Requirements</span></span>



| <span data-ttu-id="a1236-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1236-123">Requirement</span></span> | <span data-ttu-id="a1236-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a1236-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1236-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1236-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a1236-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1236-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a1236-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1236-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a1236-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1236-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1236-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1236-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1236-130"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1236-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1236-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1236-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1236-132">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="a1236-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




