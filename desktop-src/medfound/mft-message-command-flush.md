---
description: 'MFT_MESSAGE_COMMAND_FLUSH: richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092739"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="e80e9-103">MFT \_ MESSAGE \_ COMMAND \_ FLUSH</span><span class="sxs-lookup"><span data-stu-id="e80e9-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="e80e9-104">Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="e80e9-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="e80e9-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="e80e9-105">Message Parameter</span></span>

<span data-ttu-id="e80e9-106">No.</span><span class="sxs-lookup"><span data-stu-id="e80e9-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e80e9-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e80e9-107">Remarks</span></span>

<span data-ttu-id="e80e9-108">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="e80e9-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="e80e9-109">Dopo l'invio di questo messaggio, il MFT può accettare nuovi esempi di input.</span><span class="sxs-lookup"><span data-stu-id="e80e9-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="e80e9-110">I tipi di supporti correnti non vengono invalidati.</span><span class="sxs-lookup"><span data-stu-id="e80e9-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="e80e9-111">Implementazione</span><span class="sxs-lookup"><span data-stu-id="e80e9-111">Implementation</span></span>

<span data-ttu-id="e80e9-112">Tutti i MFT devono implementare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="e80e9-112">All MFTs must implement this message.</span></span> <span data-ttu-id="e80e9-113">Quando riceve questo messaggio, il MFT deve rimuovere tutti i campioni di supporti in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="e80e9-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="e80e9-114">[MFT](asynchronous-mfts.md)asincroni: MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) dal client.</span><span class="sxs-lookup"><span data-stu-id="e80e9-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80e9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e80e9-115">Requirements</span></span>



| <span data-ttu-id="e80e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80e9-116">Requirement</span></span> | <span data-ttu-id="e80e9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e80e9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80e9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e80e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e80e9-119">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e80e9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e80e9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e80e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e80e9-121">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e80e9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e80e9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e80e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80e9-123"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="e80e9-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80e9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e80e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80e9-125">**TIPO DI \_ MESSAGGIO \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="e80e9-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




