---
description: Notifica a un Media Foundation Transform (MFT) che il primo campione sta per essere elaborato.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049665"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="a4c6b-103">\_ \_ avvio notifica messaggio \_ MFT \_ del \_ flusso</span><span class="sxs-lookup"><span data-stu-id="a4c6b-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="a4c6b-104">Notifica a un Media Foundation Transform (MFT) che il primo campione sta per essere elaborato.</span><span class="sxs-lookup"><span data-stu-id="a4c6b-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="a4c6b-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="a4c6b-105">Message Parameter</span></span>

<span data-ttu-id="a4c6b-106">No.</span><span class="sxs-lookup"><span data-stu-id="a4c6b-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c6b-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a4c6b-107">Remarks</span></span>

<span data-ttu-id="a4c6b-108">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="a4c6b-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="a4c6b-109">Per MFTs sincrono, è facoltativo inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a4c6b-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="a4c6b-110">Per MFTs asincrono, il client deve inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a4c6b-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="a4c6b-111">Implementazione</span><span class="sxs-lookup"><span data-stu-id="a4c6b-111">Implementation</span></span>

<span data-ttu-id="a4c6b-112">Non è necessario un MFT sincrono per rispondere al messaggio.</span><span class="sxs-lookup"><span data-stu-id="a4c6b-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="a4c6b-113">Un MFT asincrono deve implementare questo messaggio, come descritto in [MFTS asincrono](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="a4c6b-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c6b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4c6b-114">Requirements</span></span>



| <span data-ttu-id="a4c6b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c6b-115">Requirement</span></span> | <span data-ttu-id="a4c6b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c6b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c6b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4c6b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c6b-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4c6b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a4c6b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4c6b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c6b-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4c6b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a4c6b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4c6b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c6b-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c6b-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c6b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4c6b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c6b-124">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="a4c6b-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




