---
description: Notifica a una Media Foundation trasformazione (MFT) che il flusso sta per iniziare.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226529"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="3bd68-103">\_notifica di \_ \_ inizio \_ trasmissione del messaggio MFT</span><span class="sxs-lookup"><span data-stu-id="3bd68-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="3bd68-104">Notifica a una Media Foundation trasformazione (MFT) che il flusso sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="3bd68-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="3bd68-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="3bd68-105">Message Parameter</span></span>

<span data-ttu-id="3bd68-106">No.</span><span class="sxs-lookup"><span data-stu-id="3bd68-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd68-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3bd68-107">Remarks</span></span>

<span data-ttu-id="3bd68-108">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="3bd68-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="3bd68-109">Il client non è necessario per l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3bd68-109">The client is not required to send this message.</span></span> <span data-ttu-id="3bd68-110">Se il client invia questo messaggio, è necessario eseguire questa operazione dopo avere impostato tutti i tipi di supporto in MFT e prima di chiamare [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="3bd68-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="3bd68-111">Il MFT può rispondere allocando buffer o altre risorse.</span><span class="sxs-lookup"><span data-stu-id="3bd68-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="3bd68-112">Se il client non invia questo messaggio, il MFT alloca le risorse alla prima chiamata a **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="3bd68-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="3bd68-113">Pertanto, l'invio di questo messaggio può ridurre la latenza iniziale all'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="3bd68-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="3bd68-114">Implementazione</span><span class="sxs-lookup"><span data-stu-id="3bd68-114">Implementation</span></span>

<span data-ttu-id="3bd68-115">Non è necessario un MFT per rispondere a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3bd68-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd68-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bd68-116">Requirements</span></span>



| <span data-ttu-id="3bd68-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd68-117">Requirement</span></span> | <span data-ttu-id="3bd68-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3bd68-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd68-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bd68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd68-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bd68-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3bd68-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bd68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd68-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3bd68-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bd68-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bd68-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bd68-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd68-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd68-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bd68-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd68-126">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="3bd68-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




