---
description: Richiede una trasformazione Media Foundation (MFT) a tale flusso sta per terminare.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527913"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="c5c88-103">\_ \_ \_ flusso finale notifiche messaggio \_ MFT</span><span class="sxs-lookup"><span data-stu-id="c5c88-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="c5c88-104">Richiede una trasformazione Media Foundation (MFT) a tale flusso sta per terminare.</span><span class="sxs-lookup"><span data-stu-id="c5c88-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="c5c88-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="c5c88-105">Message Parameter</span></span>

<span data-ttu-id="c5c88-106">No.</span><span class="sxs-lookup"><span data-stu-id="c5c88-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c88-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c5c88-107">Remarks</span></span>

<span data-ttu-id="c5c88-108">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="c5c88-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="c5c88-109">Il client non deve inviare questo messaggio, anche se il client ha inviato in precedenza il messaggio relativo all' **\_ inizio del \_ \_ \_ flusso di notifica del messaggio MFT** .</span><span class="sxs-lookup"><span data-stu-id="c5c88-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="c5c88-110">Implementazione</span><span class="sxs-lookup"><span data-stu-id="c5c88-110">Implementation</span></span>

<span data-ttu-id="c5c88-111">Il MFT può rispondere a questo messaggio rilasciando i buffer e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="c5c88-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="c5c88-112">MFT non Scarica i dati di input o Reimposta i tipi di supporto in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c5c88-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="c5c88-113">Non è necessario un MFT per rispondere a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c5c88-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c88-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5c88-114">Requirements</span></span>



| <span data-ttu-id="c5c88-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c88-115">Requirement</span></span> | <span data-ttu-id="c5c88-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c5c88-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c88-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c88-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5c88-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5c88-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c88-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5c88-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5c88-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5c88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c88-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c88-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c88-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5c88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c88-124">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="c5c88-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




